---
title: Cookie HTTP
description: I cookie HTTP forniscono al server un meccanismo per archiviare e recuperare le informazioni sullo stato nel sistema dell'applicazione client.
ms.assetid: c3574592-572f-4fde-adfa-aed3e862f13f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6855f0b105dc73760541bf9eb7a6da80dfb38e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300032"
---
# <a name="http-cookies"></a>Cookie HTTP

I cookie HTTP forniscono al server un meccanismo per archiviare e recuperare le informazioni sullo stato nel sistema dell'applicazione client. Questo meccanismo consente alle applicazioni basate sul Web di archiviare informazioni sugli elementi selezionati, le preferenze utente, le informazioni di registrazione e altre informazioni che possono essere recuperate in un secondo momento.

## <a name="cookie-related-headers"></a>Intestazioni Cookie-Related

Sono disponibili due intestazioni, Set-Cookie e cookie, correlate ai cookie. L'intestazione Set-Cookie viene inviata dal server in risposta a una richiesta HTTP, che viene utilizzata per creare un cookie nel sistema dell'utente. L'intestazione del cookie è inclusa dall'applicazione client con una richiesta HTTP inviata a un server, se è presente un cookie con un dominio e un percorso corrispondenti.

### <a name="set-cookie-header"></a>Intestazione Set-Cookie

L'intestazione della risposta Set-Cookie usa il formato seguente:

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

Una o più sequenze di stringhe (separate da punti e virgola) che seguono il valore del *nome* del modello =  devono essere incluse nell'intestazione della risposta Set-Cookie. Il server può utilizzare queste sequenze di stringhe per archiviare i dati nel sistema del client.

La data di scadenza viene impostata utilizzando il formato scade =*Data*, dove *Data* è la data di scadenza nell'ora di Greenwich (GMT). Se la data di scadenza non è impostata, il cookie scade al termine della sessione Internet. In caso contrario, il cookie viene mantenuto nella cache fino alla data di scadenza. La data deve usare il formato seguente:

*giorno*, *GG* - *mmm* - *aaaa* *HH*:*mm*:*ss* GMT

<dl> <dt>

<span id="DAY"></span><span id="day"></span>*GIORNO*
</dt> <dd>

Il giorno della settimana (Sun, Mon, Mar, Mer, Gio, ven, Sat).

</dd> <dt>

<span id="DD"></span><span id="dd"></span>*GG*
</dt> <dd>

Il giorno del mese, ad esempio 01 per il primo giorno del mese.

</dd> <dt>

<span id="MMM"></span><span id="mmm"></span>*MMM*
</dt> <dd>

Abbreviazione di tre lettere per il mese (gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, Dec).

</dd> <dt>

<span id="YYYY"></span><span id="yyyy"></span>*AAAA*
</dt> <dd>

Anno.

</dd> <dt>

<span id="HH"></span><span id="hh"></span>*HH*
</dt> <dd>

Il valore dell'ora nell'ora militare, ad esempio 22 è 10:00.

</dd> <dt>

<span id="MM"></span><span id="mm"></span>*MM*
</dt> <dd>

Valore dei minuti.

</dd> <dt>

<span id="SS"></span><span id="ss"></span>*SS*
</dt> <dd>

Secondo valore.

</dd> </dl>

Specificare il nome di dominio, usando il modello Domain =*Domain \_ Name*, è facoltativo per i cookie permanenti e viene usato per indicare la fine del dominio per il quale il cookie è valido. I cookie di sessione che specificano un dominio vengono rifiutati. Se il nome di dominio specificato che termina corrisponde alla richiesta, il cookie tenta di trovare la corrispondenza con il percorso per determinare se il cookie deve essere inviato. Ad esempio, se il nome di dominio che termina è. microsoft.com, le richieste a home.microsoft.com e support.microsoft.com vengono controllate per verificare se il modello specificato corrisponde alla richiesta. Il nome di dominio deve avere almeno due o tre punti per impedire l'impostazione dei cookie per le terminazioni del nome di dominio ampiamente utilizzate, ad esempio. com,. edu e co.jp. I nomi di dominio consentiti saranno simili a. microsoft.com,. someschool.edu e. someserver.co.jp. Solo gli host nel dominio specificato possono impostare un cookie per un dominio.

L'impostazione del percorso, usando il percorso del pattern =*some \_ path*, è facoltativa e può essere usata per specificare un subset degli URL per i quali il cookie è valido. Se viene specificato un percorso, il cookie viene considerato valido per tutte le richieste corrispondenti a tale percorso. Se, ad esempio, il percorso specificato è/example, le richieste con i percorsi/ExampleCode e/example/code.htm corrisponderanno. Se non viene specificato alcun percorso, si presuppone che il percorso corrisponda al percorso della risorsa associata all'intestazione Set-Cookie.

Il cookie può anche essere contrassegnato come protetto, che specifica che il cookie può essere inviato solo ai server HTTPS.

Infine, un cookie può essere contrassegnato come HttpOnly (gli attributi non fanno distinzione tra maiuscole e minuscole), per indicare che il cookie non è configurabile tramite script e non deve essere rivelato all'applicazione client, per motivi di sicurezza. All'interno di Windows Internet, ciò significa che non è possibile recuperare il cookie tramite la funzione **InternetGetCookie** .

### <a name="cookie-header"></a>Intestazione cookie

L'intestazione del cookie è inclusa in tutte le richieste HTTP con un cookie il cui dominio e percorso corrispondono alla richiesta. Il formato dell'intestazione del cookie è il seguente:

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

Una o più sequenze di stringhe, usando il valore del *nome* formato = , contengono le informazioni impostate nel cookie.

## <a name="generating-cookies"></a>Generazione di cookie

Sono disponibili tre metodi per la generazione di cookie per Microsoft Internet Explorer: utilizzo di Microsoft JScript, utilizzo delle funzioni WinINet e utilizzo di uno script CGI. Tutti i metodi devono impostare le informazioni incluse nell'intestazione Set-Cookie.

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a>Generazione di un cookie con il modello a oggetti DHTML

Usando il modello a oggetti DHTML (Dynamic HTML), i cookie possono essere impostati chiamando la proprietà **cookie** dell'oggetto Document, come illustrato nell'esempio seguente.

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a>Generazione di un cookie mediante le funzioni WinInet

I cookie possono essere creati dalle applicazioni mediante la funzione [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) . Per ulteriori informazioni, vedere [impostazione di un cookie](managing-cookies.md).

### <a name="generating-a-cookie-using-a-cgi-script"></a>Generazione di un cookie mediante uno script CGI

I cookie vengono generati includendo un'intestazione Set-Cookie come parte di uno script CGI incluso nella risposta HTTP a una richiesta.

L'esempio seguente è uno script CGI che include un'intestazione Set-Cookie usando Perl.

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 