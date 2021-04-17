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
# <a name="http-cookies"></a><span data-ttu-id="548b1-103">Cookie HTTP</span><span class="sxs-lookup"><span data-stu-id="548b1-103">HTTP Cookies</span></span>

<span data-ttu-id="548b1-104">I cookie HTTP forniscono al server un meccanismo per archiviare e recuperare le informazioni sullo stato nel sistema dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="548b1-104">HTTP cookies provide the server with a mechanism to store and retrieve state information on the client application's system.</span></span> <span data-ttu-id="548b1-105">Questo meccanismo consente alle applicazioni basate sul Web di archiviare informazioni sugli elementi selezionati, le preferenze utente, le informazioni di registrazione e altre informazioni che possono essere recuperate in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="548b1-105">This mechanism allows web-based applications the ability to store information about selected items, user preferences, registration information, and other information that can be retrieved later.</span></span>

## <a name="cookie-related-headers"></a><span data-ttu-id="548b1-106">Intestazioni Cookie-Related</span><span class="sxs-lookup"><span data-stu-id="548b1-106">Cookie-Related Headers</span></span>

<span data-ttu-id="548b1-107">Sono disponibili due intestazioni, Set-Cookie e cookie, correlate ai cookie.</span><span class="sxs-lookup"><span data-stu-id="548b1-107">There are two headers, Set-Cookie and Cookie, that are related to cookies.</span></span> <span data-ttu-id="548b1-108">L'intestazione Set-Cookie viene inviata dal server in risposta a una richiesta HTTP, che viene utilizzata per creare un cookie nel sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="548b1-108">The Set-Cookie header is sent by the server in response to an HTTP request, which is used to create a cookie on the user's system.</span></span> <span data-ttu-id="548b1-109">L'intestazione del cookie è inclusa dall'applicazione client con una richiesta HTTP inviata a un server, se è presente un cookie con un dominio e un percorso corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="548b1-109">The Cookie header is included by the client application with an HTTP request sent to a server, if there is a cookie that has a matching domain and path.</span></span>

### <a name="set-cookie-header"></a><span data-ttu-id="548b1-110">Intestazione Set-Cookie</span><span class="sxs-lookup"><span data-stu-id="548b1-110">Set-Cookie Header</span></span>

<span data-ttu-id="548b1-111">L'intestazione della risposta Set-Cookie usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="548b1-111">The Set-Cookie response header uses the following format:</span></span>

``` syntax
Set-Cookie: <name>=<value>[; <name>=<value>]...
[; expires=<date>][; domain=<domain_name>]
[; path=<some_path>][; secure][; httponly]
```

<span data-ttu-id="548b1-112">Una o più sequenze di stringhe (separate da punti e virgola) che seguono il valore del *nome* del modello =  devono essere incluse nell'intestazione della risposta Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="548b1-112">One or more string sequences (separated by semicolons) that follow the pattern *name*=*value* must be included in the Set-Cookie response header.</span></span> <span data-ttu-id="548b1-113">Il server può utilizzare queste sequenze di stringhe per archiviare i dati nel sistema del client.</span><span class="sxs-lookup"><span data-stu-id="548b1-113">The server can use these string sequences to store data on the client's system.</span></span>

<span data-ttu-id="548b1-114">La data di scadenza viene impostata utilizzando il formato scade =*Data*, dove *Data* è la data di scadenza nell'ora di Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="548b1-114">The expiration date is set by using the format expires=*date*, where *date* is the expiration date in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="548b1-115">Se la data di scadenza non è impostata, il cookie scade al termine della sessione Internet.</span><span class="sxs-lookup"><span data-stu-id="548b1-115">If the expiration date is not set, the cookie expires after the Internet session ends.</span></span> <span data-ttu-id="548b1-116">In caso contrario, il cookie viene mantenuto nella cache fino alla data di scadenza.</span><span class="sxs-lookup"><span data-stu-id="548b1-116">Otherwise, the cookie is persisted in the cache until the expiration date.</span></span> <span data-ttu-id="548b1-117">La data deve usare il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="548b1-117">The date must use the following format:</span></span>

<span data-ttu-id="548b1-118">*giorno*, *GG* - *mmm* - *aaaa* *HH*:*mm*:*ss* GMT</span><span class="sxs-lookup"><span data-stu-id="548b1-118">*DAY*, *DD*-*MMM*-*YYYY* *HH*:*MM*:*SS* GMT</span></span>

<dl> <dt>

