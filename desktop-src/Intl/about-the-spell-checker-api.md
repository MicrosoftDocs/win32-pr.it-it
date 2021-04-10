---
description: Per gli utenti in tutto il mondo, l'input testuale fa parte di un'esperienza di elaborazione moderna, per blogging, commenti, Tweet, messaggistica istantanea o qualsiasi altro tipo di testo. In Windows 8, il controllo ortografico è incorporato per modificare i controlli.
ms.assetid: ED569D4F-568B-4381-91C3-8EAEDA4DD47C
title: Informazioni sull'API controllo ortografico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d356823e665781052e2a2d5ea98b358155038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883018"
---
# <a name="about-the-spell-checking-api"></a><span data-ttu-id="2fc68-104">Informazioni sull'API controllo ortografico</span><span class="sxs-lookup"><span data-stu-id="2fc68-104">About the Spell Checking API</span></span>

<span data-ttu-id="2fc68-105">Per gli utenti in tutto il mondo, l'input testuale fa parte di un'esperienza di elaborazione moderna, per blogging, commenti, Tweet, messaggistica istantanea o qualsiasi altro tipo di testo.</span><span class="sxs-lookup"><span data-stu-id="2fc68-105">For users worldwide, textual input is part of a modern computing experience, for blogging, commenting, tweeting, instant messaging, or any other kind of text typing.</span></span> <span data-ttu-id="2fc68-106">In Windows 8, il controllo ortografico è incorporato per modificare i controlli.</span><span class="sxs-lookup"><span data-stu-id="2fc68-106">In Windows 8, spell checking is built-in to edit controls.</span></span>

<span data-ttu-id="2fc68-107">Gli sviluppatori possono usare l'API di controllo ortografico nelle app per utilizzare i servizi di controllo ortografico disponibili.</span><span class="sxs-lookup"><span data-stu-id="2fc68-107">Developers can use the spell checking API in their apps to consume available spell checking services.</span></span> <span data-ttu-id="2fc68-108">Gli sviluppatori possono inoltre creare i controllo ortografici che diventano provider e sono integrati nel Framework di controllo ortografico di Windows.</span><span class="sxs-lookup"><span data-stu-id="2fc68-108">Developers can also create spell checkers that become providers and are integrated into the Windows spell checking framework.</span></span>

<span data-ttu-id="2fc68-109">L'API di controllo ortografico è progettata per l'uso da parte degli sviluppatori C/C++ professionali delle app Windows Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="2fc68-109">The Spell Checking API is designed for use by professional C/C++ developers of Windows Component Object Model (COM) apps.</span></span> <span data-ttu-id="2fc68-110">L'API di controllo ortografico non è supportata per l'uso in un servizio Windows o ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="2fc68-110">The Spell Checking API is not supported for use in a Windows or ASP.NET service.</span></span>

## <a name="versioning"></a><span data-ttu-id="2fc68-111">Controllo delle versioni</span><span class="sxs-lookup"><span data-stu-id="2fc68-111">Versioning</span></span>

