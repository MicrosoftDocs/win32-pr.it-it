---
description: Questo argomento descrive come usare i nomi di dominio internazionalizzati (IDN) nelle applicazioni.
ms.assetid: e0ca356e-f8c1-4845-ae1e-ce2ae8987515
title: Gestione dei nomi di dominio internazionalizzati (IDN)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6310cf74e39758dc6974a1247fe9a5b506276f5c3da55d546d6bc6c2b5a8c992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898587"
---
# <a name="handling-internationalized-domain-names-idns"></a>Gestione dei nomi di dominio internazionalizzati (IDN)

Questo argomento descrive come usare i nomi di dominio internazionalizzati (IDN) nelle applicazioni. Gli IDN vengono specificati da NETWORK Working Group [RFC 3490: Internationalizing Domain Names in Applications (IDNA).](http://www.faqs.org/rfcs/rfc3490.html) Prima di questa bozza di standard, gli IDN erano limitati ai caratteri latini senza segni diacritici. IDNA consente agli IDN di includere caratteri latini con segni diacritici, insieme ai caratteri di script non latini, ad esempio cirillico, arabo e cinese. Lo standard stabilisce anche regole per il mapping degli IDN ai nomi di dominio solo ASCII. I problemi IDNA possono quindi essere gestiti sul lato client, senza richiedere modifiche al server dei nomi di dominio (DNS).

> [!Caution]  
> RFC 3490 introduce una serie di problemi di sicurezza correlati all'uso di IDN. Per altre informazioni, vedere la sezione correlata Considerazioni [sulla sicurezza: Funzionalità internazionali](security-considerations--international-features.md).

 

> [!Note]  
> IDNA è attualmente basato su Unicode 3.2.

 

## <a name="nls-api-functions-for-handling-idns"></a>NLS API funzioni per la gestione degli IDN

NLS include le funzioni di conversione seguenti che l'applicazione può usare per convertire un IDN in rappresentazioni diverse. Per un esempio dell'uso di queste funzioni, vedere [NLS: Internationalized Domain Name (IDN) Conversion Sample](nls--internationalized-domain-name--idn--conversion-sample.md).

-   [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii). Converte un IDN in Punycode.
-   [**IdnToNameprepUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntonameprepunicode). Esegue la parte NamePrep della conversione di un IDN in un nome ASCII. Questa funzione crea una rappresentazione Unicode canonica di una stringa.
-   [**IdnToUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntounicode). Converte una stringa Punycode in una normale stringa UTF-16.

NLS definisce anche diverse funzioni API che possono essere usate per attenuare alcuni dei rischi per la sicurezza presentati dalla tecnologia IDN. In Windows Vista e versioni successive, le funzioni seguenti vengono usate per verificare che i caratteri in un IDN specifico siano tratti interamente dagli script associati a determinate impostazioni locali o impostazioni locali. Per un esempio dell'uso di queste funzioni, vedere [NLS: Internationalized Domain Name (IDN) Mitigation Sample](nls--internationalized-domain-name--idn--mitigation-sample.md).

-   [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts). Fornisce un elenco di script utilizzati in una determinata stringa.
-   [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa), [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex). Recuperare le informazioni sulle impostazioni locali. L'uso delle funzioni *con LCType* impostato su [LOCALE \_ SSCRIPTS](locale-sscripts.md) fornisce un elenco di script normalmente usati per determinate impostazioni locali.
-   [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts). Confronta gli elenchi di script. Per verificare in base a più impostazioni locali, l'applicazione può eseguire più chiamate a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) e [**VerifyScripts.**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)

Per le applicazioni eseguite in Windows XP e Windows Server 2003, le funzioni [**DownlevelGetLocaleScripts,**](downlevelgetlocalescripts.md) [**DownlevelGetStringScripts**](downlevelgetstringscripts.md)e [**DownlevelVerifyScripts**](downlevelverifyscripts.md) svolgono un ruolo simile alle funzioni elencate in precedenza per attenuare i rischi di sicurezza. Il download ["MICROSOFT Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) è disponibile nell'Area [download MSDN.](https://www.microsoft.com/?ref=go)

## <a name="handle-unicode-strings"></a>Gestire stringhe Unicode

IDNA supporta la trasformazione di stringhe Unicode in etichette di nomi host legittime, ad eccezione delle stringhe contenenti determinati caratteri non consentiti, ad esempio caratteri di controllo, caratteri dell'area di utilizzo privato (PUA) e simili. L'applicazione può usare il flag IDN USE STD3 ASCII RULES con diverse funzioni di conversione NLS per forzare l'esito negativo delle funzioni se rilevano caratteri ASCII diversi da lettere, numeri o trattini meno \_ (-) o se una stringa inizia o termina con il trattino \_ \_ \_ meno. A questi caratteri è sempre stato vietato l'uso nei nomi di dominio e rimangono vietati nella bozza di standard.

## <a name="handle-unassigned-code-points"></a>Gestire i punti di codice non assegnati

Gli IDN non possono contenere punti di codice non assegnati. Pertanto, i punti di codice non associati a un carattere ("assegnato") a livello di Unicode 3.2 non hanno mapping IDN definiti, anche se il flag IDN ALLOW UNASSIGNED in determinate funzioni di conversione ne consente il mapping a \_ \_ Punycode. È possibile trovare un elenco di punti di codice non assegnati in [RFC 3454](http://www.faqs.org/rfcs/rfc3454.html).

> [!Caution]  
> Se l'applicazione codifica i punti di codice non assegnati come Punycode, i nomi di dominio risultanti non devono essere validi. La sicurezza può essere compromessa se una versione successiva di IDNA rende validi questi nomi o se l'applicazione filtra i caratteri non validi per tentare di creare un nome di dominio valido.

 

I punti di codice non assegnati non sono consentiti nelle stringhe archiviate usate negli identificatori di protocollo e nelle entità denominate, ad esempio i nomi nei certificati digitali e nelle parti del nome di dominio DNS. Tuttavia, i punti di codice sono consentiti nelle stringhe di query, ad esempio i nomi immessi dall'utente per le autorità di certificazione digitali e le ricerche DNS, che vengono usati per la corrispondenza con gli identificatori archiviati.

> [!Caution]  
> Anche se le stringhe di query possono usare punti di codice non assegnati, non è consigliabile usarli nelle applicazioni. Anche una stringa di query fornita dall'utente presenta il rischio di un attacco di "spoofing". In questo tipo di attacco, il sito host senza scrupoli reindirizza gli utenti dal sito a cui intendono accedere a un altro sito che potrebbe fornire informazioni riservate a terze parti. Ad esempio, la copia di una stringa da un messaggio di posta elettronica in arrivo può presentare gli stessi rischi di fare clic su un collegamento in un browser.

 

## <a name="convert-domain-names-to-ascii-names"></a>Convertire i nomi di dominio in nomi ASCII

L'applicazione può usare la [**funzione IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii) e alcune funzioni di mitigazione per convertire gli IDN in ASCII.

> [!Caution]  
> Poiché le stringhe con rappresentazioni binarie molto diverse possono essere confrontate come identiche, questa funzione può generare determinati problemi di sicurezza. Per altre informazioni, vedere la discussione sulle funzioni di confronto in [Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

## <a name="examples"></a>Esempio

[Esempio di conversione NLS: IDN (Internationalized Domain Name)](nls--internationalized-domain-name--idn--conversion-sample.md) illustra l'uso delle funzioni di conversione IDN. [NLS: Internationalized Domain Name (IDN) Mitigation Sample](nls--internationalized-domain-name--idn--mitigation-sample.md) illustra l'uso delle funzioni di mitigazione IDN.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto linguistico nazionale](using-national-language-support.md)
</dt> <dt>

[Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md)
</dt> </dl>

 

 



