---
description: .
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifesto dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4fd1ae8a9f66dafbe65a3db09dd014dbef31e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318888"
---
# <a name="application-manifest"></a><span data-ttu-id="75a8f-103">Manifesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="75a8f-103">Application Manifest</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="75a8f-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="75a8f-104">Affected Platforms</span></span>

<span data-ttu-id="75a8f-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="75a8f-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="75a8f-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="75a8f-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="75a8f-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="75a8f-107">Feature Impact</span></span>

 <span data-ttu-id="75a8f-108">**Gravità** -bassa</span><span class="sxs-lookup"><span data-stu-id="75a8f-108">**Severity** - Low</span></span>  
<span data-ttu-id="75a8f-109">**Frequenza** -bassa</span><span class="sxs-lookup"><span data-stu-id="75a8f-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="75a8f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75a8f-110">Description</span></span>

<span data-ttu-id="75a8f-111">In Windows 7 è stata introdotta una nuova sezione nel manifesto dell'applicazione denominata "compatibilità".</span><span class="sxs-lookup"><span data-stu-id="75a8f-111">Windows 7 introduces a new section in the application manifest called "Compatibility."</span></span> <span data-ttu-id="75a8f-112">Questa sezione consente a Windows di determinare le versioni di Windows per cui un'applicazione è stata progettata come destinazione e consente a Windows di fornire il comportamento previsto dall'applicazione in base alla versione di Windows di destinazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="75a8f-112">This section helps Windows determine the versions of Windows that an application was designed to target, and enables Windows to provide the behavior that the application expects based on the version of Windows that the application targeted.</span></span>

<span data-ttu-id="75a8f-113">La sezione compatibilità consente a Windows di fornire nuovo comportamento al nuovo software creato dagli sviluppatori, mantenendo al tempo stesso la compatibilità per il software esistente.</span><span class="sxs-lookup"><span data-stu-id="75a8f-113">The Compatibility section allows Windows to provide new behavior to new developer-created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="75a8f-114">Questa sezione consente inoltre a Windows di garantire una maggiore compatibilità nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="75a8f-114">This section also helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="75a8f-115">Ad esempio, un'applicazione che dichiara il supporto solo per Windows 7 nella sezione compatibilità continuerà a ricevere il comportamento di Windows 7 nella versione futura di Windows.</span><span class="sxs-lookup"><span data-stu-id="75a8f-115">For example, an application declaring support only for Windows 7 in the Compatibility section will continue to receive Windows 7 behavior in future version of Windows.</span></span>

## <a name="manifestation-of-change"></a><span data-ttu-id="75a8f-116">Manifesto della modifica</span><span class="sxs-lookup"><span data-stu-id="75a8f-116">Manifestation of Change</span></span>

<span data-ttu-id="75a8f-117">Le applicazioni prive di una sezione di compatibilità nel manifesto riceveranno il comportamento di Windows Vista per impostazione predefinita in Windows 7 e nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="75a8f-117">Applications without a Compatibility section in their manifest will receive Windows Vista behavior by default on Windows 7 and future Windows versions.</span></span> <span data-ttu-id="75a8f-118">Si noti che Windows XP e Windows Vista ignorano questa sezione del manifesto e non hanno alcun effetto su di essi.</span><span class="sxs-lookup"><span data-stu-id="75a8f-118">Note that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="75a8f-119">I componenti di Windows seguenti forniscono un comportamento divergente basato sulla sezione compatibilità di Windows 7:</span><span class="sxs-lookup"><span data-stu-id="75a8f-119">The following Windows components provide divergent behavior based on the Compatibility section in Windows 7:</span></span>

<span data-ttu-id="75a8f-120">**Pool di thread predefinito RPC**</span><span class="sxs-lookup"><span data-stu-id="75a8f-120">**RPC Default Thread Pool**</span></span>

-   <span data-ttu-id="75a8f-121">**Windows 7:** Per migliorare la scalabilità e ridurre i conteggi dei thread, RPC passa al pool di thread NT (pool predefinito).</span><span class="sxs-lookup"><span data-stu-id="75a8f-121">**Windows 7:** To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="75a8f-122">Per Windows Vista, RPC usava un pool di thread privato.</span><span class="sxs-lookup"><span data-stu-id="75a8f-122">For Windows Vista, RPC used a private thread pool.</span></span>
    -   <span data-ttu-id="75a8f-123">Per i binari compilati per Win7 viene usato il pool predefinito</span><span class="sxs-lookup"><span data-stu-id="75a8f-123">For binaries compiled for Win7 the default pool is used</span></span>
    -   <span data-ttu-id="75a8f-124">Se si \_ chiama RpcMgmtEnableDedicatedThreadPool prima che venga chiamata un'API RPC, viene usato il pool di thread privati (comportamento di vista)</span><span class="sxs-lookup"><span data-stu-id="75a8f-124">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior)</span></span>
    -   <span data-ttu-id="75a8f-125">Se I \_ RpcMgmtEnableDedicatedThreadPool vengono chiamati dopo una chiamata RPC, viene usato il pool predefinito, \_ RpcMgmtEnableDedicatedThreadPool restituisce l'errore 1764 e l'operazione richiesta non è supportata</span><span class="sxs-lookup"><span data-stu-id="75a8f-125">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported</span></span>
