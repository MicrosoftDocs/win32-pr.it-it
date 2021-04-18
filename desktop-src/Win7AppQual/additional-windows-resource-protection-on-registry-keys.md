---
description: .
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Protezione risorse di Windows aggiuntive sulle chiavi del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb048a45324e52c9b9319f52f95b64361b95bbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318898"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a><span data-ttu-id="de48d-103">Protezione risorse di Windows aggiuntive sulle chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="de48d-103">Additional Windows Resource Protection on Registry Keys</span></span>

## <a name="platform"></a><span data-ttu-id="de48d-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="de48d-104">Platform</span></span>

<span data-ttu-id="de48d-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="de48d-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="de48d-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de48d-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="de48d-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="de48d-107">Feature Impact</span></span>

<span data-ttu-id="de48d-108">**Gravità** -medio</span><span class="sxs-lookup"><span data-stu-id="de48d-108">**Severity** - Medium</span></span>  
<span data-ttu-id="de48d-109">**Frequenza** -bassa</span><span class="sxs-lookup"><span data-stu-id="de48d-109">**Frequency** - Low</span></span>  


## <a name="description"></a><span data-ttu-id="de48d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de48d-110">Description</span></span>

<span data-ttu-id="de48d-111">Altre risorse di sistema hanno aggiunto le impostazioni Protezione risorse di Windows (WRP) in Windows 7, rendendole impostazioni di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="de48d-111">Additional system resources have added Windows Resource Protection (WRP) settings in Windows 7, making them read-only settings.</span></span> <span data-ttu-id="de48d-112">La maggior parte delle risorse che hanno ricevuto una protezione aggiuntiva è costituita da chiavi server COM di sistema, anche se alcune funzionalità hanno aggiunto la protezione delle risorse di destinazione.</span><span class="sxs-lookup"><span data-stu-id="de48d-112">The vast majority of resources that received added protection are system COM server keys, although some features have added targeted resource protection.</span></span> <span data-ttu-id="de48d-113">Microsoft ha modificato queste risorse per proteggere il sistema e le altre applicazioni e fornire una piattaforma stabile e coerente su cui possano essere eseguite in modo affidabile le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="de48d-113">Microsoft changed these resources in order to protect the system and other applications from breaking each other and to provide a consistent, stable platform upon which applications can reliably run.</span></span> <span data-ttu-id="de48d-114">In passato, le applicazioni potevano fornire file personalizzati e utilizzare la registrazione COM non protetta per modificare il sistema.</span><span class="sxs-lookup"><span data-stu-id="de48d-114">In the past, applications could provide custom files and use the unprotected COM registration to change the system.</span></span> <span data-ttu-id="de48d-115">Nel caso di applicazioni meno recenti, questo può effettuare il downgrade dei runtime di sistema o modificare l'interfaccia su cui altre applicazioni necessitano di funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="de48d-115">In the case of older applications, this can downgrade system runtimes or change the interface upon which other applications needed to work properly.</span></span> <span data-ttu-id="de48d-116">Nel peggiore dei casi, tali installazioni potrebbero causare un errore o un calo del sistema nel tempo.</span><span class="sxs-lookup"><span data-stu-id="de48d-116">In the worst case, such installations could cause system failure or degradation over time.</span></span> <span data-ttu-id="de48d-117">Per offrire un'esperienza migliore e una piattaforma applicativa più stabile, abbiamo bloccato queste registrazioni, in modo che solo gli aggiornamenti Microsoft potessero modificare i componenti di sistema.</span><span class="sxs-lookup"><span data-stu-id="de48d-117">To provide a better experience and a more stable application platform, we locked down these registrations so that only Microsoft updates could change system components.</span></span>

