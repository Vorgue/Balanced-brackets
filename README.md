# Balanced-brackets
I can't believe I'm doing this

    function balancedBrackets(str) {
      var brackets = str.split('').filter(x => (x === '[') || (x === ']')).join('');
      if (brackets == '') return true;
      var stack = [];
      for (var i = 0; i < brackets.length; i++) {
        if ((brackets[i] === ']') && (stack == '')) return false;
        if (brackets[i] === '[') stack.push('[')
        else if (brackets[i] === ']') stack.pop(']');
      }
      if (stack == '') return true;	
      return false
    }