-   <span data-ttu-id="75a8f-126">**Windows Vista (impostazione predefinita):** Per i file binari compilati per Windows Vista e versioni precedenti, viene usato il pool privato.</span><span class="sxs-lookup"><span data-stu-id="75a8f-126">**Windows Vista (default):** For binaries compiled for Windows Vista and below, the private pool is used.</span></span>

<span data-ttu-id="75a8f-127">**Blocco DirectDraw**</span><span class="sxs-lookup"><span data-stu-id="75a8f-127">**DirectDraw Lock**</span></span>

-   <span data-ttu-id="75a8f-128">**Windows 7:** Le applicazioni manifeste per Windows 7 non possono chiamare l'API Lock in DDRAW per bloccare il buffer video del desktop primario.</span><span class="sxs-lookup"><span data-stu-id="75a8f-128">**Windows 7:** Applications manifested for Windows 7 cannot call Lock API in DDRAW to lock the primary Desktop video buffer.</span></span> <span data-ttu-id="75a8f-129">Questa operazione genera un errore e viene restituito un puntatore **null** per il database primario.</span><span class="sxs-lookup"><span data-stu-id="75a8f-129">Doing so will result in error, and **NULL** pointer for the primary will be returned.</span></span> <span data-ttu-id="75a8f-130">Questo comportamento viene applicato anche se Gestione finestre desktop composizione non è attivata.</span><span class="sxs-lookup"><span data-stu-id="75a8f-130">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="75a8f-131">Le applicazioni compatibili con Windows 7 non devono bloccare il rendering del buffer video primario.</span><span class="sxs-lookup"><span data-stu-id="75a8f-131">Windows 7 compatible applications must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="75a8f-132">**Windows Vista (impostazione predefinita):** Le applicazioni potranno acquisire un blocco sul buffer video primario perché le applicazioni legacy dipendono da questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="75a8f-132">**Windows Vista (default):** Applications will be able to acquire a lock on the primary video buffer as legacy applications depend on this behavior.</span></span> <span data-ttu-id="75a8f-133">L'esecuzione dell'applicazione disattiva Gestione finestre desktop.</span><span class="sxs-lookup"><span data-stu-id="75a8f-133">Running the application turns off Desktop Window Manager.</span></span>

<span data-ttu-id="75a8f-134">**Il trasferimento di blocchi di bit (BLT) a database primario senza finestra di ridimensionamento**</span><span class="sxs-lookup"><span data-stu-id="75a8f-134">**DirectDraw Bit Block Transfer (Blt) to Primary without Clipping Window**</span></span>

-   <span data-ttu-id="75a8f-135">**Windows 7:** Le applicazioni manifeste per Windows 7 non sono in grado di eseguire BLT nel buffer video del desktop primario senza una finestra di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="75a8f-135">**Windows 7:** Applications manifested for Windows 7 are prevented from performing Blt's to the primary Desktop video buffer without a clipping window.</span></span> <span data-ttu-id="75a8f-136">In caso contrario, verrà generato un errore e non verrà eseguito il rendering dell'area BLT.</span><span class="sxs-lookup"><span data-stu-id="75a8f-136">Doing so will result in error and the Blt area will not be rendered.</span></span> <span data-ttu-id="75a8f-137">Windows applica questo comportamento anche se non si attiva Gestione finestre desktop composizione.</span><span class="sxs-lookup"><span data-stu-id="75a8f-137">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="75a8f-138">Le applicazioni compatibili con Windows 7 devono essere BLT in una finestra di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="75a8f-138">Windows 7 compatible applications must Blt to a clipping window.</span></span>
-   <span data-ttu-id="75a8f-139">**Windows Vista (impostazione predefinita):** Le applicazioni devono essere in grado di eseguire il BLT nel database primario senza una finestra di ridimensionamento poiché le applicazioni legacy dipendono da questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="75a8f-139">**Windows Vista (default):** Applications must be able to Blt to the primary without a clipping window as legacy applications depend on this behavior.</span></span> <span data-ttu-id="75a8f-140">L'esecuzione di questa applicazione disattiva la Gestione finestre desktop.</span><span class="sxs-lookup"><span data-stu-id="75a8f-140">Running this application turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="75a8f-141">**API GetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="75a8f-141">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="75a8f-142">**Windows 7:** Risolve un race condition in cui un'app multithreading che usa GetOverlappedResult può restituire senza reimpostare l'evento nella struttura sovrapposta, causando la restituzione anticipata della chiamata successiva a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="75a8f-142">**Windows 7:** Resolves a race condition where a multithreaded app using GetOverlappedResult can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="75a8f-143">**Windows Vista (impostazione predefinita):** Fornisce il comportamento con il race condition cui le applicazioni possono avere una dipendenza.</span><span class="sxs-lookup"><span data-stu-id="75a8f-143">**Windows Vista (default):** Provides the behavior with the race condition that applications may have a dependency on.</span></span> <span data-ttu-id="75a8f-144">Le applicazioni che desiderano evitare questa corsa prima del comportamento di Windows 7 devono attendere l'evento sovrapposto e, quando segnalato, chiamare GetOverlappedResult con bWait = = **false**.</span><span class="sxs-lookup"><span data-stu-id="75a8f-144">Applications wishing to avoid this race prior to the Windows 7 behavior should wait on the overlapped event and when signaled, call GetOverlappedResult with bWait == **FALSE**.</span></span>

