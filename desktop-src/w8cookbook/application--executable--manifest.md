---
title: Manifesto app (eseguibile)
description: Manifesto app (eseguibile)
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047489"
---
# <a name="app-executable-manifest"></a><span data-ttu-id="a9193-103">Manifesto app (eseguibile)</span><span class="sxs-lookup"><span data-stu-id="a9193-103">App (executable) manifest</span></span>

## <a name="platforms"></a><span data-ttu-id="a9193-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="a9193-104">Platforms</span></span>

<span data-ttu-id="a9193-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="a9193-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="a9193-106">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9193-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="a9193-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9193-107">Description</span></span>

<span data-ttu-id="a9193-108">La sezione relativa alla compatibilità del manifesto dell'app (eseguibile) introdotta in Windows consente al sistema operativo di determinare le versioni di Windows per cui è stata progettata la destinazione di un'app.</span><span class="sxs-lookup"><span data-stu-id="a9193-108">The compatibility section of the app (executable) manifest introduced in Windows helps the operating system determine the versions of Windows an app was designed to target.</span></span> <span data-ttu-id="a9193-109">Il manifesto dell'app consente inoltre a Windows di fornire il comportamento previsto dall'app in base alla versione di Windows di destinazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="a9193-109">Additionally, the app manifest enables Windows to provide the behavior that the app expects based on the version of Windows that the app targeted.</span></span>

<span data-ttu-id="a9193-110">La sezione compatibilità del manifesto consente a Windows di fornire nuovo comportamento al software appena creato, mantenendo al tempo stesso la compatibilità per il software esistente.</span><span class="sxs-lookup"><span data-stu-id="a9193-110">The compatibility section of the manifest allows Windows to provide new behavior to newly created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="a9193-111">Questa sezione aiuta Windows a offrire una maggiore compatibilità anche nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="a9193-111">This section helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="a9193-112">Ad esempio, un'app che dichiara il supporto per solo Windows 8 nella sezione compatibilità continuerà a ricevere il comportamento di Windows 8 nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="a9193-112">For example, an app declaring support for only Windows 8 in the compatibility section will continue to receive Windows 8 behavior in future versions of Windows.</span></span>

## <a name="manifestation"></a><span data-ttu-id="a9193-113">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="a9193-113">Manifestation</span></span>

<span data-ttu-id="a9193-114">Le app senza una sezione di compatibilità nel manifesto avranno il comportamento di Windows Vista per impostazione predefinita in Windows 7 e Windows 8 e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="a9193-114">Apps without a compatibility section in their manifest will have Windows Vista behavior by default on Windows 7 and Windows 8 and future Windows versions.</span></span> <span data-ttu-id="a9193-115">Tenere presente che Windows XP e Windows Vista ignorano questa sezione del manifesto e non hanno alcun effetto su di essi.</span><span class="sxs-lookup"><span data-stu-id="a9193-115">Be aware that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="a9193-116">Questi componenti di Windows forniscono un comportamento divergente basato sulla sezione compatibilità:</span><span class="sxs-lookup"><span data-stu-id="a9193-116">These Windows components provide divergent behavior based on the compatibility section:</span></span>

<span data-ttu-id="a9193-117">**Pool di thread predefinito RPC (Remote Procedure Call)**</span><span class="sxs-lookup"><span data-stu-id="a9193-117">**Remote procedure call (RPC) default thread pool**</span></span>

-   <span data-ttu-id="a9193-118">Windows 8 e Windows 7: per migliorare la scalabilità e ridurre i conteggi dei thread, RPC passa al pool di thread NT (pool predefinito).</span><span class="sxs-lookup"><span data-stu-id="a9193-118">Windows 8 and Windows 7: To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="a9193-119">Per Windows Vista, RPC usava un pool di thread privato:</span><span class="sxs-lookup"><span data-stu-id="a9193-119">For Windows Vista, RPC used a private thread pool:</span></span>

    -   <span data-ttu-id="a9193-120">Per i file binari compilati per Windows 7 e versioni successive di Windows, viene usato il pool predefinito.</span><span class="sxs-lookup"><span data-stu-id="a9193-120">For binaries compiled for Windows 7 and later versions of Windows, the default pool is used.</span></span>
    -   <span data-ttu-id="a9193-121">Se I \_ RpcMgmtEnableDedicatedThreadPool vengono chiamati prima della chiamata di qualsiasi API RPC, viene usato il pool di thread privati (comportamento di vista).</span><span class="sxs-lookup"><span data-stu-id="a9193-121">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior).</span></span>
    -   <span data-ttu-id="a9193-122">Se I \_ RpcMgmtEnableDedicatedThreadPool vengono chiamati dopo una chiamata RPC, viene usato il pool predefinito, \_ RpcMgmtEnableDedicatedThreadPool restituisce l'errore 1764 e l'operazione richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a9193-122">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported.</span></span>