<span data-ttu-id="548b1-119"><span id="DAY"></span><span id="day"></span>*GIORNO*</span><span class="sxs-lookup"><span data-stu-id="548b1-119"><span id="DAY"></span><span id="day"></span>*DAY*</span></span>
</dt> <dd>

<span data-ttu-id="548b1-120">Il giorno della settimana (Sun, Mon, Mar, Mer, Gio, ven, Sat).</span><span class="sxs-lookup"><span data-stu-id="548b1-120">The day of the week (Sun, Mon, Tue, Wed, Thu, Fri, Sat).</span></span>

</dd> <dt>

<span data-ttu-id="548b1-121"><span id="DD"></span><span id="dd"></span>*GG*</span><span class="sxs-lookup"><span data-stu-id="548b1-121"><span id="DD"></span><span id="dd"></span>*DD*</span></span>
</dt> <dd>

<span data-ttu-id="548b1-122">Il giorno del mese, ad esempio 01 per il primo giorno del mese.</span><span class="sxs-lookup"><span data-stu-id="548b1-122">The day in the month (such as 01 for the first day of the month).</span></span>

</dd> <dt>

<span data-ttu-id="548b1-123"><span id="MMM"></span><span id="mmm"></span>*MMM*</span><span class="sxs-lookup"><span data-stu-id="548b1-123"><span id="MMM"></span><span id="mmm"></span>*MMM*</span></span>
</dt> <dd>

<span data-ttu-id="548b1-124">Abbreviazione di tre lettere per il mese (gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, Dec).</span><span class="sxs-lookup"><span data-stu-id="548b1-124">The three-letter abbreviation for the month (Jan, Feb, Mar, Apr, May, Jun, Jul, Aug, Sep, Oct, Nov, Dec).</span></span>

</dd> <dt>

<span data-ttu-id="548b1-125"><span id="YYYY"></span><span id="yyyy"></span>*AAAA*</span><span class="sxs-lookup"><span data-stu-id="548b1-125"><span id="YYYY"></span><span id="yyyy"></span>*YYYY*</span></span>
</dt> <dd>

<span data-ttu-id="548b1-126">Anno.</span><span class="sxs-lookup"><span data-stu-id="548b1-126">The year.</span></span>

</dd> <dt>

<span data-ttu-id="548b1-127"><span id="HH"></span><span id="hh"></span>*HH*</span><span class="sxs-lookup"><span data-stu-id="548b1-127"><span id="HH"></span><span id="hh"></span>*HH*</span></span>
</dt> <dd>

<span data-ttu-id="548b1-128">Il valore dell'ora nell'ora militare, ad esempio 22 è 10:00.</span><span class="sxs-lookup"><span data-stu-id="548b1-128">The hour value in military time (22 would be 10:00 P.M., for example).</span></span>

</dd> <dt>

<span data-ttu-id="548b1-129"><span id="MM"></span><span id="mm"></span>*MM*</span><span class="sxs-lookup"><span data-stu-id="548b1-129"><span id="MM"></span><span id="mm"></span>*MM*</span></span>
</dt> <dd>

<span data-ttu-id="548b1-130">Valore dei minuti.</span><span class="sxs-lookup"><span data-stu-id="548b1-130">The minute value.</span></span>

</dd> <dt>

<span data-ttu-id="548b1-131"><span id="SS"></span><span id="ss"></span>*SS*</span><span class="sxs-lookup"><span data-stu-id="548b1-131"><span id="SS"></span><span id="ss"></span>*SS*</span></span>
</dt> <dd>

<span data-ttu-id="548b1-132">Secondo valore.</span><span class="sxs-lookup"><span data-stu-id="548b1-132">The second value.</span></span>

</dd> </dl>

