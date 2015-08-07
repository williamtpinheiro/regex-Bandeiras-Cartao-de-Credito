# regex-Bandeiras-Cartao-de-Credito
regex Bandeiras Cartao de Credito
```
function detectCardType(number) {
    var re = {
        visa: /^4[0-9]{12}(?:[0-9]{3})?$/,
        mastercard: /^5[1-5][0-9]{14}$/,
        amex: /^3[47][0-9]{13}$/,
        diners: /^3(?:0[0-5]|[68][0-9])[0-9]{11}$/,
        discover: /^6(?:011|5[0-9]{2})[0-9]{12}$/,
        hipercard: /^(606282\d{10}(\d{3})?)|(3841\d{15})$/,
        elo: /^((((636368)|(438935)|(504175)|(451416)|(636297))\d{0,10})|((5067)|(4576)|(4011))\d{0,12})$/,
        aura: /^(5078\d{2})(\d{2})(\d{11})$/
    };
    if (re.visa.test(number)) {
        return 'visa';
    } else if (re.mastercard.test(number)) {
        return 'mastercard';
    } else if (re.amex.test(number)) {
        return 'amex';
    } else if (re.diners.test(number)) {
        return 'diners';
    } else if (re.discover.test(number)) {
        return 'discover';
    } else if (re.hipercard.test(number)) {
        return 'hipercard';
    } else if (re.elo.test(number)) {
    	return 'elo';
    } else if (re.aura.test(number)) {
    	return 'aura';
    } else {
        return undefined;
    }
}
```