-   <span data-ttu-id="a9193-123">Windows Vista (impostazione predefinita): per i file binari compilati per Windows Vista e le versioni precedenti di Windows, viene usato il pool privato.</span><span class="sxs-lookup"><span data-stu-id="a9193-123">Windows Vista (default): For binaries compiled for Windows Vista and earlier versions of Windows, the private pool is used.</span></span>

<span data-ttu-id="a9193-124">**Blocco DirectDraw**</span><span class="sxs-lookup"><span data-stu-id="a9193-124">**DirectDraw lock**</span></span>

-   <span data-ttu-id="a9193-125">Windows 8 e Windows 7: le app manifestate per Windows 7 e versioni successive del sistema operativo non possono chiamare l'API Lock in DDRAW per bloccare il buffer video del desktop primario. in questo modo si otterrà un errore e viene restituito un puntatore NULL per il database primario.</span><span class="sxs-lookup"><span data-stu-id="a9193-125">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of the operating system cannot call Lock API in DDRAW to lock the primary desktop video buffer; doing so will result in an error, and a NULL pointer for the primary is returned.</span></span> <span data-ttu-id="a9193-126">Questo comportamento viene applicato anche se Gestione finestre desktop composizione non è attivata.</span><span class="sxs-lookup"><span data-stu-id="a9193-126">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="a9193-127">Le app con compatibilità dichiarata per Windows 7 e versioni successive non devono bloccare il rendering del buffer video primario.</span><span class="sxs-lookup"><span data-stu-id="a9193-127">Apps with compatibility declared for Windows 7 and later must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="a9193-128">Windows Vista (impostazione predefinita): le app possono acquisire un blocco sul buffer video primario, perché le app legacy dipendono da questo comportamento. l'esecuzione dell'app disattiva Gestione finestre desktop.</span><span class="sxs-lookup"><span data-stu-id="a9193-128">Windows Vista (default): Apps can acquire a lock on the primary video buffer, as legacy apps depend on this behavior; running the app turns off Desktop Window Manager.</span></span>

<span data-ttu-id="a9193-129">**Trasferimento a blocchi di bit DirectDraw (BitBlt) a primario senza finestra di ridimensionamento**</span><span class="sxs-lookup"><span data-stu-id="a9193-129">**DirectDraw bit-block transfer (bitblt) to primary without clipping window**</span></span>

