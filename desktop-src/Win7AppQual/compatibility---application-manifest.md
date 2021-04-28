---
description: Manifesto dell'applicazione
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifesto dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c52b8eb2af87c271151be3d7989f50b2903084
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088589"
---
# <a name="application-manifest"></a><span data-ttu-id="23c31-103">Manifesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="23c31-103">Application Manifest</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="23c31-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="23c31-104">Affected Platforms</span></span>

<span data-ttu-id="23c31-105">**Client** - Windows 7</span><span class="sxs-lookup"><span data-stu-id="23c31-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="23c31-106">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="23c31-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="23c31-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="23c31-107">Feature Impact</span></span>

 <span data-ttu-id="23c31-108">**Gravità** - Bassa</span><span class="sxs-lookup"><span data-stu-id="23c31-108">**Severity** - Low</span></span>  
<span data-ttu-id="23c31-109">**Frequenza** - Bassa</span><span class="sxs-lookup"><span data-stu-id="23c31-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="23c31-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23c31-110">Description</span></span>

<span data-ttu-id="23c31-111">Windows 7 introduce una nuova sezione nel manifesto dell'applicazione denominata "Compatibilità".</span><span class="sxs-lookup"><span data-stu-id="23c31-111">Windows 7 introduces a new section in the application manifest called "Compatibility."</span></span> <span data-ttu-id="23c31-112">Questa sezione consente a Windows di determinare le versioni di Windows destinate a un'applicazione e consente a Windows di fornire il comportamento previsto dall'applicazione in base alla versione di Windows di destinazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="23c31-112">This section helps Windows determine the versions of Windows that an application was designed to target, and enables Windows to provide the behavior that the application expects based on the version of Windows that the application targeted.</span></span>

<span data-ttu-id="23c31-113">La sezione Compatibilità consente a Windows di fornire un nuovo comportamento al nuovo software creato dallo sviluppatore mantenendo al tempo stesso la compatibilità per il software esistente.</span><span class="sxs-lookup"><span data-stu-id="23c31-113">The Compatibility section allows Windows to provide new behavior to new developer-created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="23c31-114">Questa sezione consente anche a Windows di offrire maggiore compatibilità anche nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="23c31-114">This section also helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="23c31-115">Ad esempio, un'applicazione che dichiara il supporto solo per Windows 7 nella sezione Compatibilità continuerà a ricevere il comportamento di Windows 7 nella versione futura di Windows.</span><span class="sxs-lookup"><span data-stu-id="23c31-115">For example, an application declaring support only for Windows 7 in the Compatibility section will continue to receive Windows 7 behavior in future version of Windows.</span></span>

## <a name="manifestation-of-change"></a><span data-ttu-id="23c31-116">Modifica apportata</span><span class="sxs-lookup"><span data-stu-id="23c31-116">Manifestation of Change</span></span>

<span data-ttu-id="23c31-117">Le applicazioni senza una sezione Compatibility nel manifesto riceveranno il comportamento di Windows Vista per impostazione predefinita in Windows 7 e versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="23c31-117">Applications without a Compatibility section in their manifest will receive Windows Vista behavior by default on Windows 7 and future Windows versions.</span></span> <span data-ttu-id="23c31-118">Si noti che Windows XP e Windows Vista ignorano questa sezione del manifesto e non influiscono su di esse.</span><span class="sxs-lookup"><span data-stu-id="23c31-118">Note that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="23c31-119">I componenti di Windows seguenti offrono un comportamento divergente in base alla sezione Compatibilità in Windows 7:</span><span class="sxs-lookup"><span data-stu-id="23c31-119">The following Windows components provide divergent behavior based on the Compatibility section in Windows 7:</span></span>

<span data-ttu-id="23c31-120">**Pool di thread predefinito RPC**</span><span class="sxs-lookup"><span data-stu-id="23c31-120">**RPC Default Thread Pool**</span></span>

-   <span data-ttu-id="23c31-121">**Windows 7:** Per migliorare la scalabilità e ridurre il numero di thread, RPC è passata al pool di thread NT (pool predefinito).</span><span class="sxs-lookup"><span data-stu-id="23c31-121">**Windows 7:** To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="23c31-122">Per Windows Vista, RPC usa un pool di thread privato.</span><span class="sxs-lookup"><span data-stu-id="23c31-122">For Windows Vista, RPC used a private thread pool.</span></span>
    -   <span data-ttu-id="23c31-123">Per i file binari compilati per Win7 viene usato il pool predefinito</span><span class="sxs-lookup"><span data-stu-id="23c31-123">For binaries compiled for Win7 the default pool is used</span></span>
    -   <span data-ttu-id="23c31-124">Se I RpcMgmtEnableDedicatedThreadPool viene chiamato prima di qualsiasi API RPC, viene usato il pool di thread privato \_ (comportamento vista)</span><span class="sxs-lookup"><span data-stu-id="23c31-124">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior)</span></span>
    -   <span data-ttu-id="23c31-125">Se I RpcMgmtEnableDedicatedThreadPool viene chiamato dopo una chiamata RPC, viene usato il \_ pool predefinito, I RpcMgmtEnableDedicatedThreadPool restituisce l'errore 1764 e l'operazione richiesta non è \_ supportata</span><span class="sxs-lookup"><span data-stu-id="23c31-125">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported</span></span>