<span data-ttu-id="548b1-133">Specificare il nome di dominio, usando il modello Domain =*Domain \_ Name*, è facoltativo per i cookie permanenti e viene usato per indicare la fine del dominio per il quale il cookie è valido.</span><span class="sxs-lookup"><span data-stu-id="548b1-133">Specifying the domain name, using the pattern domain=*domain\_name*, is optional for persistent cookies and is used to indicate the end of the domain for which the cookie is valid.</span></span> <span data-ttu-id="548b1-134">I cookie di sessione che specificano un dominio vengono rifiutati.</span><span class="sxs-lookup"><span data-stu-id="548b1-134">Session cookies that specify a domain are rejected.</span></span> <span data-ttu-id="548b1-135">Se il nome di dominio specificato che termina corrisponde alla richiesta, il cookie tenta di trovare la corrispondenza con il percorso per determinare se il cookie deve essere inviato.</span><span class="sxs-lookup"><span data-stu-id="548b1-135">If the specified domain name ending matches the request, the cookie tries to match the path to determine if the cookie should be sent.</span></span> <span data-ttu-id="548b1-136">Ad esempio, se il nome di dominio che termina è. microsoft.com, le richieste a home.microsoft.com e support.microsoft.com vengono controllate per verificare se il modello specificato corrisponde alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="548b1-136">For example, if the domain name ending is .microsoft.com, requests to home.microsoft.com and support.microsoft.com would be checked to see if the specified pattern matches the request.</span></span> <span data-ttu-id="548b1-137">Il nome di dominio deve avere almeno due o tre punti per impedire l'impostazione dei cookie per le terminazioni del nome di dominio ampiamente utilizzate, ad esempio. com,. edu e co.jp.</span><span class="sxs-lookup"><span data-stu-id="548b1-137">The domain name must have at least two or three periods in it to prevent cookies from being set for widely used domain name endings, such as .com, .edu, and co.jp.</span></span> <span data-ttu-id="548b1-138">I nomi di dominio consentiti saranno simili a. microsoft.com,. someschool.edu e. someserver.co.jp.</span><span class="sxs-lookup"><span data-stu-id="548b1-138">Allowable domain names would be similar to .microsoft.com, .someschool.edu, and .someserver.co.jp.</span></span> <span data-ttu-id="548b1-139">Solo gli host nel dominio specificato possono impostare un cookie per un dominio.</span><span class="sxs-lookup"><span data-stu-id="548b1-139">Only hosts within the specified domain can set a cookie for a domain.</span></span>

<span data-ttu-id="548b1-140">L'impostazione del percorso, usando il percorso del pattern =*some \_ path*, è facoltativa e può essere usata per specificare un subset degli URL per i quali il cookie è valido.</span><span class="sxs-lookup"><span data-stu-id="548b1-140">Setting the path, using the pattern path=*some\_path*, is optional and can be used to specify a subset of the URLs for which the cookie is valid.</span></span> <span data-ttu-id="548b1-141">Se viene specificato un percorso, il cookie viene considerato valido per tutte le richieste corrispondenti a tale percorso.</span><span class="sxs-lookup"><span data-stu-id="548b1-141">If a path is specified, the cookie is considered valid for any requests that match that path.</span></span> <span data-ttu-id="548b1-142">Se, ad esempio, il percorso specificato è/example, le richieste con i percorsi/ExampleCode e/example/code.htm corrisponderanno.</span><span class="sxs-lookup"><span data-stu-id="548b1-142">For example, if the specified path is /example, requests with the paths /examplecode and /example/code.htm would match.</span></span> <span data-ttu-id="548b1-143">Se non viene specificato alcun percorso, si presuppone che il percorso corrisponda al percorso della risorsa associata all'intestazione Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="548b1-143">If no path is specified, the path is assumed to be the path of the resource associated with the Set-Cookie header.</span></span>

<span data-ttu-id="548b1-144">Il cookie può anche essere contrassegnato come protetto, che specifica che il cookie può essere inviato solo ai server HTTPS.</span><span class="sxs-lookup"><span data-stu-id="548b1-144">The cookie can also be marked as secure, which specifies that the cookie can be sent only to https servers.</span></span>

<span data-ttu-id="548b1-145">Infine, un cookie può essere contrassegnato come HttpOnly (gli attributi non fanno distinzione tra maiuscole e minuscole), per indicare che il cookie non è configurabile tramite script e non deve essere rivelato all'applicazione client, per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="548b1-145">Finally, a cookie can be marked as HttpOnly (attributes are not case-sensitive), to indicate that the cookie is non-scriptable and should not be revealed to the client application, for security reasons.</span></span> <span data-ttu-id="548b1-146">All'interno di Windows Internet, ciò significa che non è possibile recuperare il cookie tramite la funzione **InternetGetCookie** .</span><span class="sxs-lookup"><span data-stu-id="548b1-146">Within Windows Internet, this means that the cookie cannot be retrieved through the **InternetGetCookie** function.</span></span>

### <a name="cookie-header"></a><span data-ttu-id="548b1-147">Intestazione cookie</span><span class="sxs-lookup"><span data-stu-id="548b1-147">Cookie Header</span></span>

<span data-ttu-id="548b1-148">L'intestazione del cookie è inclusa in tutte le richieste HTTP con un cookie il cui dominio e percorso corrispondono alla richiesta.</span><span class="sxs-lookup"><span data-stu-id="548b1-148">The Cookie header is included with any HTTP requests that have a cookie whose domain and path match the request.</span></span> <span data-ttu-id="548b1-149">Il formato dell'intestazione del cookie è il seguente:</span><span class="sxs-lookup"><span data-stu-id="548b1-149">The Cookie header has the following format:</span></span>