-   <span data-ttu-id="a9193-130">Windows 8 e Windows 7: le app manifestate per Windows 7 e versioni successive di Windows non possono eseguire un BitBlt al buffer video del desktop primario senza una finestra di ridimensionamento. in questo modo si verifica un errore e non viene eseguito il rendering dell'area BitBlt.</span><span class="sxs-lookup"><span data-stu-id="a9193-130">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of Windows are prevented from performing a bitblt to the primary Desktop video buffer without a clipping window; doing so results in an error and the bitblt area will not be rendered.</span></span> <span data-ttu-id="a9193-131">Windows applica questo comportamento anche se non si attiva Gestione finestre desktop composizione.</span><span class="sxs-lookup"><span data-stu-id="a9193-131">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="a9193-132">Le app con compatibilità dichiarata per Windows 7 e versioni successive devono eseguire un BitBlt in una finestra di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="a9193-132">Apps with compatibility declared for Windows 7 and later must perform a bitblt to a clipping window.</span></span>
-   <span data-ttu-id="a9193-133">Windows Vista (impostazione predefinita): le app devono essere in grado di eseguire un BitBlt nel database primario senza una finestra di ridimensionamento, perché le app legacy dipendono da questo comportamento. l'esecuzione di questa app disattiva la Gestione finestre desktop.</span><span class="sxs-lookup"><span data-stu-id="a9193-133">Windows Vista (default): Apps must be able to perform a bitblt to the primary without a clipping window, as legacy apps depend on this behavior; running this app turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="a9193-134">**API GetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="a9193-134">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="a9193-135">Windows 8 e Windows 7: risolve un race condition in cui un'app multithreading che usa **GetOverlappedResult** può restituire senza reimpostare l'evento nella struttura sovrapposta, causando la restituzione anticipata della chiamata successiva a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="a9193-135">Windows 8 and Windows 7: Resolves a race condition where a multithreaded app using **GetOverlappedResult** can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="a9193-136">Windows Vista (impostazione predefinita): fornisce il comportamento con il race condition cui le app possono avere una dipendenza.</span><span class="sxs-lookup"><span data-stu-id="a9193-136">Windows Vista (default): Provides the behavior with the race condition that apps might have a dependency on.</span></span> <span data-ttu-id="a9193-137">Le app che devono evitare questa corsa prima del comportamento di Windows 7 devono attendere l'evento sovrapposto e, quando segnalate, chiamare GetOverlappedResult con bWait = = FALSE.</span><span class="sxs-lookup"><span data-stu-id="a9193-137">Apps that must avoid this race prior to the Windows 7 behavior should wait on the overlapped event and, when signaled, call GetOverlappedResult with bWait == FALSE.</span></span>

<span data-ttu-id="a9193-138">**Stato temi Shell in modalità a contrasto elevato**</span><span class="sxs-lookup"><span data-stu-id="a9193-138">**Shell themes status in high contrast mode**</span></span>

-   <span data-ttu-id="a9193-139">Windows 8: restituisce lo stato del tema reale per in modalità a contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="a9193-139">Windows 8: Returns the real theming status for when in high contrast mode.</span></span>
-   <span data-ttu-id="a9193-140">Windows 7: i temi non sono disponibili quando si è in modalità a contrasto elevato perché DWM è ancora in funzione.</span><span class="sxs-lookup"><span data-stu-id="a9193-140">Windows 7: Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>
-   <span data-ttu-id="a9193-141">Windows Vista (impostazione predefinita): restituisce un tema non disponibile in modalità a contrasto elevato perché DWM è ancora acceso.</span><span class="sxs-lookup"><span data-stu-id="a9193-141">Windows Vista (default): Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>

<span data-ttu-id="a9193-142">**Metodo Shell iPersistFile:: Save**</span><span class="sxs-lookup"><span data-stu-id="a9193-142">**Shell iPersistFile::Save method**</span></span>

-   <span data-ttu-id="a9193-143">Windows 8: CShellLink:: Save ora determina se il gestore IPersistFile viene chiamato con un argomento di percorso relativo e non riesce a chiamare se è.</span><span class="sxs-lookup"><span data-stu-id="a9193-143">Windows 8: CShellLink::Save now determines if the IPersistFile handler is called with a relative path argument and fails the call if it is.</span></span>

    <span data-ttu-id="a9193-144">La [documentazione pubblica](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) che descrive questo comportamento indica che l'argomento path deve essere un percorso assoluto:</span><span class="sxs-lookup"><span data-stu-id="a9193-144">The [public documentation](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) describing this behavior indicates that path argument has to be an absolute path:</span></span>

-   <span data-ttu-id="a9193-145">Windows 7 e versioni precedenti (impostazione predefinita): CShellLink:: Save non determina se il gestore iPersistFile Invia un controllo del percorso relativo e consente alle app di continuare a usare percorsi assoluti o relativi.</span><span class="sxs-lookup"><span data-stu-id="a9193-145">Windows 7 and earlier (default): CShellLink::Save does not determine if the iPersistFile handler sends a relative path check and allows apps to continue working with absolute or relative paths.</span></span>