<span data-ttu-id="75a8f-145">**Assistente compatibilità programmi (PCA)**</span><span class="sxs-lookup"><span data-stu-id="75a8f-145">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="75a8f-146">**Windows 7:** La sezione applicazioni con compatibilità non otterrà la mitigazione PCA.</span><span class="sxs-lookup"><span data-stu-id="75a8f-146">**Windows 7:** Applications with Compatibility section will not get the PCA mitigation.</span></span>
-   <span data-ttu-id="75a8f-147">**Windows Vista (impostazione predefinita):** Le applicazioni che non vengono installate correttamente o si arrestano in modo anomalo in fase di esecuzione in alcune circostanze specifiche otterranno la mitigazione PCA.</span><span class="sxs-lookup"><span data-stu-id="75a8f-147">**Windows Vista (default):** Applications that fail to install properly or crash during runtime under some specific circumstances will get the PCA mitigation.</span></span> <span data-ttu-id="75a8f-148">Per ulteriori informazioni, vedere la sezione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="75a8f-148">For more details, see the reference section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="75a8f-149">Sfruttando le funzionalità</span><span class="sxs-lookup"><span data-stu-id="75a8f-149">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="75a8f-150">Aggiornare il manifesto dell'applicazione con le informazioni di compatibilità più recenti per il supporto del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="75a8f-150">Update the application manifest with the latest Compatibility information for operating system support.</span></span> <span data-ttu-id="75a8f-151">La sezione descrive le aggiunte al manifesto:</span><span class="sxs-lookup"><span data-stu-id="75a8f-151">The section describes the additions to the manifest:</span></span>

-   <span data-ttu-id="75a8f-152">**Spazio dei nomi:** Compatibility. V1 (xmlns = "urn: schemas-microsoft-com: Compatibility. V1" >)</span><span class="sxs-lookup"><span data-stu-id="75a8f-152">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

-   <span data-ttu-id="75a8f-153">**Nome della sezione:** Compatibilità (nuova sezione)</span><span class="sxs-lookup"><span data-stu-id="75a8f-153">**Section Name:** Compatibility (new section)</span></span>

-   <span data-ttu-id="75a8f-154">**Supportato:** GUID del sistema operativo supportato: i GUID che eseguono il mapping ai sistemi operativi supportati sono:</span><span class="sxs-lookup"><span data-stu-id="75a8f-154">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

    -   <span data-ttu-id="75a8f-155">{e2011457-1546-43C5-a5fe-008deee3d3f0} per Windows Vista: si tratta del valore predefinito per il contesto Switchback.</span><span class="sxs-lookup"><span data-stu-id="75a8f-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} for Windows Vista: This is the default value for the switchback context.</span></span>
    -   <span data-ttu-id="75a8f-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} per Windows 7: le applicazioni che impostano questo valore nel manifesto dell'applicazione ottengono il comportamento di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="75a8f-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} for Windows 7: Applications that set this value in the application manifest get the Windows 7 behavior.</span></span>

    > [!Note]  
    > <span data-ttu-id="75a8f-157">Microsoft genererà e pubblicherà i GUID per le versioni future di Windows in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="75a8f-157">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

     

<span data-ttu-id="75a8f-158">Di seguito è riportato un esempio di un manifesto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="75a8f-158">The following is an example of an updated manifest.</span></span>

> [!Note]  
> <span data-ttu-id="75a8f-159">I nomi di attributo e tag nel manifesto dell'applicazione fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="75a8f-159">The attribute and tag names in the application manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



