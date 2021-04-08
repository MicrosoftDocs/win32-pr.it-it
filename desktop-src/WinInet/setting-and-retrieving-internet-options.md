---
title: Impostazione e recupero delle opzioni Internet
description: In questo argomento viene descritto come impostare e recuperare le opzioni Internet utilizzando le funzioni InternetSetOption e InternetQueryOption.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Impostazione e recupero delle opzioni Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872830"
---
# <a name="setting-and-retrieving-internet-options"></a><span data-ttu-id="5c09f-104">Impostazione e recupero delle opzioni Internet</span><span class="sxs-lookup"><span data-stu-id="5c09f-104">Setting and Retrieving Internet Options</span></span>

<span data-ttu-id="5c09f-105">In questo argomento viene descritto come impostare e recuperare le opzioni Internet utilizzando le funzioni [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .</span><span class="sxs-lookup"><span data-stu-id="5c09f-105">This topic describes how to set and retrieve Internet options using the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) functions.</span></span>

<span data-ttu-id="5c09f-106">Le opzioni Internet possono essere impostate o recuperate da un handle [**HINTERNET**](appendix-a-hinternet-handles.md) specificato o dalle impostazioni correnti in Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5c09f-106">Internet options can be set on, or retrieved from, a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle or the current settings in Microsoft Internet Explorer.</span></span>