-   <span data-ttu-id="23c31-126">**Windows Vista (impostazione predefinita):** Per i file binari compilati per Windows Vista e versioni seguenti, viene usato il pool privato.</span><span class="sxs-lookup"><span data-stu-id="23c31-126">**Windows Vista (default):** For binaries compiled for Windows Vista and below, the private pool is used.</span></span>

<span data-ttu-id="23c31-127">**Blocco DirectDraw**</span><span class="sxs-lookup"><span data-stu-id="23c31-127">**DirectDraw Lock**</span></span>

-   <span data-ttu-id="23c31-128">**Windows 7:** Le applicazioni manifeste per Windows 7 non possono chiamare l'API Lock in DDRAW per bloccare il buffer video desktop primario.</span><span class="sxs-lookup"><span data-stu-id="23c31-128">**Windows 7:** Applications manifested for Windows 7 cannot call Lock API in DDRAW to lock the primary Desktop video buffer.</span></span> <span data-ttu-id="23c31-129">In questo modo verrà restituito un errore e verrà restituito **il puntatore NULL** per il database primario.</span><span class="sxs-lookup"><span data-stu-id="23c31-129">Doing so will result in error, and **NULL** pointer for the primary will be returned.</span></span> <span data-ttu-id="23c31-130">Questo comportamento viene applicato anche se Gestione finestre desktop composizione non è attivata.</span><span class="sxs-lookup"><span data-stu-id="23c31-130">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="23c31-131">Le applicazioni compatibili con Windows 7 non devono bloccare il buffer video primario per il rendering.</span><span class="sxs-lookup"><span data-stu-id="23c31-131">Windows 7 compatible applications must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="23c31-132">**Windows Vista (impostazione predefinita):** Le applicazioni saranno in grado di acquisire un blocco sul buffer video primario, in quanto le applicazioni legacy dipendono da questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="23c31-132">**Windows Vista (default):** Applications will be able to acquire a lock on the primary video buffer as legacy applications depend on this behavior.</span></span> <span data-ttu-id="23c31-133">L'esecuzione dell'applicazione Gestione finestre desktop.</span><span class="sxs-lookup"><span data-stu-id="23c31-133">Running the application turns off Desktop Window Manager.</span></span>

<span data-ttu-id="23c31-134">**Trasferimento del blocco di bit DirectDraw (Blt) a primario senza finestra di ritaglio**</span><span class="sxs-lookup"><span data-stu-id="23c31-134">**DirectDraw Bit Block Transfer (Blt) to Primary without Clipping Window**</span></span>

-   <span data-ttu-id="23c31-135">**Windows 7:** Alle applicazioni manifeste per Windows 7 non è consentito eseguire Blt nel buffer video desktop primario senza una finestra di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="23c31-135">**Windows 7:** Applications manifested for Windows 7 are prevented from performing Blt's to the primary Desktop video buffer without a clipping window.</span></span> <span data-ttu-id="23c31-136">In questo modo verrà generato un errore e non verrà eseguito il rendering dell'area Blt.</span><span class="sxs-lookup"><span data-stu-id="23c31-136">Doing so will result in error and the Blt area will not be rendered.</span></span> <span data-ttu-id="23c31-137">Windows applica questo comportamento anche se non si attiva Gestione finestre desktop composizione.</span><span class="sxs-lookup"><span data-stu-id="23c31-137">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="23c31-138">Le applicazioni compatibili con Windows 7 devono essere distribuite in una finestra di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="23c31-138">Windows 7 compatible applications must Blt to a clipping window.</span></span>
-   <span data-ttu-id="23c31-139">**Windows Vista (impostazione predefinita):** Le applicazioni devono essere in grado di eseguire il Blt nel database primario senza una finestra di ritaglio, in quanto le applicazioni legacy dipendono da questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="23c31-139">**Windows Vista (default):** Applications must be able to Blt to the primary without a clipping window as legacy applications depend on this behavior.</span></span> <span data-ttu-id="23c31-140">L'esecuzione di questa applicazione disattiva la Gestione finestre desktop.</span><span class="sxs-lookup"><span data-stu-id="23c31-140">Running this application turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="23c31-141">**GetOverlappedResult API**</span><span class="sxs-lookup"><span data-stu-id="23c31-141">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="23c31-142">**Windows 7:** Risolve un race condition in cui un'app multithreading che usa GetOverlappedResult può restituire senza reimpostare l'evento nella struttura sovrapposta, causando la restituzione prematura della chiamata successiva a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="23c31-142">**Windows 7:** Resolves a race condition where a multithreaded app using GetOverlappedResult can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="23c31-143">**Windows Vista (impostazione predefinita):** Fornisce il comportamento con il race condition da cui le applicazioni possono avere una dipendenza.</span><span class="sxs-lookup"><span data-stu-id="23c31-143">**Windows Vista (default):** Provides the behavior with the race condition that applications may have a dependency on.</span></span> <span data-ttu-id="23c31-144">Le applicazioni che vogliono evitare questa race prima del comportamento di Windows 7 devono attendere l'evento sovrapposto e, quando viene segnalato, chiamare GetOverlappedResult con bWait == **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="23c31-144">Applications wishing to avoid this race prior to the Windows 7 behavior should wait on the overlapped event and when signaled, call GetOverlappedResult with bWait == **FALSE**.</span></span>