<span data-ttu-id="de48d-118">Poiché la maggior parte delle risorse modificate sono chiavi COM utilizzate dal sistema, questa modifica non influirà sulla maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="de48d-118">Since most resources changed are COM keys used by the system, this change will not affect the majority of applications.</span></span> <span data-ttu-id="de48d-119">Sebbene ci si aspetta che la maggior parte delle applicazioni abbia un'esperienza migliore in Windows 7 in seguito a queste modifiche, un piccolo subset di applicazioni potrebbe essere influenzato negativamente.</span><span class="sxs-lookup"><span data-stu-id="de48d-119">While we expect most applications to have a better experience on Windows 7 as a result of these changes, a small subset of applications may be negatively affected.</span></span> <span data-ttu-id="de48d-120">I livelli di compatibilità delle applicazioni del sistema risolveranno automaticamente i problemi di installazione indicando sempre all'applicazione che è riuscita a modificare un'impostazione, anche se non è riuscita perché è una risorsa protetta.</span><span class="sxs-lookup"><span data-stu-id="de48d-120">The system's application compatibility layers will automatically resolve setup problems by always telling the application that it succeeded in changing a setting, even if it failed due to it being a protected resource.</span></span> <span data-ttu-id="de48d-121">In questo modo si impedisce l'interruzioni delle configurazioni dell'applicazione, ma possono verificarsi problemi se è necessario modificare l'impostazione affinché l'applicazione funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="de48d-121">This prevents application setups from breaking but may cause problems if the setting needed to be changed in order for the application to function properly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="de48d-122">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="de48d-122">Manifestation</span></span>

<span data-ttu-id="de48d-123">Le applicazioni potrebbero avere modificato queste impostazioni prima di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="de48d-123">Applications may have modified these settings prior to Windows 7.</span></span> <span data-ttu-id="de48d-124">Quando si esegue l'installazione in Windows 7, le applicazioni potrebbero rilevare che alcune funzionalità non funzionano più perché le impostazioni non riflettono ciò che è previsto per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de48d-124">Upon installing on Windows 7, applications may find certain features no longer work because the settings did not reflect what the application expected.</span></span>

<span data-ttu-id="de48d-125">Esistono due scenari in cui le applicazioni possono riscontrare problemi correlati a questa protezione aggiuntiva:</span><span class="sxs-lookup"><span data-stu-id="de48d-125">There are two scenarios in which applications may encounter problems related to this added protection:</span></span>

-   <span data-ttu-id="de48d-126">Applicazioni che potrebbero avere utilizzato le impostazioni protette da ora come archivio dati o come punto di estensibilità raro o non intenzionale</span><span class="sxs-lookup"><span data-stu-id="de48d-126">Applications that may have been using the now-protected settings as a data store or as a rare or unintended extensibility point</span></span>
-   <span data-ttu-id="de48d-127">In rari casi, il meccanismo di rilevamento usato per identificare le configurazioni dell'applicazione potrebbe non riconoscere una particolare configurazione, quindi il livello di mitigazione della compatibilità delle applicazioni potrebbe non essere applicato</span><span class="sxs-lookup"><span data-stu-id="de48d-127">In rare cases, the detection mechanism used to identify application setups may not recognize a particular setup and so the application compatibility mitigation layer may not be applied</span></span>

## <a name="mitigation"></a><span data-ttu-id="de48d-128">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="de48d-128">Mitigation</span></span>

<span data-ttu-id="de48d-129">Il metodo principale di mitigazione è il livello di compatibilità delle applicazioni del sistema, che viene applicato automaticamente alle configurazioni dell'applicazione quando viene rilevato.</span><span class="sxs-lookup"><span data-stu-id="de48d-129">The primary means of mitigation is the system's application compatibility layer, which is automatically applied to application setups when detected.</span></span> <span data-ttu-id="de48d-130">È anche possibile applicarla manualmente a qualsiasi applicazione usando la scheda compatibilità nelle proprietà dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de48d-130">You can also manually apply it to any application using the compatibility tab in the application's properties.</span></span>

