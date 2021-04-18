---
title: Chiavi e voci del registro di sistema per un archivio online di tipo 1
description: Chiavi e voci del registro di sistema per un archivio online di tipo 1
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Windows Media Player Online Stores, registro di sistema
- archivi online, registro di sistema
- digitare 1 archivi online, registro di sistema
- Registro di sistema, digitare 1 negozio online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299423"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a><span data-ttu-id="4f178-107">Chiavi e voci del registro di sistema per un archivio online di tipo 1</span><span class="sxs-lookup"><span data-stu-id="4f178-107">Registry Keys and Entries for a Type 1 Online Store</span></span>

<span data-ttu-id="4f178-108">Per rendere disponibile un archivio online di tipo 1 in Windows Media Player, il provider di archivio online deve creare le sottochiavi e le voci del registro di sistema seguenti nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4f178-108">To make a type 1 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> <span data-ttu-id="4f178-109">L'impostazione del valore di DllSurrogate sulla stringa vuota indica che il runtime COM caricherà il plug-in del negozio online nel surrogato predefinito della DLL, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="4f178-109">Setting the value of DllSurrogate to the empty string indicates that the COM runtime will load the online store's plug-in into the default DLL surrogate, dllhost.exe.</span></span>

 

<span data-ttu-id="4f178-110">Nella sintassi del registro di sistema precedente, i simboli in corsivo sono segnaposto per i nomi e identificatori univoci globali (GUID) specifici per l'archivio online.</span><span class="sxs-lookup"><span data-stu-id="4f178-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="4f178-111">Nella tabella seguente vengono descritti i segnaposto.</span><span class="sxs-lookup"><span data-stu-id="4f178-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="4f178-112">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="4f178-112">Placeholder</span></span>    | <span data-ttu-id="4f178-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f178-113">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f178-114">*keyName*</span><span class="sxs-lookup"><span data-stu-id="4f178-114">*keyName*</span></span>      | <span data-ttu-id="4f178-115">Stringa concordata tra Microsoft e il negozio online.</span><span class="sxs-lookup"><span data-stu-id="4f178-115">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="4f178-116">Questa stringa identifica in modo univoco l'archivio online. Esempio: "Proseware"</span><span class="sxs-lookup"><span data-stu-id="4f178-116">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="4f178-117">*flags*</span><span class="sxs-lookup"><span data-stu-id="4f178-117">*flags*</span></span>        | <span data-ttu-id="4f178-118">Un operatore OR bit per bit di uno o più plug-in **flag di funzionalità** questi flag specificano se Windows Media Player deve chiamare metodi specifici di [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner).</span><span class="sxs-lookup"><span data-stu-id="4f178-118">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner).</span></span> <span data-ttu-id="4f178-119">Per informazioni sui flag supportati, vedere la tabella dei flag di funzionalità plug-in che seguono questa tabella. Esempio: 00000058</span><span class="sxs-lookup"><span data-stu-id="4f178-119">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000058</span></span><br/> |
| <span data-ttu-id="4f178-120">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="4f178-120">*clsid*</span></span>        | <span data-ttu-id="4f178-121">GUID che rappresenta l'identificatore di classe (CLSID) per la classe che implementa **IWMPContentPartner** nel plug-in del negozio online.</span><span class="sxs-lookup"><span data-stu-id="4f178-121">A GUID that is the class identifier (CLSID) for the class that implements **IWMPContentPartner** in the online store's plug-in.</span></span> <span data-ttu-id="4f178-122">Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="4f178-122">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                  |
| <span data-ttu-id="4f178-123">*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="4f178-123">*friendlyname*</span></span> | <span data-ttu-id="4f178-124">Nome descrittivo per il negozio online. Esempio: "Proseware Music Service"</span><span class="sxs-lookup"><span data-stu-id="4f178-124">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="4f178-125">*appid*</span><span class="sxs-lookup"><span data-stu-id="4f178-125">*appid*</span></span>        | <span data-ttu-id="4f178-126">GUID che rappresenta l'ID applicazione (AppID) per il plug-in del negozio online.</span><span class="sxs-lookup"><span data-stu-id="4f178-126">A GUID that is the application identifier (AppID) for the online store's plug-in.</span></span> <span data-ttu-id="4f178-127">Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="4f178-127">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                |
| <span data-ttu-id="4f178-128">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="4f178-128">*pluginName*</span></span>   | <span data-ttu-id="4f178-129">Nome del plug-in del negozio online. Esempio: "plug-in di Proseware content partner"</span><span class="sxs-lookup"><span data-stu-id="4f178-129">A name for the online store's plug-in.Example: "Proseware Content Partner Plug-in"</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="4f178-130">*className*</span><span class="sxs-lookup"><span data-stu-id="4f178-130">*className*</span></span>    | <span data-ttu-id="4f178-131">Nome della classe che implementa **IWMPContentpartner** nel plug-in del negozio online. Esempio: "CProsewarePartner"</span><span class="sxs-lookup"><span data-stu-id="4f178-131">The name of the class that implements **IWMPContentpartner** in the online store's plug-in.Example: "CProsewarePartner"</span></span><br/>                                                                                                                                                                                              |
| <span data-ttu-id="4f178-132">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="4f178-132">*moduleName*</span></span>   | <span data-ttu-id="4f178-133">Percorso completo della DLL che implementa il plug-in del negozio online. Esempio: "C: \\ Program Files \\ Proseware \\ProsewarePartner.dll"</span><span class="sxs-lookup"><span data-stu-id="4f178-133">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewarePartner.dll"</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="4f178-134">*Threading*</span><span class="sxs-lookup"><span data-stu-id="4f178-134">*threading*</span></span>    | <span data-ttu-id="4f178-135">Tipo di Apartment in cui viene eseguito il plug-in.</span><span class="sxs-lookup"><span data-stu-id="4f178-135">The type of apartment the plug-in runs in.</span></span> <span data-ttu-id="4f178-136">"ThreadingModel" = "Apartment" indica che il plug-in viene eseguito in un Apartment a thread singolo (STA).</span><span class="sxs-lookup"><span data-stu-id="4f178-136">"ThreadingModel"="Apartment" indicates that the plug-in runs in a single-threaded apartment (STA).</span></span> <span data-ttu-id="4f178-137">"ThreadingModel" = "Free" indica che il plug-in viene eseguito nell'Apartment a thread multipli (MTA).</span><span class="sxs-lookup"><span data-stu-id="4f178-137">"ThreadingModel"="Free" indicates that the plug-in runs in the multithreaded apartment (MTA).</span></span>                                                                                     |



 