<span data-ttu-id="23c31-145">**Program Compatibility Assistant (PCA)**</span><span class="sxs-lookup"><span data-stu-id="23c31-145">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="23c31-146">**Windows 7:** La sezione Applicazioni con compatibilità non riceverà la mitigazione PCA.</span><span class="sxs-lookup"><span data-stu-id="23c31-146">**Windows 7:** Applications with Compatibility section will not get the PCA mitigation.</span></span>
-   <span data-ttu-id="23c31-147">**Windows Vista (impostazione predefinita):** Le applicazioni che non vengono installate correttamente o si arresteranno in modo anomalo durante il runtime in determinate circostanze otterrà la mitigazione PCA.</span><span class="sxs-lookup"><span data-stu-id="23c31-147">**Windows Vista (default):** Applications that fail to install properly or crash during runtime under some specific circumstances will get the PCA mitigation.</span></span> <span data-ttu-id="23c31-148">Per altri dettagli, vedere la sezione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="23c31-148">For more details, see the reference section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="23c31-149">Uso delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="23c31-149">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="23c31-150">Aggiornare il manifesto dell'applicazione con le informazioni di compatibilità più recenti per il supporto del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="23c31-150">Update the application manifest with the latest Compatibility information for operating system support.</span></span> <span data-ttu-id="23c31-151">La sezione descrive le aggiunte al manifesto:</span><span class="sxs-lookup"><span data-stu-id="23c31-151">The section describes the additions to the manifest:</span></span>

-   <span data-ttu-id="23c31-152">**Spazio dei nomi:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span><span class="sxs-lookup"><span data-stu-id="23c31-152">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

-   <span data-ttu-id="23c31-153">**Nome sezione:** Compatibilità (nuova sezione)</span><span class="sxs-lookup"><span data-stu-id="23c31-153">**Section Name:** Compatibility (new section)</span></span>

-   <span data-ttu-id="23c31-154">**SupportedOS:** GUID del sistema operativo supportato: i GUID mappati ai sistemi operativi supportati sono:</span><span class="sxs-lookup"><span data-stu-id="23c31-154">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

    -   <span data-ttu-id="23c31-155">{e2011457-1546-43c5-a5fe-008dee3d3f0} per Windows Vista: questo è il valore predefinito per il contesto di switchback.</span><span class="sxs-lookup"><span data-stu-id="23c31-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} for Windows Vista: This is the default value for the switchback context.</span></span>
    -   <span data-ttu-id="23c31-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} per Windows 7: le applicazioni che impostano questo valore nel manifesto dell'applicazione ottengono il comportamento di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="23c31-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} for Windows 7: Applications that set this value in the application manifest get the Windows 7 behavior.</span></span>

    > [!Note]  
    > <span data-ttu-id="23c31-157">Microsoft genererà e inviare GUID per le versioni future di Windows in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="23c31-157">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

     

<span data-ttu-id="23c31-158">Di seguito è riportato un esempio di manifesto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="23c31-158">The following is an example of an updated manifest.</span></span>

> [!Note]  
> <span data-ttu-id="23c31-159">I nomi di attributo e tag nel manifesto dell'applicazione fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="23c31-159">The attribute and tag names in the application manifest are case sensitive.</span></span>

 


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