-   [<span data-ttu-id="5c09f-107">Passaggi di implementazione</span><span class="sxs-lookup"><span data-stu-id="5c09f-107">Implementation Steps</span></span>](#implementation-steps)
    -   [<span data-ttu-id="5c09f-108">Scelta delle opzioni Internet</span><span class="sxs-lookup"><span data-stu-id="5c09f-108">Choosing Internet Options</span></span>](#choosing-internet-options)
    -   [<span data-ttu-id="5c09f-109">Scelta dell'handle HINTERNET</span><span class="sxs-lookup"><span data-stu-id="5c09f-109">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
    -   [<span data-ttu-id="5c09f-110">Impostazione o recupero delle opzioni</span><span class="sxs-lookup"><span data-stu-id="5c09f-110">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)
-   [<span data-ttu-id="5c09f-111">Ambito dell'handle HINTERNET</span><span class="sxs-lookup"><span data-stu-id="5c09f-111">Scope of HINTERNET Handle</span></span>](#scope-of-hinternet-handle)
-   [<span data-ttu-id="5c09f-112">Impostazione delle singole opzioni</span><span class="sxs-lookup"><span data-stu-id="5c09f-112">Setting Individual Options</span></span>](#setting-individual-options)
-   [<span data-ttu-id="5c09f-113">Recupero di singole opzioni</span><span class="sxs-lookup"><span data-stu-id="5c09f-113">Retrieving Individual Options</span></span>](#retrieving-individual-options)
    -   [<span data-ttu-id="5c09f-114">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="5c09f-114">Complete Sample</span></span>](#complete-sample)
-   [<span data-ttu-id="5c09f-115">Impostazione delle opzioni di connessione</span><span class="sxs-lookup"><span data-stu-id="5c09f-115">Setting Connection Options</span></span>](#setting-connection-options)
-   [<span data-ttu-id="5c09f-116">Recupero delle opzioni di connessione</span><span class="sxs-lookup"><span data-stu-id="5c09f-116">Retrieving Connection Options</span></span>](#retrieving-connection-options)
-   [<span data-ttu-id="5c09f-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c09f-117">Related topics</span></span>](#related-topics)

## <a name="implementation-steps"></a><span data-ttu-id="5c09f-118">Passaggi di implementazione</span><span class="sxs-lookup"><span data-stu-id="5c09f-118">Implementation Steps</span></span>

<span data-ttu-id="5c09f-119">Per impostare o recuperare le opzioni Internet, completare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c09f-119">To set or retrieve Internet options complete the following:</span></span>

-   [<span data-ttu-id="5c09f-120">Scelta delle opzioni Internet</span><span class="sxs-lookup"><span data-stu-id="5c09f-120">Choosing Internet Options</span></span>](#choosing-internet-options)
-   [<span data-ttu-id="5c09f-121">Scelta dell'handle HINTERNET</span><span class="sxs-lookup"><span data-stu-id="5c09f-121">Choosing the HINTERNET Handle</span></span>](#choosing-the-hinternet-handle)
-   [<span data-ttu-id="5c09f-122">Impostazione o recupero delle opzioni</span><span class="sxs-lookup"><span data-stu-id="5c09f-122">Setting or Retrieving the Options</span></span>](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a><span data-ttu-id="5c09f-123">Scelta delle opzioni Internet</span><span class="sxs-lookup"><span data-stu-id="5c09f-123">Choosing Internet Options</span></span>

<span data-ttu-id="5c09f-124">Poiché sono disponibili numerose opzioni Internet, è importante scegliere le opzioni corrette.</span><span class="sxs-lookup"><span data-stu-id="5c09f-124">Because there are so many Internet options, choosing the right options is important.</span></span> <span data-ttu-id="5c09f-125">Molte opzioni Internet influiscono sul comportamento delle funzioni WinINet e di Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="5c09f-125">Many Internet options affect the behavior of the WinINet functions and Internet Explorer:</span></span>

<span data-ttu-id="5c09f-126">Ad esempio, è possibile:</span><span class="sxs-lookup"><span data-stu-id="5c09f-126">For example, you can:</span></span>

-   <span data-ttu-id="5c09f-127">Gestire l'autenticazione di base del server e del proxy impostando nomi utente e password.</span><span class="sxs-lookup"><span data-stu-id="5c09f-127">Handle basic server and proxy authentication by setting user names and passwords.</span></span>
-   <span data-ttu-id="5c09f-128">Impostare o recuperare la stringa agente utente utilizzata dai server per identificare le funzionalità dell'applicazione client o del browser.</span><span class="sxs-lookup"><span data-stu-id="5c09f-128">Set or retrieve the user agent string used by servers to identify the features of the client application or browser.</span></span>
-   <span data-ttu-id="5c09f-129">Recupera il tipo di handle dell'handle [**HINTERNET**](appendix-a-hinternet-handles.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="5c09f-129">Retrieve the handle type of the specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="5c09f-130">Per ulteriori informazioni e per un elenco delle opzioni Internet, vedere [**flag di opzione**](option-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5c09f-130">For more information and a list of the Internet options, see [**Option Flags**](option-flags.md).</span></span>

<span data-ttu-id="5c09f-131">In Internet Explorer 5 e versioni successive è possibile impostare o recuperare alcune opzioni da una connessione Internet specifica utilizzando [**Internet \_ per ogni \_ \_ \_ elenco**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) di opzioni Conn e le strutture di opzioni Internet [**\_ per \_ conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="5c09f-131">In Internet Explorer 5 and later, some options can be set or retrieved from a specific Internet connection using the [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) and [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span> <span data-ttu-id="5c09f-132">Per ulteriori informazioni e un elenco di opzioni che è possibile impostare o recuperare da una connessione Internet specifica, vedere il membro **dwOptions** della struttura di [**Internet \_ per ogni \_ \_ opzione conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="5c09f-132">For more information and a list of options that can be set or retrieved from a specific Internet connection, see the **dwOptions** member of the [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structure.</span></span>

### <a name="choosing-the-hinternet-handle"></a><span data-ttu-id="5c09f-133">Scelta dell'handle HINTERNET</span><span class="sxs-lookup"><span data-stu-id="5c09f-133">Choosing the HINTERNET Handle</span></span>

<span data-ttu-id="5c09f-134">L'handle [**HINTERNET**](appendix-a-hinternet-handles.md) usato per impostare o recuperare le opzioni Internet determina l'ambito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5c09f-134">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the scope of the operation.</span></span> <span data-ttu-id="5c09f-135">Tutti gli handle creati tramite questo handle erediteranno le opzioni impostate in questo handle.</span><span class="sxs-lookup"><span data-stu-id="5c09f-135">All the handles created through this handle will inherit the options set on this handle.</span></span>

<span data-ttu-id="5c09f-136">Ad esempio, le applicazioni client che richiedono un proxy con autenticazione, probabilmente non richiedono l'impostazione del nome utente e della password del proxy ogni volta che l'applicazione tenta di accedere a una risorsa Internet.</span><span class="sxs-lookup"><span data-stu-id="5c09f-136">For example, client applications that require a proxy with authentication, probably do not require setting the proxy user name and password every time the application attempts to access an Internet resource.</span></span> <span data-ttu-id="5c09f-137">Se tutte le richieste su una determinata connessione vengono gestite dallo stesso proxy, l'impostazione del nome utente e della password del proxy in un tipo di connessione [**HINTERNET**](appendix-a-hinternet-handles.md) handle, ovvero un handle creato da una chiamata a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), consentirebbe a qualsiasi chiamata derivata da questo handle **HINTERNET** di utilizzare lo stesso nome utente e la stessa password del proxy.</span><span class="sxs-lookup"><span data-stu-id="5c09f-137">If all requests on a given connection are handled by the same proxy, setting the proxy user name and password on a connection type [**HINTERNET**](appendix-a-hinternet-handles.md) handle, that is, a handle created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), would allow any calls derived from this **HINTERNET** handle to use the same proxy user name and password.</span></span> <span data-ttu-id="5c09f-138">L'impostazione del nome utente e della password del proxy ogni volta che un handle **HINTERNET** viene creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) richiederebbe un sovraccarico aggiuntivo e non necessario.</span><span class="sxs-lookup"><span data-stu-id="5c09f-138">Setting the proxy user name and password every time an **HINTERNET** handle is created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) would require extra and unnecessary overhead.</span></span> <span data-ttu-id="5c09f-139">Tenere presente che se l'applicazione utilizza un proxy che richiede l'autenticazione, è necessario impostare le credenziali del proxy per ogni nuova connessione.</span><span class="sxs-lookup"><span data-stu-id="5c09f-139">Be aware that if the application uses a proxy that requires authentication, it should set the proxy credentials on every new connection.</span></span>

### <a name="setting-or-retrieving-the-options"></a><span data-ttu-id="5c09f-140">Impostazione o recupero delle opzioni</span><span class="sxs-lookup"><span data-stu-id="5c09f-140">Setting or Retrieving the Options</span></span>

<span data-ttu-id="5c09f-141">Quando sono state determinate le opzioni Internet e l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) da usare, recuperare le opzioni Internet.</span><span class="sxs-lookup"><span data-stu-id="5c09f-141">When you have determined what Internet options and [**HINTERNET**](appendix-a-hinternet-handles.md) handle to use, retrieve those Internet options.</span></span> <span data-ttu-id="5c09f-142">Per impostare o recuperare le opzioni, chiamare [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="5c09f-142">To set or retrieve options, call either [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

## <a name="scope-of-hinternet-handle"></a><span data-ttu-id="5c09f-143">Ambito dell'handle HINTERNET</span><span class="sxs-lookup"><span data-stu-id="5c09f-143">Scope of HINTERNET Handle</span></span>

<span data-ttu-id="5c09f-144">L'handle [**HINTERNET**](appendix-a-hinternet-handles.md) usato per impostare o recuperare le opzioni Internet determina le azioni per le quali sono valide le opzioni.</span><span class="sxs-lookup"><span data-stu-id="5c09f-144">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle used to set or retrieve Internet options determines the actions for which the options are valid.</span></span>

<span data-ttu-id="5c09f-145">Questi handle hanno tre livelli:</span><span class="sxs-lookup"><span data-stu-id="5c09f-145">These handles have three levels:</span></span>

-   <span data-ttu-id="5c09f-146">L'handle [**HINTERNET**](appendix-a-hinternet-handles.md) radice (creato da una chiamata a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) conterrà tutte le opzioni Internet che interessano questa istanza di WinInet.</span><span class="sxs-lookup"><span data-stu-id="5c09f-146">The root [**HINTERNET**](appendix-a-hinternet-handles.md) handle (created by a call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) would contain all the Internet options that affect this instance of WinINet.</span></span>
-   <span data-ttu-id="5c09f-147">Handle [**HINTERNET**](appendix-a-hinternet-handles.md) che si connettono a un server (creato da una chiamata a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))</span><span class="sxs-lookup"><span data-stu-id="5c09f-147">[**HINTERNET**](appendix-a-hinternet-handles.md) handles that connect to a server (created by a call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))</span></span>
-   <span data-ttu-id="5c09f-148">Handle [**HINTERNET**](appendix-a-hinternet-handles.md) associati a una risorsa o a un'enumerazione di risorse in un determinato server.</span><span class="sxs-lookup"><span data-stu-id="5c09f-148">[**HINTERNET**](appendix-a-hinternet-handles.md) handles associated with a resource or enumeration of resources on a particular server.</span></span>

<span data-ttu-id="5c09f-149">Oltre ai vari handle [**HINTERNET**](appendix-a-hinternet-handles.md) , un'applicazione può utilizzare anche **null** per impostare o recuperare i valori predefiniti delle opzioni Internet utilizzate da Internet Explorer e dalle funzioni WinInet.</span><span class="sxs-lookup"><span data-stu-id="5c09f-149">In addition to the various [**HINTERNET**](appendix-a-hinternet-handles.md) handles, an application can also use **NULL** to set or retrieve the default values of the Internet options used by Internet Explorer and the WinINet functions.</span></span> <span data-ttu-id="5c09f-150">Impostazione delle opzioni Internet quando si usa **null** come handle per modificare i valori predefiniti delle opzioni, attualmente archiviate nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5c09f-150">Setting Internet options when using **NULL** as the handle changes the default values of the options, which are currently stored in the registry.</span></span> <span data-ttu-id="5c09f-151">Le applicazioni client non devono utilizzare le funzioni del registro di sistema per modificare i valori predefiniti delle opzioni Internet, perché l'implementazione della modalità di archiviazione delle opzioni può essere modificata in futuro.</span><span class="sxs-lookup"><span data-stu-id="5c09f-151">Client applications should not use registry functions to change the default values of the Internet options, because the implementation of how the options are stored can be altered in the future.</span></span>

<span data-ttu-id="5c09f-152">La tabella seguente elenca il tipo di handle [**HINTERNET**](appendix-a-hinternet-handles.md) e l'ambito delle opzioni Internet associate.</span><span class="sxs-lookup"><span data-stu-id="5c09f-152">The following table lists the type of [**HINTERNET**](appendix-a-hinternet-handles.md) handles and the scope of the Internet options associated with them.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c09f-153">Tipo di handle</span><span class="sxs-lookup"><span data-stu-id="5c09f-153">Handle Type</span></span></th>
<th><span data-ttu-id="5c09f-154">Ambito</span><span class="sxs-lookup"><span data-stu-id="5c09f-154">Scope</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c09f-155"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="5c09f-155"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="5c09f-156">Impostazioni predefinite delle opzioni per Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5c09f-156">The default option settings for Internet Explorer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c09f-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span><span class="sxs-lookup"><span data-stu-id="5c09f-157">INTERNET_HANDLE_TYPE_CONNECT_FTP</span></span></td>
<td><span data-ttu-id="5c09f-158">Impostazioni delle opzioni per la connessione a un server FTP.</span><span class="sxs-lookup"><span data-stu-id="5c09f-158">The option settings for this connection to an FTP server.</span></span> <span data-ttu-id="5c09f-159">Queste opzioni influiscono su qualsiasi operazione avviata da questo handle <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , ad esempio download di file.</span><span class="sxs-lookup"><span data-stu-id="5c09f-159">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c09f-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span><span class="sxs-lookup"><span data-stu-id="5c09f-160">INTERNET_HANDLE_TYPE_CONNECT_GOPHER</span></span></td>
<td><span data-ttu-id="5c09f-161">Impostazioni delle opzioni per la connessione a un server gopher.</span><span class="sxs-lookup"><span data-stu-id="5c09f-161">The option settings for this connection to a Gopher server.</span></span> <span data-ttu-id="5c09f-162">Queste opzioni influiscono su qualsiasi operazione avviata da questo handle <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , ad esempio download di file.</span><span class="sxs-lookup"><span data-stu-id="5c09f-162">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5c09f-163">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="5c09f-163">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c09f-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span><span class="sxs-lookup"><span data-stu-id="5c09f-164">INTERNET_HANDLE_TYPE_CONNECT_HTTP</span></span></td>
<td><span data-ttu-id="5c09f-165">Impostazioni delle opzioni per la connessione a un server HTTP.</span><span class="sxs-lookup"><span data-stu-id="5c09f-165">The option settings for this connection to an HTTP server.</span></span> <span data-ttu-id="5c09f-166">Queste opzioni influiscono su qualsiasi operazione avviata da questo handle <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , ad esempio download di file.</span><span class="sxs-lookup"><span data-stu-id="5c09f-166">These options affect any operations initiated from this <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> handle, such as file downloads.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c09f-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span><span class="sxs-lookup"><span data-stu-id="5c09f-167">INTERNET_HANDLE_TYPE_FILE_REQUEST</span></span></td>
<td><span data-ttu-id="5c09f-168">Impostazioni delle opzioni associate alla richiesta di file.</span><span class="sxs-lookup"><span data-stu-id="5c09f-168">The option settings associated with this file request.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c09f-169">INTERNET_HANDLE_TYPE_FTP_FILE</span><span class="sxs-lookup"><span data-stu-id="5c09f-169">INTERNET_HANDLE_TYPE_FTP_FILE</span></span></td>
<td><span data-ttu-id="5c09f-170">Impostazioni delle opzioni associate a questo download di risorsa FTP.</span><span class="sxs-lookup"><span data-stu-id="5c09f-170">The option settings associated with this FTP resource download.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c09f-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="5c09f-171">INTERNET_HANDLE_TYPE_FTP_FILE_HTML</span></span></td>
<td><span data-ttu-id="5c09f-172">Impostazioni delle opzioni associate a questo download di risorsa FTP formattato in HTML.</span><span class="sxs-lookup"><span data-stu-id="5c09f-172">The option settings associated with this FTP resource download formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c09f-173">INTERNET_HANDLE_TYPE_FTP_FIND</span><span class="sxs-lookup"><span data-stu-id="5c09f-173">INTERNET_HANDLE_TYPE_FTP_FIND</span></span></td>
<td><span data-ttu-id="5c09f-174">Impostazioni delle opzioni associate a questa ricerca di file in un server FTP.</span><span class="sxs-lookup"><span data-stu-id="5c09f-174">The option settings associated with this search of files on an FTP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c09f-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="5c09f-175">INTERNET_HANDLE_TYPE_FTP_FIND_HTML</span></span></td>
<td><span data-ttu-id="5c09f-176">Impostazioni delle opzioni associate a questa ricerca di file in un server FTP formattato in HTML.</span><span class="sxs-lookup"><span data-stu-id="5c09f-176">The option settings associated with this search of files on an FTP server formatted in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c09f-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span><span class="sxs-lookup"><span data-stu-id="5c09f-177">INTERNET_HANDLE_TYPE_GOPHER_FILE</span></span></td>
<td><span data-ttu-id="5c09f-178">Impostazioni delle opzioni associate a questo download di risorsa gopher.</span><span class="sxs-lookup"><span data-stu-id="5c09f-178">The option settings associated with this Gopher resource download.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5c09f-179">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="5c09f-179">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c09f-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span><span class="sxs-lookup"><span data-stu-id="5c09f-180">INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</span></span></td>
<td><span data-ttu-id="5c09f-181">Le impostazioni delle opzioni associate a questo download di risorsa Gopher sono state formattate in HTML.</span><span class="sxs-lookup"><span data-stu-id="5c09f-181">The option settings associated with this Gopher resource download formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5c09f-182">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="5c09f-182">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c09f-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span><span class="sxs-lookup"><span data-stu-id="5c09f-183">INTERNET_HANDLE_TYPE_GOPHER_FIND</span></span></td>
<td><span data-ttu-id="5c09f-184">Impostazioni delle opzioni associate a questa ricerca di file in un server gopher.</span><span class="sxs-lookup"><span data-stu-id="5c09f-184">The option settings associated with this search of files on an Gopher server.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5c09f-185">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="5c09f-185">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c09f-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span><span class="sxs-lookup"><span data-stu-id="5c09f-186">INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</span></span></td>
<td><span data-ttu-id="5c09f-187">Impostazioni delle opzioni associate a questa ricerca di file in un server gopher formattato in HTML.</span><span class="sxs-lookup"><span data-stu-id="5c09f-187">The option settings associated with this search of files on an Gopher server formatted in HTML.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5c09f-188">Windows XP e Windows Server 2003 R2 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="5c09f-188">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c09f-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span><span class="sxs-lookup"><span data-stu-id="5c09f-189">INTERNET_HANDLE_TYPE_HTTP_REQUEST</span></span></td>
<td><span data-ttu-id="5c09f-190">Impostazioni delle opzioni associate a questa richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="5c09f-190">The option settings associated with this HTTP request.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c09f-191">INTERNET_HANDLE_TYPE_INTERNET</span><span class="sxs-lookup"><span data-stu-id="5c09f-191">INTERNET_HANDLE_TYPE_INTERNET</span></span></td>
<td><span data-ttu-id="5c09f-192">Impostazioni delle opzioni associate a questa istanza delle funzioni WinINet.</span><span class="sxs-lookup"><span data-stu-id="5c09f-192">The option settings associated with this instance of the WinINet functions.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a><span data-ttu-id="5c09f-193">Impostazione delle singole opzioni</span><span class="sxs-lookup"><span data-stu-id="5c09f-193">Setting Individual Options</span></span>

<span data-ttu-id="5c09f-194">Dopo aver determinato le opzioni Internet che si desidera impostare e l'ambito interessato da queste opzioni, l'impostazione delle opzioni Internet non è complessa.</span><span class="sxs-lookup"><span data-stu-id="5c09f-194">After determining the Internet options you want to set and the scope you want affected by these options, setting Internet options is not complicated.</span></span> <span data-ttu-id="5c09f-195">È sufficiente chiamare la funzione [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) desiderato, il flag di opzione Internet e un buffer che contiene le informazioni che si desidera impostare.</span><span class="sxs-lookup"><span data-stu-id="5c09f-195">All you would need to do is call the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function with desired [**HINTERNET**](appendix-a-hinternet-handles.md) handle, Internet option flag, and a buffer that contains the information you want set.</span></span>

<span data-ttu-id="5c09f-196">Nell'esempio seguente viene illustrato come impostare il nome utente e la password del proxy in un handle [**HINTERNET**](appendix-a-hinternet-handles.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="5c09f-196">The following example shows how to set the proxy user name and password on a specified [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a><span data-ttu-id="5c09f-197">Recupero di singole opzioni</span><span class="sxs-lookup"><span data-stu-id="5c09f-197">Retrieving Individual Options</span></span>

<span data-ttu-id="5c09f-198">È possibile recuperare le opzioni Internet utilizzando la funzione [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .</span><span class="sxs-lookup"><span data-stu-id="5c09f-198">Internet options can be retrieved using the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) function.</span></span> <span data-ttu-id="5c09f-199">Per recuperare le opzioni Internet:</span><span class="sxs-lookup"><span data-stu-id="5c09f-199">To retrieve Internet options:</span></span>

1.  <span data-ttu-id="5c09f-200">Determinare le dimensioni del buffer necessarie per recuperare le informazioni sull'opzione Internet.</span><span class="sxs-lookup"><span data-stu-id="5c09f-200">Determine the buffer size necessary to retrieve the Internet option information.</span></span>

    <span data-ttu-id="5c09f-201">È possibile determinare le dimensioni del buffer usando **null** per l'indirizzo del buffer e passandogli una dimensione del buffer pari a zero.</span><span class="sxs-lookup"><span data-stu-id="5c09f-201">The buffer size can be determined by using **NULL** for the address of the buffer and passing it a buffer size of zero.</span></span>

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    <span data-ttu-id="5c09f-202">Il valore restituito da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) è la quantità di memoria necessaria per recuperare le informazioni, in byte.</span><span class="sxs-lookup"><span data-stu-id="5c09f-202">The value returned by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) is the amount of memory required to retrieve the information, in bytes.</span></span>

2.  <span data-ttu-id="5c09f-203">Allocare una memoria per il buffer.</span><span class="sxs-lookup"><span data-stu-id="5c09f-203">Allocate a memory for the buffer.</span></span>
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  <span data-ttu-id="5c09f-204">Recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="5c09f-204">Retrieve the data.</span></span>
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  <span data-ttu-id="5c09f-205">Liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="5c09f-205">Free the memory.</span></span>
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a><span data-ttu-id="5c09f-206">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="5c09f-206">Complete Sample</span></span>

<span data-ttu-id="5c09f-207">Di seguito è riportato l'esempio completo usato nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="5c09f-207">The following is the complete sample used in the previous section.</span></span> <span data-ttu-id="5c09f-208">In questo esempio viene illustrato come recuperare la stringa agente utente predefinita.</span><span class="sxs-lookup"><span data-stu-id="5c09f-208">This sample shows how to retrieve the default user agent string.</span></span>


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a><span data-ttu-id="5c09f-209">Impostazione delle opzioni di connessione</span><span class="sxs-lookup"><span data-stu-id="5c09f-209">Setting Connection Options</span></span>

<span data-ttu-id="5c09f-210">In Internet Explorer 5 e versioni successive, è possibile impostare le opzioni Internet per una connessione specifica.</span><span class="sxs-lookup"><span data-stu-id="5c09f-210">In Internet Explorer 5 and later, Internet options can be set for on a specific connection.</span></span> <span data-ttu-id="5c09f-211">In precedenza, tutte le connessioni condividevano le stesse impostazioni delle opzioni Internet.</span><span class="sxs-lookup"><span data-stu-id="5c09f-211">Previously, all connections shared the same Internet option settings.</span></span> <span data-ttu-id="5c09f-212">Per impostare le opzioni per una connessione specifica:</span><span class="sxs-lookup"><span data-stu-id="5c09f-212">To set options for a particular connection:</span></span>

1.  <span data-ttu-id="5c09f-213">Creare una struttura [**Internet \_ per ogni \_ \_ \_ elenco di opzioni conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .</span><span class="sxs-lookup"><span data-stu-id="5c09f-213">Create an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="5c09f-214">Allocare la memoria per le singole opzioni Internet che si desidera impostare per la connessione.</span><span class="sxs-lookup"><span data-stu-id="5c09f-214">Allocate the memory for the individual Internet options that you want to set for the connection.</span></span>
3.  <span data-ttu-id="5c09f-215">Impostare le opzioni in [**Internet \_ per \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) le strutture delle opzioni conn.</span><span class="sxs-lookup"><span data-stu-id="5c09f-215">Set the options in [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="5c09f-216">Impostare le opzioni usando [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="5c09f-216">Set the options using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="5c09f-217">Nell'esempio di codice seguente viene illustrato come impostare i dati proxy per una connessione LAN.</span><span class="sxs-lookup"><span data-stu-id="5c09f-217">The following code example shows how to set proxy data for a LAN connection.</span></span>


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a><span data-ttu-id="5c09f-218">Recupero delle opzioni di connessione</span><span class="sxs-lookup"><span data-stu-id="5c09f-218">Retrieving Connection Options</span></span>

<span data-ttu-id="5c09f-219">In Internet Explorer 5 e versioni successive è possibile recuperare le opzioni Internet da una connessione specifica.</span><span class="sxs-lookup"><span data-stu-id="5c09f-219">In Internet Explorer 5 and later, Internet options can be retrieved from a specific connection.</span></span> <span data-ttu-id="5c09f-220">Per recuperare le opzioni da una particolare connessione:</span><span class="sxs-lookup"><span data-stu-id="5c09f-220">To retrieve options from a particular connection:</span></span>

1.  <span data-ttu-id="5c09f-221">Creare una struttura [**Internet \_ per ogni \_ \_ \_ elenco di opzioni conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .</span><span class="sxs-lookup"><span data-stu-id="5c09f-221">Create a [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure.</span></span>
2.  <span data-ttu-id="5c09f-222">Allocare la memoria per le singole opzioni Internet da recuperare dalla connessione.</span><span class="sxs-lookup"><span data-stu-id="5c09f-222">Allocate the memory for the individual Internet options to retrieve from the connection.</span></span>
3.  <span data-ttu-id="5c09f-223">Specificare le opzioni tramite [**Internet per le strutture di \_ \_ \_ Opzioni conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .</span><span class="sxs-lookup"><span data-stu-id="5c09f-223">Specify the options using [**INTERNET\_PER\_CONN\_OPTION**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) structures.</span></span>
4.  <span data-ttu-id="5c09f-224">Recuperare le opzioni usando [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="5c09f-224">Retrieve the options using [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>
5.  <span data-ttu-id="5c09f-225">Usare i dati di opzione.</span><span class="sxs-lookup"><span data-stu-id="5c09f-225">Utilize the option data.</span></span>
6.  <span data-ttu-id="5c09f-226">Liberare la memoria, allocata per conservare i dati delle opzioni, usando la funzione [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="5c09f-226">Free the memory, allocated to hold the option data, using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="5c09f-227">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="5c09f-227">WinINet does not support server implementations.</span></span> <span data-ttu-id="5c09f-228">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="5c09f-228">In addition, it should not be used from a service.</span></span> <span data-ttu-id="5c09f-229">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="5c09f-229">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5c09f-230">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c09f-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c09f-231">Gestione dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="5c09f-231">Handling Authentication</span></span>](handling-authentication.md)
</dt> <dt>

[<span data-ttu-id="5c09f-232">Handle HINTERNET</span><span class="sxs-lookup"><span data-stu-id="5c09f-232">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
</dt> </dl>

 