<span data-ttu-id="4f178-138">Nella tabella seguente vengono descritti i flag di funzionalità plug-in.</span><span class="sxs-lookup"><span data-stu-id="4f178-138">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="4f178-139">Flag</span><span class="sxs-lookup"><span data-stu-id="4f178-139">Flag</span></span>                                    | <span data-ttu-id="4f178-140">valore</span><span class="sxs-lookup"><span data-stu-id="4f178-140">Value</span></span> | <span data-ttu-id="4f178-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f178-141">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f178-142">\_BACKGROUNDPROCESSING Cap \_ sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="4f178-142">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="4f178-143">0x8</span><span class="sxs-lookup"><span data-stu-id="4f178-143">0x8</span></span>   | <span data-ttu-id="4f178-144">Windows Media Player deve chiamare [IWMPContentPartner:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) per informare il plug-in quando deve avviare e arrestare l'elaborazione in background.</span><span class="sxs-lookup"><span data-stu-id="4f178-144">Windows Media Player should call [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) to inform the plug-in when it should start and stop background processing.</span></span>                                                                                                     |
| <span data-ttu-id="4f178-145">\_DEVICEAVAILABLE Cap \_ sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="4f178-145">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="4f178-146">0x10</span><span class="sxs-lookup"><span data-stu-id="4f178-146">0x10</span></span>  | <span data-ttu-id="4f178-147">Windows Media Player deve chiamare [IWMPContentPartner:: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).</span><span class="sxs-lookup"><span data-stu-id="4f178-147">Windows Media Player should call [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).</span></span>                                                                                                                                                                   |
| <span data-ttu-id="4f178-148">il \_ limite della sottoscrizione \_ è \_ CONTENTPARTNER</span><span class="sxs-lookup"><span data-stu-id="4f178-148">SUBSCRIPTION\_CAP\_IS\_CONTENTPARTNER</span></span>   | <span data-ttu-id="4f178-149">0x40</span><span class="sxs-lookup"><span data-stu-id="4f178-149">0x40</span></span>  | <span data-ttu-id="4f178-150">Informa Windows Media Player che il plug-in implementa l'interfaccia **IWMPContentPartner** .</span><span class="sxs-lookup"><span data-stu-id="4f178-150">Informs Windows Media Player that the plug-in implements the **IWMPContentPartner** interface.</span></span> <span data-ttu-id="4f178-151">Tutti i plug-in di archiviazione di tipo 1 devono impostare questo flag.</span><span class="sxs-lookup"><span data-stu-id="4f178-151">All type 1 online store plug-ins must set this flag.</span></span>                                                                                                                         |
| <span data-ttu-id="4f178-152">\_ALTLOGIN Cap \_ sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="4f178-152">SUBSCRIPTION\_CAP\_ALTLOGIN</span></span>             | <span data-ttu-id="4f178-153">0x80</span><span class="sxs-lookup"><span data-stu-id="4f178-153">0x80</span></span>  | <span data-ttu-id="4f178-154">Informa Windows Media Player che il plug-in supporta un account di accesso alternativo.</span><span class="sxs-lookup"><span data-stu-id="4f178-154">Informs Windows Media Player that the plug-in supports an alternate login.</span></span> <span data-ttu-id="4f178-155">Se il plug-in supporta un account di accesso alternativo, Windows Media Player recupera l'URL e la didascalia di accesso alternativi chiamando [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo).</span><span class="sxs-lookup"><span data-stu-id="4f178-155">If the plug-in supports an alternate login, Windows Media Player retrieves the alternate login URL and caption by calling [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo).</span></span> |



 

