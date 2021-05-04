# dublicateEncoder



function duplicateEncode(word) {
            const new_word = word.toUpperCase();
            let newString1 = [];
            for (let i = 0; i < new_word.length; i++) {
                // debugger;

                if (new_word.includes(new_word[i], i + 1) == true) {
                    newString1.push(')');
                }

                else if (i - 1 == 0 || i !== 0) {

                    var a = Math.abs(i - 1);
                    if (new_word.lastIndexOf(new_word[i], a) == -1) {
                        newString1.push('(');
                    } else {
                        newString1.push(')');
                    }

                } else {
                    newString1.push('(');

                }


            }
            let newString2 = newString1.toString();
            let result = newString2.replace(/,/g, "");
            return result;
        }