<span data-ttu-id="a9193-146">**Assistente compatibilità programmi (PCA)**</span><span class="sxs-lookup"><span data-stu-id="a9193-146">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="a9193-147">Windows 8: le app con la sezione compatibilità non ottengono la mitigazione PCA.</span><span class="sxs-lookup"><span data-stu-id="a9193-147">Windows 8: Apps with the compatibility section do not get the PCA mitigation.</span></span>
-   <span data-ttu-id="a9193-148">Windows 7: le app con la sezione compatibilità vengono registrate per i potenziali problemi di compatibilità per le modifiche apportate a Windows 8 (descritte in questo documento).</span><span class="sxs-lookup"><span data-stu-id="a9193-148">Windows 7: Apps with the compatibility section are tracked for potential compatibility issues for Windows 8 changes (described in this document).</span></span>
-   <span data-ttu-id="a9193-149">Windows Vista (impostazione predefinita): le app che non vengono installate correttamente o arrestano in modo anomalo in fase di esecuzione in alcune circostanze specifiche ottengono la mitigazione PCA.</span><span class="sxs-lookup"><span data-stu-id="a9193-149">Windows Vista (default): Apps that fail to install properly or crash during runtime under some specific circumstances get the PCA mitigation.</span></span> <span data-ttu-id="a9193-150">Per altre informazioni, vedere la sezione Resources (risorse).</span><span class="sxs-lookup"><span data-stu-id="a9193-150">For more info, see the Resources section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="a9193-151">Sfruttando le funzionalità</span><span class="sxs-lookup"><span data-stu-id="a9193-151">Leveraging feature capabilities</span></span>

<span data-ttu-id="a9193-152">Aggiornare il manifesto dell'applicazione con le ultime informazioni sulla compatibilità per il supporto del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a9193-152">Update the app manifest with the latest compatibility info for operating system support.</span></span> <span data-ttu-id="a9193-153">In questa sezione vengono descritte le aggiunte al manifesto:</span><span class="sxs-lookup"><span data-stu-id="a9193-153">This section describes the additions to the manifest:</span></span>

<span data-ttu-id="a9193-154">**Spazio dei nomi:** Compatibility. V1 (xmlns = "urn: schemas-microsoft-com: Compatibility. V1" >)</span><span class="sxs-lookup"><span data-stu-id="a9193-154">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

<span data-ttu-id="a9193-155">**Nome della sezione:** Compatibilità (nuova sezione)</span><span class="sxs-lookup"><span data-stu-id="a9193-155">**Section name:** Compatibility (new section)</span></span>

<span data-ttu-id="a9193-156">**Supportato:** GUID del sistema operativo supportato: i GUID che eseguono il mapping ai sistemi operativi supportati sono:</span><span class="sxs-lookup"><span data-stu-id="a9193-156">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

-   <span data-ttu-id="a9193-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="a9193-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span>

    <span data-ttu-id="a9193-158">per **Windows Vista**: si tratta del valore predefinito per il contesto Switchback</span><span class="sxs-lookup"><span data-stu-id="a9193-158">for **Windows Vista**: This is the default value for the switchback context</span></span>

-   <span data-ttu-id="a9193-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span><span class="sxs-lookup"><span data-stu-id="a9193-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span>

    <span data-ttu-id="a9193-160">per **Windows 7**: le app che impostano questo valore nel manifesto dell'app ottengono il comportamento di Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9193-160">for **Windows 7**: Apps that set this value in the app manifest get the Windows 7 behavior</span></span>

-   <span data-ttu-id="a9193-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="a9193-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span>

    <span data-ttu-id="a9193-162">per **Windows 8**: le app che impostano questo valore nel manifesto dell'applicazione ottengono il comportamento di Windows 8</span><span class="sxs-lookup"><span data-stu-id="a9193-162">for **Windows 8**: Apps that set this value in the application manifest get the Windows 8 behavior</span></span>

<span data-ttu-id="a9193-163">Microsoft genererà e pubblicherà i GUID per le versioni future di Windows in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="a9193-163">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

<span data-ttu-id="a9193-164">Esempio XML di un manifesto aggiornato:</span><span class="sxs-lookup"><span data-stu-id="a9193-164">An XML example of an updated manifest:</span></span>

> [!Note]  
> <span data-ttu-id="a9193-165">I nomi di attributo e tag nel manifesto dell'applicazione fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a9193-165">The attribute and tag names in the app manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



