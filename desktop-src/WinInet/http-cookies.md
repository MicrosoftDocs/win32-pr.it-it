---
title: Cookie HTTP
description: I cookie HTTP forniscono al server un meccanismo per archiviare e recuperare informazioni sullo stato nel sistema dell'applicazione client.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ba5b2d3917ea8f140e334f5f78b1bd730908d25506d9023667403410833c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113715"
---
# <a name="http-cookies"></a>Cookie HTTP

I cookie HTTP forniscono al server un meccanismo per archiviare e recuperare informazioni sullo stato nel sistema dell'applicazione client. Questo meccanismo consente alle applicazioni basate sul Web di archiviare informazioni su elementi selezionati, preferenze utente, informazioni di registrazione e altre informazioni che possono essere recuperate in un secondo momento.

## <a name="cookie-related-headers"></a>Cookie-Related intestazioni

Esistono due intestazioni, Set-Cookie e Cookie, correlate ai cookie. LSet-Cookie'intestazione viene inviata dal server in risposta a una richiesta HTTP, usata per creare un cookie nel sistema dell'utente. L'intestazione Cookie viene inclusa dall'applicazione client con una richiesta HTTP inviata a un server, se è presente un cookie con un dominio e un percorso corrispondenti.

### <a name="set-cookie-header"></a>intestazione Set-Cookie

LSet-Cookie intestazione della risposta usa il formato seguente:

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

Una o più sequenze di stringhe (separate da punti e virgola) che seguono il valore del nome del modello devono essere incluse nell'intestazione Set-Cookie =  risposta. Il server può usare queste sequenze di stringhe per archiviare i dati nel sistema del client.

La data di scadenza viene impostata usando il formato expires=*date*, dove *date* è la data di scadenza nell'ora di Greenwich (GMT). Se la data di scadenza non è impostata, il cookie scade al termine della sessione Internet. In caso contrario, il cookie viene mantenuto nella cache fino alla data di scadenza. La data deve usare il formato seguente:

*DAY*, *DD* - *MMM* - *YYYY* *HH*:*MM*:*SS* GMT

<dl> <dt>

<span id="DAY"></span><span id="day"></span>*Giorno*
</dt> <dd>

Giorno della settimana (dom, lun, mar, mer, gio, ven, sab).

</dd> <dt>

<span id="DD"></span><span id="dd"></span>*Dd*
</dt> <dd>

Giorno del mese (ad esempio 01 per il primo giorno del mese).

</dd> <dt>

<span id="MMM"></span><span id="mmm"></span>*Mmm*
</dt> <dd>

Abbreviazione di tre lettere per il mese (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec).

</dd> <dt>

<span id="YYYY"></span><span id="yyyy"></span>*Aaaa*
</dt> <dd>

Anno.

</dd> <dt>

<span id="HH"></span><span id="hh"></span>*Hh*
</dt> <dd>

Valore dell'ora in tempo reale (ad esempio, 22 sarebbero le 22.00).

</dd> <dt>

<span id="MM"></span><span id="mm"></span>*Mm*
</dt> <dd>

Valore dei minuti.

</dd> <dt>

<span id="SS"></span><span id="ss"></span>*Ss*
</dt> <dd>

Secondo valore.

</dd> </dl>

Specificare il nome di dominio, usando il modello dominio = nome di dominio , è facoltativo per i cookie persistenti e viene usato per indicare la fine del dominio per cui il cookie è valido.*\_* I cookie di sessione che specificano un dominio vengono rifiutati. Se il nome di dominio specificato termina con la richiesta, il cookie tenta di trovare la corrispondenza con il percorso per determinare se il cookie deve essere inviato. Ad esempio, se il nome di dominio finale è .microsoft.com, le richieste a home.microsoft.com e support.microsoft.com verranno controllate per verificare se il modello specificato corrisponde alla richiesta. Il nome di dominio deve contenere almeno due o tre punti per impedire che i cookie vengano impostati per le terminazioni dei nomi di dominio ampiamente usate, ad esempio .com, .edu e co.jp. I nomi di dominio consentiti saranno simili a .microsoft.com, .someschool.edu e .someserver.co.jp. Solo gli host all'interno del dominio specificato possono impostare un cookie per un dominio.

L'impostazione del percorso, usando il modello path= un percorso , è facoltativa e può essere usata per specificare un subset degli URL per cui il cookie è valido.*\_* Se viene specificato un percorso, il cookie viene considerato valido per tutte le richieste che corrispondono a tale percorso. Ad esempio, se il percorso specificato è /example, le richieste con i percorsi /examplecode e /example/code.htm corrisponderebbero. Se non viene specificato alcun percorso, si presuppone che sia il percorso della risorsa associata all'intestazione Set-Cookie specificata.

Il cookie può anche essere contrassegnato come sicuro, che specifica che il cookie può essere inviato solo ai server HTTPS.

Infine, un cookie può essere contrassegnato come HttpOnly (gli attributi non supportano la distinzione tra maiuscole e minuscole), per indicare che il cookie non è gestibile tramite script e non deve essere rivelato all'applicazione client, per motivi di sicurezza. All Windows Internet, ciò significa che il cookie non può essere recuperato tramite la **funzione InternetGetCookie.**

### <a name="cookie-header"></a>Intestazione cookie

L'intestazione Cookie è inclusa in tutte le richieste HTTP con un cookie il cui dominio e percorso corrispondono alla richiesta. L'intestazione Cookie ha il formato seguente:

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

Una o più sequenze di stringhe, usando il valore del *nome di* formato , contengono le informazioni impostate nel = cookie.

## <a name="generating-cookies"></a>Generazione di cookie

Esistono tre metodi per generare cookie per Microsoft Internet Explorer: uso di Microsoft JScript, uso delle funzioni WinINet e uso di uno script CGI. Tutti i metodi devono impostare le informazioni incluse nell'intestazione Set-Cookie personalizzata.

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a>Generazione di un cookie tramite il modello a oggetti DHTML

Usando il modello a oggetti DHTML (Dynamic HTML), i cookie possono essere impostati chiamando la proprietà **cookie** dell'oggetto documento, come illustrato nell'esempio seguente.

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a>Generazione di un cookie tramite le funzioni WinInet

I cookie possono essere creati da applicazioni che usano [**la funzione InternetSetCookie.**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) Per altre informazioni, vedere [Impostazione di un cookie.](managing-cookies.md)

### <a name="generating-a-cookie-using-a-cgi-script"></a>Generazione di un cookie tramite uno script CGI

I cookie vengono generati includendo Set-Cookie'intestazione come parte di uno script CGI incluso nella risposta HTTP a una richiesta.

L'esempio seguente è uno script CGI che include un'Set-Cookie con Perl.

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi server, [usare Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 