<span data-ttu-id="de48d-131">Questo livello risolve il problema intercettando le operazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="de48d-131">This layer resolves the problem by intercepting registry operations.</span></span> <span data-ttu-id="de48d-132">Nel caso in cui l'applicazione tenti di modificare un'impostazione di sola lettura (WRP), il livello restituisce sempre esito positivo, anche se l'impostazione non è stata effettivamente modificata.</span><span class="sxs-lookup"><span data-stu-id="de48d-132">In the case where the application was attempting to modify a read-only (WRP) setting, the layer always returns success, even though the setting was not really changed.</span></span> <span data-ttu-id="de48d-133">Per la maggior parte delle applicazioni, questa operazione non provocherà alcun problema.</span><span class="sxs-lookup"><span data-stu-id="de48d-133">For most applications, this will cause no problems.</span></span> <span data-ttu-id="de48d-134">Tuttavia, è possibile che l'applicazione abbia richiesto l'impostazione modificata per funzionare correttamente, ovvero il primo scenario descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="de48d-134">However, there is a possibility that the application needed that setting changed in order to function properly, which is the first scenario described above.</span></span>

## <a name="solution"></a><span data-ttu-id="de48d-135">Soluzione</span><span class="sxs-lookup"><span data-stu-id="de48d-135">Solution</span></span>

<span data-ttu-id="de48d-136">Per i due scenari indicati in precedenza:</span><span class="sxs-lookup"><span data-stu-id="de48d-136">For the two scenarios identified above:</span></span>

-   <span data-ttu-id="de48d-137">Se l'applicazione richiede che la chiave sia scrivibile per funzionare o usare l'archivio dati, non esiste alcuna soluzione diversa dalla modifica dell'applicazione in modo che non scriva più in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="de48d-137">If the application requires the key to be writable in order to function or use the data store, there is no solution other than changing the application so that it no longer writes to that location.</span></span>
-   <span data-ttu-id="de48d-138">Se il livello di compatibilità non è stato applicato a una configurazione, l'errore di installazione deve essere rilevato e offerto per essere applicato ed eseguito nuovamente.</span><span class="sxs-lookup"><span data-stu-id="de48d-138">If the compatibility layer was not applied to a setup, the setup failure should be detected and offered to be applied and re-run.</span></span> <span data-ttu-id="de48d-139">Le applicazioni possono anche essere eseguite in modalità di compatibilità, nel qual caso il livello di mitigazione viene sempre applicato.</span><span class="sxs-lookup"><span data-stu-id="de48d-139">Applications can also run in compatibility mode, in which case the mitigation layer is always applied.</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="de48d-140">Test di compatibilità</span><span class="sxs-lookup"><span data-stu-id="de48d-140">Compatibility Tests</span></span>

<span data-ttu-id="de48d-141">Come rilevare se per un'applicazione è stata applicata la mitigazione WRP:</span><span class="sxs-lookup"><span data-stu-id="de48d-141">How to detect if an application had WRP mitigation applied to it:</span></span>

-   <span data-ttu-id="de48d-142">Windows Installer è a conoscenza di WRP; ignora automaticamente i tentativi di scrittura o modifica di una risorsa protetta.</span><span class="sxs-lookup"><span data-stu-id="de48d-142">Windows Installer is aware of WRP; it automatically and silently ignores attempts to write or modify a protected resource.</span></span> <span data-ttu-id="de48d-143">Se l'applicazione è stata installata con Windows Installer e la registrazione è stata abilitata, viene registrato un avviso per ogni operazione di scrittura della chiave del registro di sistema che è stata ignorata perché è una risorsa protetta da WRP.</span><span class="sxs-lookup"><span data-stu-id="de48d-143">If the application was installed with Windows Installer and logging was enabled, then a warning will be logged for each registry key write operation that was ignored due to its being a WRP-protected resource.</span></span>
-   <span data-ttu-id="de48d-144">L'API WRP incorpora SfCIsKeyProtected, che può eseguire una query se una chiave del registro di sistema è protetta da WRP nel sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="de48d-144">The WRP API incorporates SfCIsKeyProtected, which can query if a registry key is WRP-protected on the current system.</span></span> <span data-ttu-id="de48d-145">Per altre informazioni sull'uso di questa API, vedere la voce relativa a WRP in MSDN nei collegamenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="de48d-145">See the WRP entry in MSDN in the links below for additional information on using this API.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="de48d-146">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="de48d-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="de48d-147">Protezione risorse di Windows</span><span class="sxs-lookup"><span data-stu-id="de48d-147">Windows Resource Protection</span></span>](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