<span data-ttu-id="a9193-166">I GUID per tutti i sistemi operativi nell'esempio precedente forniscono supporto di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="a9193-166">The GUIDs for all the operating systems in the previous example provide down-level support.</span></span> <span data-ttu-id="a9193-167">Le app che supportano più piattaforme non necessitano di manifesti distinti per ogni piattaforma.</span><span class="sxs-lookup"><span data-stu-id="a9193-167">Apps that support multiple platforms do not need separate manifests for each platform.</span></span>

## <a name="tests"></a><span data-ttu-id="a9193-168">Test</span><span class="sxs-lookup"><span data-stu-id="a9193-168">Tests</span></span>

<span data-ttu-id="a9193-169">Un'app può specificare più ID del sistema operativo supportati.</span><span class="sxs-lookup"><span data-stu-id="a9193-169">An app can specify multiple supported operating system IDs.</span></span> <span data-ttu-id="a9193-170">È necessario aggiungere un ID sistema operativo supportato se è stato testato o si sta eseguendo il test dell'app nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a9193-170">You should add a supported operating system ID if you have tested, or are in the process of testing, the app on that operating system.</span></span> <span data-ttu-id="a9193-171">Windows Vista e le versioni precedenti del sistema operativo non prestano attenzione a queste voci.</span><span class="sxs-lookup"><span data-stu-id="a9193-171">Windows Vista and prior operating system versions do not pay attention to these entries.</span></span> <span data-ttu-id="a9193-172">A partire da Windows 7, Windows sceglierà il GUID della versione più recente nel manifesto fino alla versione di Windows in esecuzione e fornirà il supporto dell'app a tale livello.</span><span class="sxs-lookup"><span data-stu-id="a9193-172">Starting with Windows 7, Windows will choose the highest version GUID in the manifest up to the running Windows version, and give the app support at that level.</span></span> <span data-ttu-id="a9193-173">Per verificare che l'app funzioni con la nuova sezione compatibilità del manifesto dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="a9193-173">To verify that the app works with the new app manifest compatibility section:</span></span>

1.  <span data-ttu-id="a9193-174">Testare l'app con la nuova sezione relativa alla compatibilità e ID supportati = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} per assicurarsi che l'app funzioni correttamente usando il comportamento più recente di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a9193-174">Test the app with the new compatibility section and SupportedOS ID = { 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} to ensure that the app works properly using the latest Windows 8 behavior.</span></span>
2.  <span data-ttu-id="a9193-175">Testare l'app con la nuova sezione relativa alla compatibilità e ID supportati = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} per assicurarsi che l'app funzioni correttamente usando il comportamento di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a9193-175">Test the app with the new compatibility section and SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} to ensure that the app works properly using the Windows 7 behavior.</span></span>
3.  <span data-ttu-id="a9193-176">Testare l'app con la nuova sezione relativa alla compatibilità e ID supportati = {e2011457-1546-43C5-a5fe-008deee3d3f0} per assicurarsi che l'app funzioni correttamente usando il comportamento di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a9193-176">Test the app with the new compatibility section and SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0} to ensure that the app works properly using the Windows Vista behavior.</span></span>

## <a name="resources"></a><span data-ttu-id="a9193-177">Risorse</span><span class="sxs-lookup"><span data-stu-id="a9193-177">Resources</span></span>

-   [<span data-ttu-id="a9193-178">QueryActCtxW (funzione)</span><span class="sxs-lookup"><span data-stu-id="a9193-178">QueryActCtxW Function</span></span>](../sbscs/application-manifests.md)
-   <span data-ttu-id="a9193-179">[Manifesto UAC](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a9193-179">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="a9193-180">Manifesti dell'applicazione per applicazioni Windows</span><span class="sxs-lookup"><span data-stu-id="a9193-180">Application Manifests for Windows Applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="a9193-181">Gestione finestre desktop (DWM)</span><span class="sxs-lookup"><span data-stu-id="a9193-181">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="a9193-182">Aggiornamento del contesto non corrispondente</span><span class="sxs-lookup"><span data-stu-id="a9193-182">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)
-   <span data-ttu-id="a9193-183">[Assistente compatibilità programmi](/previous-versions/bb756937(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a9193-183">[Program Compatibility Assistant](/previous-versions/bb756937(v=msdn.10))</span></span>

 

 