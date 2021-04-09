---
title: Chiavi del registro di sistema e voci per un archivio di tipo 2 online
description: Chiavi del registro di sistema e voci per un archivio di tipo 2 online
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Windows Media Player Online Stores, registro di sistema
- archivi online, registro di sistema
- digitare 2 archivi online, registro di sistema
- Registro di sistema, digitare 2 archivi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117443"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a><span data-ttu-id="3c48c-107">Chiavi del registro di sistema e voci per un archivio di tipo 2 online</span><span class="sxs-lookup"><span data-stu-id="3c48c-107">Registry Keys and Entries for a Type 2 Online Store</span></span>

> [!Note]  
> <span data-ttu-id="3c48c-108">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="3c48c-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3c48c-109">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3c48c-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3c48c-110">Per rendere disponibile un archivio online di tipo 2 in Windows Media Player, il provider di archivio online deve creare le sottochiavi e le voci del registro di sistema seguenti nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3c48c-110">To make a type 2 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="3c48c-111">Nella sintassi del registro di sistema precedente, i simboli in corsivo sono segnaposto per i nomi e identificatori univoci globali (GUID) specifici per l'archivio online.</span><span class="sxs-lookup"><span data-stu-id="3c48c-111">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="3c48c-112">Nella tabella seguente vengono descritti i segnaposto.</span><span class="sxs-lookup"><span data-stu-id="3c48c-112">The following table describes those placeholders.</span></span>



| <span data-ttu-id="3c48c-113">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="3c48c-113">Placeholder</span></span>    | <span data-ttu-id="3c48c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c48c-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c48c-115">*keyName*</span><span class="sxs-lookup"><span data-stu-id="3c48c-115">*keyName*</span></span>      | <span data-ttu-id="3c48c-116">Stringa concordata tra Microsoft e il negozio online.</span><span class="sxs-lookup"><span data-stu-id="3c48c-116">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="3c48c-117">Questa stringa identifica in modo univoco l'archivio online. Esempio: "Proseware"</span><span class="sxs-lookup"><span data-stu-id="3c48c-117">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3c48c-118">*flags*</span><span class="sxs-lookup"><span data-stu-id="3c48c-118">*flags*</span></span>        | <span data-ttu-id="3c48c-119">Un operatore OR bit per bit di **uno o più** plug-in flag di funzionalità questi flag specificano se Windows Media Player deve chiamare metodi specifici di [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) e [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2).</span><span class="sxs-lookup"><span data-stu-id="3c48c-119">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) and [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2).</span></span> <span data-ttu-id="3c48c-120">Per informazioni sui flag supportati, vedere la tabella dei flag di funzionalità plug-in che seguono questa tabella. Esempio: 00000037</span><span class="sxs-lookup"><span data-stu-id="3c48c-120">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000037</span></span><br/> |
| <span data-ttu-id="3c48c-121">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="3c48c-121">*clsid*</span></span>        | <span data-ttu-id="3c48c-122">GUID che rappresenta l'identificatore di classe (CLSID) per la classe che implementa **IWMPSubscriptionService** nel plug-in del negozio online.</span><span class="sxs-lookup"><span data-stu-id="3c48c-122">A GUID that is the class identifier (CLSID) for the class that implements **IWMPSubscriptionService** in the online store's plug-in.</span></span> <span data-ttu-id="3c48c-123">Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="3c48c-123">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                                    |
| <span data-ttu-id="3c48c-124">*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="3c48c-124">*friendlyname*</span></span> | <span data-ttu-id="3c48c-125">Nome descrittivo per il negozio online. Esempio: "Proseware Music Service"</span><span class="sxs-lookup"><span data-stu-id="3c48c-125">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="3c48c-126">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="3c48c-126">*pluginName*</span></span>   | <span data-ttu-id="3c48c-127">Nome del plug-in del negozio online. Esempio: "plug-in del servizio Proseware"</span><span class="sxs-lookup"><span data-stu-id="3c48c-127">A name for the online store's plug-in.Example: "Proseware Service Plug-in"</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3c48c-128">*className*</span><span class="sxs-lookup"><span data-stu-id="3c48c-128">*className*</span></span>    | <span data-ttu-id="3c48c-129">Nome della classe che implementa **IWMPSubscriptionService** nel plug-in del negozio online. Esempio: "CProsewareService"</span><span class="sxs-lookup"><span data-stu-id="3c48c-129">The name of the class that implements **IWMPSubscriptionService** in the online store's plug-in.Example: "CProsewareService"</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="3c48c-130">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="3c48c-130">*moduleName*</span></span>   | <span data-ttu-id="3c48c-131">Percorso completo della DLL che implementa il plug-in del negozio online. Esempio: "C: \\ Program Files \\ Proseware \\ProsewareService.dll"</span><span class="sxs-lookup"><span data-stu-id="3c48c-131">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareService.dll"</span></span><br/>                                                                                                                                                                                                                                                |



 