<span data-ttu-id="23c31-160">Il valore dell'aggiunta di GUID per entrambi i sistemi operativi nell'esempio precedente è fornire supporto di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="23c31-160">The value of adding GUIDs for both operating systems in the above example is to provide down-level support.</span></span> <span data-ttu-id="23c31-161">Le applicazioni che supportano entrambe le piattaforme non necessitano di manifesti separati per ogni piattaforma.</span><span class="sxs-lookup"><span data-stu-id="23c31-161">Applications that support both platforms would not need separate manifests for each platform.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="23c31-162">Test di compatibilità, prestazioni, affidabilità e usabilità</span><span class="sxs-lookup"><span data-stu-id="23c31-162">Compatibility, Performance, Reliability, and Usability Testing</span></span>

1.  <span data-ttu-id="23c31-163">Testare l'applicazione con la nuova sezione relativa alla compatibilità e assicurarsi che l'applicazione funzioni `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` correttamente usando il comportamento più recente di Windows 7</span><span class="sxs-lookup"><span data-stu-id="23c31-163">Test the application with the new compatibility section and `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` to ensure that the application works properly using the latest Windows 7 behavior</span></span>
2.  <span data-ttu-id="23c31-164">Testare l'applicazione con la nuova sezione di compatibilità e (o senza questa sezione) per assicurarsi che l'applicazione funzioni correttamente usando i comportamenti di `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` Windows Vista in Windows 7</span><span class="sxs-lookup"><span data-stu-id="23c31-164">Test the application with the new compatibility section and `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (or without this section entirely) to ensure that the application works properly using the Windows Vista behaviors on Windows 7</span></span>

## <a name="known-issues"></a><span data-ttu-id="23c31-165">Problemi noti</span><span class="sxs-lookup"><span data-stu-id="23c31-165">Known Issues</span></span>

<span data-ttu-id="23c31-166">**Mancata corrispondenza del contesto** Un'applicazione viene eseguita in un contesto di Windows Vista anziché in un contesto di Windows 7 in un computer che esegue un'edizione x64 di Windows 7 o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="23c31-166">**Context Mismatch** An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of either Windows 7 or Windows Server 2008 R2.</span></span>

<span data-ttu-id="23c31-167">**Soluzione** Sono disponibili aggiornamenti per risolvere questo problema per tutte le versioni supportate basate su x64 di Windows 7 e Windows Server 2008 R2, nonché per tutte le versioni supportate basate su Itanium di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="23c31-167">**Solution** Updates are available to correct this for all supported x64-based versions of Windows 7 and Windows Server 2008 R2, as well as for all supported Itanium-based versions of Windows Server 2008 R2.</span></span> <span data-ttu-id="23c31-168">Passare alla pagina Supporto tecnico Microsoft per KB 978637: un'applicazione viene eseguita in un contesto di Windows Vista anziché in un contesto di Windows 7 in un computer che esegue [un'edizione x64 di Windows 7 o Windows Server 2008 R2](https://support.microsoft.com/kb/978637) per altri dettagli e per scaricare la versione corretta per il sistema.</span><span class="sxs-lookup"><span data-stu-id="23c31-168">Go to the Microsoft Support page for [KB 978637: An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of Windows 7 or of Windows Server 2008 R2](https://support.microsoft.com/kb/978637) for additional details and to download the correct version for your system.</span></span>

<span data-ttu-id="23c31-169">**Diagnosi di dump di arresto anomalo del sistema bloccata**</span><span class="sxs-lookup"><span data-stu-id="23c31-169">**Crash dump diagnosis blocked**</span></span>

<span data-ttu-id="23c31-170">**Soluzione** Passare alla pagina Supporto tecnico Microsoft [kb 976038:](https://support.microsoft.com/kb/976038) le eccezioni generate da un'applicazione eseguita in una versione a 64 bit di Windows vengono ignorate per altri dettagli.</span><span class="sxs-lookup"><span data-stu-id="23c31-170">**Solution** Go to the Microsoft Support page for [KB 976038: Exceptions that are thrown from an application that runs in a 64-bit version of Windows are ignored](https://support.microsoft.com/kb/976038) for additional details.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="23c31-171">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="23c31-171">Links to Other Resources</span></span>

-   [<span data-ttu-id="23c31-172">**Funzione QueryActCtxW**</span><span class="sxs-lookup"><span data-stu-id="23c31-172">**QueryActCtxW Function**</span></span>](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   <span data-ttu-id="23c31-173">[Manifesto del controllo dell'account utente](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="23c31-173">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="23c31-174">Manifesti dell'applicazione per le applicazioni Windows</span><span class="sxs-lookup"><span data-stu-id="23c31-174">Application manifests for Windows applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="23c31-175">Gestione finestre desktop (DWM)</span><span class="sxs-lookup"><span data-stu-id="23c31-175">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="23c31-176">Aggiornamento della mancata corrispondenza del contesto</span><span class="sxs-lookup"><span data-stu-id="23c31-176">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)

 

 