<span data-ttu-id="4f178-156">**Voci del registro di sistema per sviluppo e test**</span><span class="sxs-lookup"><span data-stu-id="4f178-156">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="4f178-157">Quando si inizia a sviluppare lo Store online, Microsoft fornisce due chiavi: una chiave di test e una chiave di produzione.</span><span class="sxs-lookup"><span data-stu-id="4f178-157">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="4f178-158">Durante la fase di sviluppo e test, il negozio online verrà visualizzato in Windows Media Player solo se la chiave di test o la chiave di produzione si trova nel registro di sistema nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4f178-158">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="4f178-159">Per ulteriori informazioni sulle chiavi di test e di produzione, vedere [chiavi di test e di produzione per un negozio online di tipo 1](test-and-production-keys-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="4f178-159">For more information about the test and production keys, see [Test and Production Keys for a Type 1 Online Store](test-and-production-keys-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="4f178-160">Inserire la chiave di test o di produzione nel seguente percorso del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4f178-160">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="4f178-161">Si noti che il valore della voce del registro di sistema TestParameter può specificare più chiavi di test o di produzione.</span><span class="sxs-lookup"><span data-stu-id="4f178-161">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="4f178-162">Si supponga, ad esempio, che Proseware disponga di una chiave di test "1234" e che Contoso disponga di una chiave di test "2345".</span><span class="sxs-lookup"><span data-stu-id="4f178-162">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="4f178-163">La voce del registro di sistema seguente specifica che gli archivi di test per Proseware e contoso verranno visualizzati in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4f178-163">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="4f178-164">**Voce del registro di sistema ActiveService**</span><span class="sxs-lookup"><span data-stu-id="4f178-164">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="4f178-165">Quando l'utente attiva uno Store online, Windows Media Player scrive le informazioni nel registro di sistema che identifica l'archivio online attivo.</span><span class="sxs-lookup"><span data-stu-id="4f178-165">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="4f178-166">Windows Media Player inserisce le informazioni nel seguente percorso del registro di sistema nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4f178-166">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="4f178-167">Nella sintassi del registro di sistema precedente, *serviceInfo* è un segnaposto per una stringa che contiene informazioni descrittive sull'archivio online attivo.</span><span class="sxs-lookup"><span data-stu-id="4f178-167">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f178-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f178-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f178-169">**Riferimento per negozi online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="4f178-169">**Reference for Type 1 Online Stores**</span></span>](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