<span data-ttu-id="75a8f-160">Il valore di aggiunta di GUID per entrambi i sistemi operativi nell'esempio precedente consiste nel fornire supporto di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="75a8f-160">The value of adding GUIDs for both operating systems in the above example is to provide down-level support.</span></span> <span data-ttu-id="75a8f-161">Le applicazioni che supportano entrambe le piattaforme non necessitano di manifesti distinti per ogni piattaforma.</span><span class="sxs-lookup"><span data-stu-id="75a8f-161">Applications that support both platforms would not need separate manifests for each platform.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="75a8f-162">Compatibilità, prestazioni, affidabilità e test di usabilità</span><span class="sxs-lookup"><span data-stu-id="75a8f-162">Compatibility, Performance, Reliability, and Usability Testing</span></span>

1.  <span data-ttu-id="75a8f-163">Testare l'applicazione con la nuova sezione compatibilità e `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` verificare che l'applicazione funzioni correttamente usando il comportamento più recente di Windows 7</span><span class="sxs-lookup"><span data-stu-id="75a8f-163">Test the application with the new compatibility section and `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` to ensure that the application works properly using the latest Windows 7 behavior</span></span>
2.  <span data-ttu-id="75a8f-164">Testare l'applicazione con la nuova sezione di compatibilità e `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (o senza questa sezione) per assicurarsi che l'applicazione funzioni correttamente utilizzando i comportamenti di Windows Vista in Windows 7</span><span class="sxs-lookup"><span data-stu-id="75a8f-164">Test the application with the new compatibility section and `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (or without this section entirely) to ensure that the application works properly using the Windows Vista behaviors on Windows 7</span></span>

## <a name="known-issues"></a><span data-ttu-id="75a8f-165">Problemi noti</span><span class="sxs-lookup"><span data-stu-id="75a8f-165">Known Issues</span></span>

<span data-ttu-id="75a8f-166">**Mancata corrispondenza del contesto** Un'applicazione viene eseguita in un contesto di Windows Vista anziché in un contesto di Windows 7 in un computer in cui è in esecuzione un'edizione x64 di Windows 7 o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="75a8f-166">**Context Mismatch** An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of either Windows 7 or Windows Server 2008 R2.</span></span>

<span data-ttu-id="75a8f-167">**Soluzione** di Sono disponibili aggiornamenti per correggere questa operazione per tutte le versioni supportate di Windows 7 e Windows Server 2008 R2, nonché per tutte le versioni basate su Itanium supportate di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="75a8f-167">**Solution** Updates are available to correct this for all supported x64-based versions of Windows 7 and Windows Server 2008 R2, as well as for all supported Itanium-based versions of Windows Server 2008 R2.</span></span> <span data-ttu-id="75a8f-168">Passare alla pagina supporto tecnico Microsoft per [KB 978637: un'applicazione viene eseguita in un contesto di Windows Vista anziché in un contesto di Windows 7 in un computer in cui è in esecuzione un'edizione x64 di Windows 7 o Windows Server 2008 R2](https://support.microsoft.com/kb/978637) per ulteriori dettagli e per scaricare la versione corretta per il sistema.</span><span class="sxs-lookup"><span data-stu-id="75a8f-168">Go to the Microsoft Support page for [KB 978637: An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of Windows 7 or of Windows Server 2008 R2](https://support.microsoft.com/kb/978637) for additional details and to download the correct version for your system.</span></span>

<span data-ttu-id="75a8f-169">**Diagnosi del dump di arresto anomalo bloccata**</span><span class="sxs-lookup"><span data-stu-id="75a8f-169">**Crash dump diagnosis blocked**</span></span>

<span data-ttu-id="75a8f-170">**Soluzione** di Passare alla pagina supporto tecnico Microsoft per [KB 976038: le eccezioni generate da un'applicazione in esecuzione in una versione di Windows a 64 bit vengono ignorate](https://support.microsoft.com/kb/976038) per ulteriori dettagli.</span><span class="sxs-lookup"><span data-stu-id="75a8f-170">**Solution** Go to the Microsoft Support page for [KB 976038: Exceptions that are thrown from an application that runs in a 64-bit version of Windows are ignored](https://support.microsoft.com/kb/976038) for additional details.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="75a8f-171">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="75a8f-171">Links to Other Resources</span></span>

-   [<span data-ttu-id="75a8f-172">**QueryActCtxW (funzione)**</span><span class="sxs-lookup"><span data-stu-id="75a8f-172">**QueryActCtxW Function**</span></span>](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   <span data-ttu-id="75a8f-173">[Manifesto UAC](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="75a8f-173">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="75a8f-174">Manifesti dell'applicazione per applicazioni Windows</span><span class="sxs-lookup"><span data-stu-id="75a8f-174">Application manifests for Windows applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="75a8f-175">Gestione finestre desktop (DWM)</span><span class="sxs-lookup"><span data-stu-id="75a8f-175">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="75a8f-176">Aggiornamento del contesto non corrispondente</span><span class="sxs-lookup"><span data-stu-id="75a8f-176">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)

 

 