``` syntax
Cookie: <name>=<value> [;<name>=<value>]...
```

<span data-ttu-id="548b1-150">Una o più sequenze di stringhe, usando il valore del *nome* formato = , contengono le informazioni impostate nel cookie.</span><span class="sxs-lookup"><span data-stu-id="548b1-150">One or more string sequences, using the format *name*=*value*, contain the information that was set in the cookie.</span></span>

## <a name="generating-cookies"></a><span data-ttu-id="548b1-151">Generazione di cookie</span><span class="sxs-lookup"><span data-stu-id="548b1-151">Generating Cookies</span></span>

<span data-ttu-id="548b1-152">Sono disponibili tre metodi per la generazione di cookie per Microsoft Internet Explorer: utilizzo di Microsoft JScript, utilizzo delle funzioni WinINet e utilizzo di uno script CGI.</span><span class="sxs-lookup"><span data-stu-id="548b1-152">There are three methods for generating cookies for Microsoft Internet Explorer: using Microsoft JScript, using the WinINet functions, and using a CGI script.</span></span> <span data-ttu-id="548b1-153">Tutti i metodi devono impostare le informazioni incluse nell'intestazione Set-Cookie.</span><span class="sxs-lookup"><span data-stu-id="548b1-153">All of the methods need to set the information that is included in the Set-Cookie header.</span></span>

### <a name="generating-a-cookie-using-the-dhtml-object-model"></a><span data-ttu-id="548b1-154">Generazione di un cookie con il modello a oggetti DHTML</span><span class="sxs-lookup"><span data-stu-id="548b1-154">Generating a Cookie Using the DHTML Object Model</span></span>

<span data-ttu-id="548b1-155">Usando il modello a oggetti DHTML (Dynamic HTML), i cookie possono essere impostati chiamando la proprietà **cookie** dell'oggetto Document, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="548b1-155">Using the Dynamic HTML (DHTML) object model, cookies can be set by calling the **cookie** property of the document object, as shown in the following example.</span></span>

``` syntax
<SCRIPT language="JavaScript">
<!--
    document.cookie = "SomeValueName = Some_Value";
-->
</SCRIPT>
```

### <a name="generating-a-cookie-using-the-wininet-functions"></a><span data-ttu-id="548b1-156">Generazione di un cookie mediante le funzioni WinInet</span><span class="sxs-lookup"><span data-stu-id="548b1-156">Generating a Cookie Using the WinInet Functions</span></span>

<span data-ttu-id="548b1-157">I cookie possono essere creati dalle applicazioni mediante la funzione [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) .</span><span class="sxs-lookup"><span data-stu-id="548b1-157">Cookies can be created by applications using the [**InternetSetCookie**](/windows/desktop/api/Wininet/nf-wininet-internetsetcookiea) function.</span></span> <span data-ttu-id="548b1-158">Per ulteriori informazioni, vedere [impostazione di un cookie](managing-cookies.md).</span><span class="sxs-lookup"><span data-stu-id="548b1-158">For more information, see [Setting a Cookie](managing-cookies.md).</span></span>

### <a name="generating-a-cookie-using-a-cgi-script"></a><span data-ttu-id="548b1-159">Generazione di un cookie mediante uno script CGI</span><span class="sxs-lookup"><span data-stu-id="548b1-159">Generating a Cookie Using a CGI Script</span></span>

<span data-ttu-id="548b1-160">I cookie vengono generati includendo un'intestazione Set-Cookie come parte di uno script CGI incluso nella risposta HTTP a una richiesta.</span><span class="sxs-lookup"><span data-stu-id="548b1-160">Cookies are generated by including a Set-Cookie header as part of a CGI script included in the HTTP response to a request.</span></span>

<span data-ttu-id="548b1-161">L'esempio seguente è uno script CGI che include un'intestazione Set-Cookie usando Perl.</span><span class="sxs-lookup"><span data-stu-id="548b1-161">The following example is a CGI script that includes a Set-Cookie header using Perl.</span></span>

``` syntax
print "Set-Cookie:Test=test_value; 
      expires=Sat, 01-Jan-2000 00:00:00 GMT;
      path=/;"
```

> [!Note]  
> <span data-ttu-id="548b1-162">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="548b1-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="548b1-163">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="548b1-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="548b1-164">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="548b1-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 