<span data-ttu-id="2fc68-112">L'API controllo ortografico è disponibile a partire da Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2fc68-112">The Spell Checking API is available beginning with the Windows 8 or Windows Server 2012.</span></span> <span data-ttu-id="2fc68-113">Le aggiunte future all'API verranno gestite creando nuove interfacce che possono essere determinate usando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su quelle esistenti.</span><span class="sxs-lookup"><span data-stu-id="2fc68-113">Future additions to the API will be handled by creating new interfaces that can be determined using [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the existing ones.</span></span>

## <a name="interfaces"></a><span data-ttu-id="2fc68-114">Interfacce</span><span class="sxs-lookup"><span data-stu-id="2fc68-114">Interfaces</span></span>

<span data-ttu-id="2fc68-115">Tutte le interfacce devono essere rilasciate quando non sono più utilizzate.</span><span class="sxs-lookup"><span data-stu-id="2fc68-115">All interfaces must be released when they are no longer used.</span></span> <span data-ttu-id="2fc68-116">Tutte le stringhe restituite (parametro out) **LPWSTR** (e gli elementi **LPOLESTR** da [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) devono essere rilasciate con [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) quando non vengono più usate.</span><span class="sxs-lookup"><span data-stu-id="2fc68-116">All returned (out parameter) **LPWSTR** strings (and **LPOLESTR** items from [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)) must be released with [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) when no longer used.</span></span>

## <a name="error-handling"></a><span data-ttu-id="2fc68-117">Gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="2fc68-117">Error handling</span></span>

<span data-ttu-id="2fc68-118">Gli errori vengono restituiti come **HRESULT** s.</span><span class="sxs-lookup"><span data-stu-id="2fc68-118">Errors are returned as **HRESULT** s.</span></span> <span data-ttu-id="2fc68-119">[**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) e [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) non sono supportati in questa API.</span><span class="sxs-lookup"><span data-stu-id="2fc68-119">[**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) and [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) are not supported in this API.</span></span> <span data-ttu-id="2fc68-120">Gli errori non sono particolarmente praticabili ad eccezione degli argomenti non corretti.</span><span class="sxs-lookup"><span data-stu-id="2fc68-120">Errors are not particularly actionable except for incorrect arguments.</span></span>

<span data-ttu-id="2fc68-121">I codici di errore RPC standard possono essere restituiti da qualsiasi chiamata API perché sono out-of-process.</span><span class="sxs-lookup"><span data-stu-id="2fc68-121">Standard RPC error codes may be returned by any of the API calls because they are out-of-proc.</span></span> <span data-ttu-id="2fc68-122">Si applicano i timeout standard RPC.</span><span class="sxs-lookup"><span data-stu-id="2fc68-122">Standard RPC timeouts apply.</span></span>

## <a name="security"></a><span data-ttu-id="2fc68-123">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="2fc68-123">Security</span></span>

<span data-ttu-id="2fc68-124">L'API di controllo ortografico può caricare codice esterno (provider di controllo ortografico).</span><span class="sxs-lookup"><span data-stu-id="2fc68-124">The Spell Checking API may load external code (spell check providers).</span></span> <span data-ttu-id="2fc68-125">Questo codice verrà eseguito out-of-process e in un contesto di sicurezza con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="2fc68-125">It will run this code out-of-proc and under a restricted security context.</span></span>

## <a name="dictionary-files"></a><span data-ttu-id="2fc68-126">File dizionario</span><span class="sxs-lookup"><span data-stu-id="2fc68-126">Dictionary files</span></span>

<span data-ttu-id="2fc68-127">I dizionari specifici dell'utente per una lingua che contiene il contenuto per gli elenchi di parole aggiunte, escluse e corrette si trovano in% AppData% \\ Microsoft \\ spelling \\ *<language tag>* .</span><span class="sxs-lookup"><span data-stu-id="2fc68-127">The user-specific dictionaries for a language, which hold the content for the Added, Excluded, and AutoCorrect word lists, are located under %AppData%\\Microsoft\\Spelling\\*<language tag>*.</span></span> <span data-ttu-id="2fc68-128">I nomi file sono default. dic (added), default. exc (escluso) e default. ACL (correzione automatica).</span><span class="sxs-lookup"><span data-stu-id="2fc68-128">The filenames are default.dic (Added), default.exc (Excluded) and default.acl (AutoCorrect).</span></span> <span data-ttu-id="2fc68-129">I file sono di testo non crittografato UTF-16 che deve iniziare con il BOM (Byte Order Mark) appropriato.</span><span class="sxs-lookup"><span data-stu-id="2fc68-129">The files are UTF-16 LE plaintext that must start with the appropriate Byte Order Mark (BOM).</span></span> <span data-ttu-id="2fc68-130">Ogni riga contiene una parola (negli elenchi di parole aggiunte ed escluse) o una coppia di correzione automatica con le parole separate da una barra verticale (" \| ") (nell'elenco di parole correzione automatica).</span><span class="sxs-lookup"><span data-stu-id="2fc68-130">Each line contains a word (in the Added and Excluded word lists), or an autocorrect pair with the words separated by a vertical bar ("\|") (in the AutoCorrect word list).</span></span> <span data-ttu-id="2fc68-131">Altri file. dic,. exc e. ACL presenti nella directory verranno rilevati dal servizio di controllo ortografico e aggiunti agli elenchi di parole utente.</span><span class="sxs-lookup"><span data-stu-id="2fc68-131">Other .dic, .exc, and .acl files present in the directory will be detected by the spell checking service and added to the user word lists.</span></span> <span data-ttu-id="2fc68-132">Questi file sono considerati di sola lettura e non vengono modificati dall'API di controllo ortografico.</span><span class="sxs-lookup"><span data-stu-id="2fc68-132">These files are considered to be read-only and are not modified by the spell checking API.</span></span>

## <a name="installing-a-spell-checking-provider"></a><span data-ttu-id="2fc68-133">Installazione di un provider di controllo ortografico</span><span class="sxs-lookup"><span data-stu-id="2fc68-133">Installing a spell checking provider</span></span>

<span data-ttu-id="2fc68-134">L'installazione di un provider di controllo ortografico deve inserire tutti i file usati in un percorso che consenta l'accesso in lettura dal SID ([ID di sicurezza](../secauthz/security-identifiers.md)) "tutti i pacchetti dell'applicazione".</span><span class="sxs-lookup"><span data-stu-id="2fc68-134">The installation of a spell checking provider must place all the files it uses in a location that allows read access from the SID ([security identifier](../secauthz/security-identifiers.md)) "ALL APPLICATION PACKAGES".</span></span> <span data-ttu-id="2fc68-135">L'installazione in una cartella in "programmi" funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="2fc68-135">Installing it in a folder under "Program Files" works well.</span></span> <span data-ttu-id="2fc68-136">Inoltre, il provider deve impostare alcune chiavi nel registro affinché venga visualizzato nell'API di controllo ortografico.</span><span class="sxs-lookup"><span data-stu-id="2fc68-136">Also, the provider must set some keys in the registry for it to appear to the spell checking API.</span></span> <span data-ttu-id="2fc68-137">Può trovarsi nell'hive dell' \_ utente corrente di HKEY \_ o nell' \_ hive del computer locale hKey, \_ a seconda che venga installato solo per l'utente corrente o per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="2fc68-137">It can be in either the HKEY\_CURRENT\_USER hive or the HKEY\_LOCAL\_MACHINE hive depending on whether it should install only for the current user or all users.</span></span>


```
Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>
     Default (REG_SZ) = <Name of the provider>

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\InprocServer32
     ThreadingModel (REG_SZ) = "Both"

Key: <Registry hive>\SOFTWARE\Classes\CLSID\<Server CLSID>\Version
     Version (REG_SZ) = <Version>

Key: <Registry hive>\SOFTWARE\Microsoft\Spelling\Spellers\<Provider id string>
     CLSID (REG_SZ) = <CLSID of the COM Server that implements the provider>
```



<span data-ttu-id="2fc68-138">L' [esempio del provider di controllo ortografico](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) fornisce un esempio della registrazione necessaria per installare un provider.</span><span class="sxs-lookup"><span data-stu-id="2fc68-138">The [spell checking provider sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider) provides an example of the registration needed to install a provider.</span></span>

<span data-ttu-id="2fc68-139">Se si creano nuove opzioni di controllo ortografico per un provider di controllo ortografico, vedere [**IOptionDescription:: ID**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) per informazioni aggiuntive sulla denominazione.</span><span class="sxs-lookup"><span data-stu-id="2fc68-139">If you are creating new spell checking options for a spell checking provider, see [**IOptionDescription::Id**](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id) for guidance on naming.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fc68-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2fc68-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fc68-141">Riferimento all'API controllo ortografico</span><span class="sxs-lookup"><span data-stu-id="2fc68-141">Spell Checking API Reference</span></span>](spell-checker-api-reference.md)
</dt> <dt>

[<span data-ttu-id="2fc68-142">Esempio di client di controllo ortografico</span><span class="sxs-lookup"><span data-stu-id="2fc68-142">Spell checking client sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerClient)
</dt> <dt>

[<span data-ttu-id="2fc68-143">Esempio di provider di controllo ortografico</span><span class="sxs-lookup"><span data-stu-id="2fc68-143">Spell checking provider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SpellCheckerProvider)
</dt> <dt>

[<span data-ttu-id="2fc68-144">**IOptionDescription:: ID**</span><span class="sxs-lookup"><span data-stu-id="2fc68-144">**IOptionDescription::Id**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ioptiondescription-get_id)
</dt> <dt>

[<span data-ttu-id="2fc68-145">**IEnumString**</span><span class="sxs-lookup"><span data-stu-id="2fc68-145">**IEnumString**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring)
</dt> <dt>

<span data-ttu-id="2fc68-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="2fc68-146">[**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> </dl>

 

 
