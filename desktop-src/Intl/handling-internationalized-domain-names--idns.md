---
description: In questo argomento viene descritto come usare i nomi di dominio internazionalizzazione (IDN) nelle applicazioni.
ms.assetid: e0ca356e-f8c1-4845-ae1e-ce2ae8987515
title: Gestione dei nomi di dominio internazionalizzati (IDN)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95e853f0ea3f62fc3e5ee848431417cc031eaa5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232451"
---
# <a name="handling-internationalized-domain-names-idns"></a>Gestione dei nomi di dominio internazionalizzati (IDN)

In questo argomento viene descritto come usare i nomi di dominio internazionalizzazione (IDN) nelle applicazioni. IDN sono specificati dal gruppo di lavoro di rete [RFC 3490: internazionalizzazione Domain Names in Applications (IDNA)](http://www.faqs.org/rfcs/rfc3490.html). Prima di questa bozza standard, IDN era limitato ai caratteri latini senza segni diacritici. IDNA consente a IDN di includere caratteri latini con segni diacritici, insieme ai caratteri degli script non latini, ad esempio cirillico, arabo e cinese. Lo standard stabilisce inoltre regole per il mapping di IDN a nomi di dominio solo ASCII. Di conseguenza, i problemi di IDNA possono essere gestiti sul lato client, senza richiedere modifiche di Domain Name Server (DNS).

> [!Caution]  
> RFC 3490 introduce una serie di problemi di sicurezza relativi all'uso di IDN. Per ulteriori informazioni, vedere la sezione relativa alle [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

> [!Note]  
> IDNA è attualmente basato su Unicode 3,2.

 

## <a name="nls-api-functions-for-handling-idns"></a>Funzioni di NLS API per la gestione di IDN

NLS include le funzioni di conversione seguenti che l'applicazione può usare per convertire un IDN in rappresentazioni diverse. Per un esempio di utilizzo di queste funzioni, vedere [NLS: esempio di conversione IDN (International Domain Name)](nls--internationalized-domain-name--idn--conversion-sample.md).

-   [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii). Converte un oggetto IDN in Punycode.
-   [**IdnToNameprepUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntonameprepunicode). Esegue la parte profili Nameprep della conversione di un oggetto IDN in un nome ASCII. Questa funzione crea una rappresentazione Unicode canonica di una stringa.
-   [**IdnToUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntounicode). Converte una stringa Punycode in una stringa UTF-16 normale.

NLS definisce inoltre diverse funzioni API che possono essere utilizzate per attenuare alcuni dei rischi di sicurezza presentati dalla tecnologia IDN. In Windows Vista e versioni successive vengono usate le funzioni seguenti per verificare che i caratteri in un determinato IDN siano disegnati interamente dagli script associati a impostazioni locali o impostazioni locali specifiche. Per un esempio di utilizzo di queste funzioni, vedere [NLS: esempio di mitigazione di un nome di dominio internazionale (IDN)](nls--internationalized-domain-name--idn--mitigation-sample.md).

-   [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts). Fornisce un elenco di script utilizzati in una determinata stringa.
-   [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa), [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex). Recuperare le informazioni sulle impostazioni locali. L'uso delle funzioni con *LCType* impostato su [locale \_ SSCRIPTS](locale-sscripts.md) fornisce un elenco di script normalmente usati per determinate impostazioni locali.
-   [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts). Consente di confrontare elenchi di script. Per eseguire la verifica rispetto a più impostazioni locali, l'applicazione può effettuare più chiamate a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) e [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).

Per le applicazioni eseguite in Windows XP e Windows Server 2003, le funzioni [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md), [**DownlevelGetStringScripts**](downlevelgetstringscripts.md)e [**DownlevelVerifyScripts**](downlevelverifyscripts.md) svolgono un ruolo simile alle funzioni elencate in precedenza per attenuare i rischi per la sicurezza. Il download di ["API di mitigazione del nome di dominio Microsoft (IDN)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) è disponibile nell' [area download MSDN](https://www.microsoft.com/?ref=go).

## <a name="handle-unicode-strings"></a>Gestisci stringhe Unicode

IDNA supporta la trasformazione di stringhe Unicode in etichette nome host legittime, fatta eccezione per le stringhe contenenti determinati caratteri non consentiti, ad esempio i caratteri di controllo, i caratteri dell'area di utilizzo privato (PUA) e l'oggetto like. Nell'applicazione è possibile utilizzare il \_ \_ flag STD3 \_ ASCII \_ Rules con diverse funzioni di conversione NLS per forzare l'esito negativo delle funzioni se vengono rilevati caratteri ASCII diversi da lettere, numeri o il segno meno (-) carattere o se una stringa inizia o termina con il segno meno. Questi caratteri sono sempre stati proibiti all'uso nei nomi di dominio e rimangono proibiti nello standard Draft.

## <a name="handle-unassigned-code-points"></a>Gestisci punti di codice non assegnati

IDN non può contenere punti di codice non assegnati. Pertanto, i punti di codice che non sono associati a un carattere ("assegnato") a partire da Unicode 3,2 non dispongono di mapping IDN definiti, anche se \_ il \_ flag IDN Allow unattributed in determinate funzioni di conversione ne consente il mapping a Punycode. È possibile trovare un elenco di punti di codice non assegnati in [RFC 3454](http://www.faqs.org/rfcs/rfc3454.html).

> [!Caution]  
> Se l'applicazione codifica i punti di codice non assegnati come Punycode, i nomi di dominio risultanti non devono essere validi. La sicurezza può essere compromessa se una versione successiva di IDNA rende validi questi nomi o se l'applicazione filtra i caratteri non validi per tentare di creare un nome di dominio valido.

 

I punti di codice non assegnati non sono consentiti nelle stringhe archiviate usate negli identificatori di protocollo e nelle entità denominate, ad esempio nomi in certificati digitali e parti del nome di dominio DNS. Tuttavia, i punti di codice sono consentiti nelle stringhe di query, ad esempio i nomi immessi dall'utente per le autorità di certificazione digitali e le ricerche DNS, che vengono usate per la corrispondenza con gli identificatori archiviati.

> [!Caution]  
> Sebbene le stringhe di query possano usare i punti di codice non assegnati, è consigliabile non usarli nelle applicazioni. Anche una stringa di query fornita dall'utente presenta il rischio di un attacco di "spoofing". In questo tipo di attacco, il sito host senza scrupoli reindirizza gli utenti del sito che intendono accedere a un altro sito che potrebbe fornire informazioni riservate a terze parti. Ad esempio, la copia di una stringa da un messaggio di posta elettronica in arrivo può presentare gli stessi rischi che si può fare facendo clic su un collegamento in un browser.

 

## <a name="convert-domain-names-to-ascii-names"></a>Converte i nomi di dominio in nomi ASCII

L'applicazione può usare la funzione [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii) e alcune funzioni di mitigazione per convertire IDN in ASCII.

> [!Caution]  
> Poiché le stringhe con rappresentazioni binarie molto diverse possono essere paragonate allo stesso modo, questa funzione può generare determinati problemi di sicurezza. Per ulteriori informazioni, vedere la discussione sulle funzioni di confronto in [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

## <a name="examples"></a>Esempio

[NLS: l'esempio di conversione IDN (International Domain Name)](nls--internationalized-domain-name--idn--conversion-sample.md) illustra l'uso delle funzioni di conversione IDN. [NLS: esempio di mitigazione del nome di dominio internazionale (IDN)](nls--internationalized-domain-name--idn--mitigation-sample.md) che illustra l'uso delle funzioni di mitigazione IDN.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto per le lingue nazionali](using-national-language-support.md)
</dt> <dt>

[Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md)
</dt> </dl>

 

 