<span data-ttu-id="3c48c-132">Nella tabella seguente vengono descritti i flag di funzionalità plug-in.</span><span class="sxs-lookup"><span data-stu-id="3c48c-132">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="3c48c-133">Flag</span><span class="sxs-lookup"><span data-stu-id="3c48c-133">Flag</span></span>                                    | <span data-ttu-id="3c48c-134">valore</span><span class="sxs-lookup"><span data-stu-id="3c48c-134">Value</span></span> | <span data-ttu-id="3c48c-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c48c-135">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c48c-136">\_ALLOWPLAY Cap \_ sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="3c48c-136">SUBSCRIPTION\_CAP\_ALLOWPLAY</span></span>            | <span data-ttu-id="3c48c-137">0X1</span><span class="sxs-lookup"><span data-stu-id="3c48c-137">0X1</span></span>   | <span data-ttu-id="3c48c-138">Windows Media Player deve chiamare [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).</span><span class="sxs-lookup"><span data-stu-id="3c48c-138">Windows Media Player should call [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).</span></span>                                                                                                                      |
| <span data-ttu-id="3c48c-139">\_ALLOWCDBURN Cap \_ sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="3c48c-139">SUBSCRIPTION\_CAP\_ALLOWCDBURN</span></span>          | <span data-ttu-id="3c48c-140">0X2</span><span class="sxs-lookup"><span data-stu-id="3c48c-140">0X2</span></span>   | <span data-ttu-id="3c48c-141">Windows Media Player deve chiamare [IWMPSubscriptionService:: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).</span><span class="sxs-lookup"><span data-stu-id="3c48c-141">Windows Media Player should call [IWMPSubscriptionService::allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).</span></span>                                                                                                                  |
| <span data-ttu-id="3c48c-142">\_ALLOWPDATRANSFER Cap \_ sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="3c48c-142">SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER</span></span>     | <span data-ttu-id="3c48c-143">0X4</span><span class="sxs-lookup"><span data-stu-id="3c48c-143">0X4</span></span>   | <span data-ttu-id="3c48c-144">Windows Media Player deve chiamare [IWMPSubscriptionService:: allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).</span><span class="sxs-lookup"><span data-stu-id="3c48c-144">Windows Media Player should call [IWMPSubscriptionService::allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).</span></span>                                                                                                        |
| <span data-ttu-id="3c48c-145">\_BACKGROUNDPROCESSING Cap \_ sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="3c48c-145">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="3c48c-146">0X8</span><span class="sxs-lookup"><span data-stu-id="3c48c-146">0X8</span></span>   | <span data-ttu-id="3c48c-147">Windows Media Player deve chiamare [IWMPSubscriptionService:: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).</span><span class="sxs-lookup"><span data-stu-id="3c48c-147">Windows Media Player should call [IWMPSubscriptionService::startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).</span></span>                                                                                      |
| <span data-ttu-id="3c48c-148">\_DEVICEAVAILABLE Cap \_ sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="3c48c-148">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="3c48c-149">0X10</span><span class="sxs-lookup"><span data-stu-id="3c48c-149">0X10</span></span>  | <span data-ttu-id="3c48c-150">Windows Media Player deve chiamare [IWMPSubscriptionService2::D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).</span><span class="sxs-lookup"><span data-stu-id="3c48c-150">Windows Media Player should call [IWMPSubscriptionService2::deviceAvailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).</span></span>                                                                                                        |
| <span data-ttu-id="3c48c-151">\_PREPAREFORSYNC Cap \_ sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="3c48c-151">SUBSCRIPTION\_CAP\_PREPAREFORSYNC</span></span>       | <span data-ttu-id="3c48c-152">0X20</span><span class="sxs-lookup"><span data-stu-id="3c48c-152">0X20</span></span>  | <span data-ttu-id="3c48c-153">Windows Media Player deve chiamare [IWMPSubscriptionService2::P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span><span class="sxs-lookup"><span data-stu-id="3c48c-153">Windows Media Player should call [IWMPSubscriptionService2::prepareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span></span>                                                                                                          |
| <span data-ttu-id="3c48c-154">Caps della sottoscrizione \_ V1 \_</span><span class="sxs-lookup"><span data-stu-id="3c48c-154">SUBSCRIPTION\_V1\_CAPS</span></span>                  | <span data-ttu-id="3c48c-155">0XF</span><span class="sxs-lookup"><span data-stu-id="3c48c-155">0XF</span></span>   | <span data-ttu-id="3c48c-156">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3c48c-156">Default.</span></span> <span data-ttu-id="3c48c-157">Questo valore viene utilizzato se non ne viene registrato nessuno.</span><span class="sxs-lookup"><span data-stu-id="3c48c-157">This value is used if none is registered.</span></span> <span data-ttu-id="3c48c-158">Equivale a combinare \_ Cap \_ ALLOWPLAY, Subscription \_ Cap \_ ALLOWCDBURN, SUBSCRIPTION \_ Cap \_ ALLOWPDATRANSFER e Subscription \_ Cap \_ BACKGROUNDPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="3c48c-158">This is equivalent to combining SUBSCRIPTION\_CAP\_ALLOWPLAY, SUBSCRIPTION\_CAP\_ALLOWCDBURN, SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER, and SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING.</span></span> |



 

<span data-ttu-id="3c48c-159">**Voci del registro di sistema per sviluppo e test**</span><span class="sxs-lookup"><span data-stu-id="3c48c-159">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="3c48c-160">Quando si inizia a sviluppare lo Store online, Microsoft fornisce due chiavi: una chiave di test e una chiave di produzione.</span><span class="sxs-lookup"><span data-stu-id="3c48c-160">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="3c48c-161">Durante la fase di sviluppo e test, il negozio online verrà visualizzato in Windows Media Player solo se la chiave di test o la chiave di produzione si trova nel registro di sistema nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3c48c-161">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="3c48c-162">Per altre informazioni sulle chiavi di test e di produzione, vedere [chiavi di test e di produzione per un negozio online di tipo 2](test-and-production-keys-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="3c48c-162">For more information about the test and production keys, see [Test and Production Keys for a Type 2 Online Store](test-and-production-keys-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="3c48c-163">Inserire la chiave di test o di produzione nel seguente percorso del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3c48c-163">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="3c48c-164">Si noti che il valore della voce del registro di sistema TestParameter può specificare più chiavi di test o di produzione.</span><span class="sxs-lookup"><span data-stu-id="3c48c-164">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="3c48c-165">Si supponga, ad esempio, che Proseware disponga di una chiave di test "1234" e che Contoso disponga di una chiave di test "2345".</span><span class="sxs-lookup"><span data-stu-id="3c48c-165">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="3c48c-166">La voce del registro di sistema seguente specifica che gli archivi di test per Proseware e contoso verranno visualizzati in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3c48c-166">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="3c48c-167">**Voce del registro di sistema ActiveService**</span><span class="sxs-lookup"><span data-stu-id="3c48c-167">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="3c48c-168">Quando l'utente attiva uno Store online, Windows Media Player scrive le informazioni nel registro di sistema che identifica l'archivio online attivo.</span><span class="sxs-lookup"><span data-stu-id="3c48c-168">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="3c48c-169">Windows Media Player inserisce le informazioni nel seguente percorso del registro di sistema nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3c48c-169">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="3c48c-170">Nella sintassi del registro di sistema precedente, *serviceInfo* è un segnaposto per una stringa che contiene informazioni descrittive sull'archivio online attivo.</span><span class="sxs-lookup"><span data-stu-id="3c48c-170">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c48c-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c48c-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c48c-172">**Riferimento per negozi online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="3c48c-172">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





