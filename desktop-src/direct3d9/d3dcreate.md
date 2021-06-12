---
description: Vedere una combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo nella costante D3DCREATE.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c24529c725b8b7c7f71c53718d56ceb50603
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011284"
---
# <a name="d3dcreate"></a><span data-ttu-id="fa452-103">D3DCREATE</span><span class="sxs-lookup"><span data-stu-id="fa452-103">D3DCREATE</span></span>

<span data-ttu-id="fa452-104">Combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa452-104">A combination of one or more flags that control the device create behavior.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa452-105">#Definire</span><span class="sxs-lookup"><span data-stu-id="fa452-105">#define</span></span></td>
<td><span data-ttu-id="fa452-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa452-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa452-107">D3DCREATE_ADAPTERGROUP_DEVICE</span><span class="sxs-lookup"><span data-stu-id="fa452-107">D3DCREATE_ADAPTERGROUP_DEVICE</span></span></td>
<td><span data-ttu-id="fa452-108">L'applicazione chiede al dispositivo di guidare tutte le teste di proprietà dell'adattatore master.</span><span class="sxs-lookup"><span data-stu-id="fa452-108">Application asks the device to drive all the heads that this master adapter owns.</span></span> <span data-ttu-id="fa452-109">Il flag non è valido per gli adattatori non master.</span><span class="sxs-lookup"><span data-stu-id="fa452-109">The flag is illegal on nonmaster adapters.</span></span> <span data-ttu-id="fa452-110">Se questo flag è impostato, i parametri di presentazione passati a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> devono puntare a una matrice <a href="d3dpresent-parameters.md"><strong>di</strong></a>D3DPRESENT_PARAMETERS .</span><span class="sxs-lookup"><span data-stu-id="fa452-110">If this flag is set, the presentation parameters passed to <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> should point to an array of <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span></span> <span data-ttu-id="fa452-111">Il numero di elementi in <strong>D3DPRESENT_PARAMETERS</strong> deve essere uguale al numero di adattatori definiti dal membro NumberOfAdaptersInGroup della struttura <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9.</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa452-111">The number of elements in <strong>D3DPRESENT_PARAMETERS</strong> should equal the number of adapters defined by the NumberOfAdaptersInGroup member of the <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> structure.</span></span> <span data-ttu-id="fa452-112">Il runtime DirectX assegna ogni elemento a ogni head nell'ordine numerico specificato dal membro AdapterOrdinalInGroup <strong>di D3DCAPS9.</strong></span><span class="sxs-lookup"><span data-stu-id="fa452-112">The DirectX runtime will assign each element to each head in the numerical order specified by the AdapterOrdinalInGroup member of <strong>D3DCAPS9</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa452-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="fa452-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span></span></td>
<td><span data-ttu-id="fa452-114">Direct3D gestirà le risorse anziché il driver.</span><span class="sxs-lookup"><span data-stu-id="fa452-114">Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="fa452-115">Le chiamate Direct3D non avranno esito negativo per errori delle risorse, ad esempio memoria video insufficiente.</span><span class="sxs-lookup"><span data-stu-id="fa452-115">Direct3D calls will not fail for resource errors such as insufficient video memory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa452-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span><span class="sxs-lookup"><span data-stu-id="fa452-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span></span></td>
<td><span data-ttu-id="fa452-117">Come D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D gestirà le risorse anziché il driver.</span><span class="sxs-lookup"><span data-stu-id="fa452-117">Like D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="fa452-118">A D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX restituirà errori per condizioni come memoria video insufficiente.</span><span class="sxs-lookup"><span data-stu-id="fa452-118">Unlike D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX will return errors for conditions such as insufficient video memory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa452-119">D3DCREATE_DISABLE_PRINTSCREEN</span><span class="sxs-lookup"><span data-stu-id="fa452-119">D3DCREATE_DISABLE_PRINTSCREEN</span></span></td>
<td><span data-ttu-id="fa452-120">Fa in modo che il runtime non registri i tasti di scelta rapida per Printscreen, Ctrl-Printscreen e Alt-Printscreen per acquisire il contenuto del desktop o della finestra.</span><span class="sxs-lookup"><span data-stu-id="fa452-120">Causes the runtime not register hotkeys for Printscreen, Ctrl-Printscreen and Alt-Printscreen to capture the desktop or window content.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa452-121">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="fa452-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="fa452-122">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="fa452-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa452-123">D3DCREATE_DISABLE_PSGP_THREADING</span><span class="sxs-lookup"><span data-stu-id="fa452-123">D3DCREATE_DISABLE_PSGP_THREADING</span></span></td>
<td><span data-ttu-id="fa452-124">Limitare il calcolo al thread principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fa452-124">Restrict computation to the main application thread.</span></span> <span data-ttu-id="fa452-125">Se il flag non è impostato, il runtime può eseguire l'elaborazione dei vertici software e altri calcoli nel thread di lavoro per migliorare le prestazioni nei sistemi a più processori.</span><span class="sxs-lookup"><span data-stu-id="fa452-125">If the flag is not set, the runtime may perform software vertex processing and other computations in worker thread to improve performance on multi-processor systems.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa452-126">Differenze tra Windows XP e Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="fa452-126">Differences between Windows XP and Windows Vista:</span></span><br/> <span data-ttu-id="fa452-127">Questo flag è disponibile in Windows Vista, Windows Server 2008 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fa452-127">This flag is available on Windows Vista, Windows Server 2008, and Windows 7.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa452-128">D3DCREATE_ENABLE_PRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="fa452-128">D3DCREATE_ENABLE_PRESENTSTATS</span></span></td>
<td><span data-ttu-id="fa452-129">Abilita la raccolta delle statistiche presenti nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa452-129">Enables the gathering of present statistics on the device.</span></span> <span data-ttu-id="fa452-130">Le chiamate <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>a GetPresentStatistics</strong></a> restituiscono dati validi.</span><span class="sxs-lookup"><span data-stu-id="fa452-130">Calls to <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> will return valid data.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa452-131">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="fa452-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="fa452-132">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="fa452-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa452-133">D3DCREATE_FPU_PRESERVE</span><span class="sxs-lookup"><span data-stu-id="fa452-133">D3DCREATE_FPU_PRESERVE</span></span></td>
<td><span data-ttu-id="fa452-134">Impostare la precisione per i calcoli a virgola mobile Direct3D sulla precisione usata dal thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="fa452-134">Set the precision for Direct3D floating-point calculations to the precision used by the calling thread.</span></span> <span data-ttu-id="fa452-135">Se non si specifica questo flag, direct3D viene impostato per impostazione predefinita sulla modalità round-to-nearest a precisione singola per due motivi:</span><span class="sxs-lookup"><span data-stu-id="fa452-135">If you do not specify this flag, Direct3D defaults to single-precision round-to-nearest mode for two reasons:</span></span>
<ul>
<li><span data-ttu-id="fa452-136">La modalità a precisione doppia ridurrà le prestazioni direct3D.</span><span class="sxs-lookup"><span data-stu-id="fa452-136">Double-precision mode will reduce Direct3D performance.</span></span></li>
<li><span data-ttu-id="fa452-137">Parti di Direct3D presuppongono che le eccezioni di unità a virgola mobile siano mascherate; L'annullamento del mascheramento di queste eccezioni può comportare un comportamento non definito.</span><span class="sxs-lookup"><span data-stu-id="fa452-137">Portions of Direct3D assume floating-point unit exceptions are masked; unmasking these exceptions may result in undefined behavior.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa452-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="fa452-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="fa452-139">Specifica l'elaborazione dei vertici hardware.</span><span class="sxs-lookup"><span data-stu-id="fa452-139">Specifies hardware vertex processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa452-140">D3DCREATE_MIXED_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="fa452-140">D3DCREATE_MIXED_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="fa452-141">Specifica l'elaborazione mista dei vertici (software e hardware).</span><span class="sxs-lookup"><span data-stu-id="fa452-141">Specifies mixed (both software and hardware) vertex processing.</span></span> <span data-ttu-id="fa452-142">Per Windows 10 versione 1607 e successive, non è consigliabile usare questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="fa452-142">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="fa452-143">Vedere D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="fa452-143">See D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa452-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="fa452-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="fa452-145">Specifica l'elaborazione dei vertici software.</span><span class="sxs-lookup"><span data-stu-id="fa452-145">Specifies software vertex processing.</span></span> <span data-ttu-id="fa452-146">Per Windows 10 versione 1607 e successive, non è consigliabile usare questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="fa452-146">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="fa452-147">Usare D3DCREATE_HARDWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="fa452-147">Use D3DCREATE_HARDWARE_VERTEXPROCESSING.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="fa452-148">A meno che l'elaborazione dei vertici hardware non sia disponibile, l'utilizzo dell'elaborazione dei vertici software non è consigliato in Windows 10, versione 1607 (e versioni successive) perché l'efficienza dell'elaborazione dei vertici software è stata notevolmente ridotta, migliorando al tempo stesso la sicurezza dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="fa452-148">Unless hardware vertex processing is not available, the usage of software vertex processing is not recommended in Windows 10, version 1607 (and later versions) because the efficiency of software vertex processing was significantly reduced while improving the security of the implementation.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa452-149">D3DCREATE_MULTITHREADED</span><span class="sxs-lookup"><span data-stu-id="fa452-149">D3DCREATE_MULTITHREADED</span></span></td>
<td><span data-ttu-id="fa452-150">Indica che l'applicazione richiede che Direct3D sia protetto da multithreading.</span><span class="sxs-lookup"><span data-stu-id="fa452-150">Indicates that the application requests Direct3D to be multithread safe.</span></span> <span data-ttu-id="fa452-151">In questo modo un thread Direct3D diventa più frequentemente proprietario della sezione critica <a href="/windows/desktop/Sync/critical-section-objects">globale,</a> con un possibile peggioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="fa452-151">This makes a Direct3D thread take ownership of its global <a href="/windows/desktop/Sync/critical-section-objects">critical section</a> more frequently, which can degrade performance.</span></span> <span data-ttu-id="fa452-152">Se un'applicazione elabora messaggi di finestra in un thread durante l'esecuzione di chiamate api Direct3D in un altro, l'applicazione deve usare questo flag durante la creazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa452-152">If an application processes window messages in one thread while making Direct3D API calls in another, the application must use this flag when creating the device.</span></span> <span data-ttu-id="fa452-153">Questa finestra deve essere anche distrutta prima di scaricare d3d9.dll.</span><span class="sxs-lookup"><span data-stu-id="fa452-153">This window must also be destroyed before unloading d3d9.dll.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa452-154">D3DCREATE_NOWINDOWCHANGES</span><span class="sxs-lookup"><span data-stu-id="fa452-154">D3DCREATE_NOWINDOWCHANGES</span></span></td>
<td><span data-ttu-id="fa452-155">Indica che Direct3D non deve modificare in alcun modo la finestra dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="fa452-155">Indicates that Direct3D must not alter the focus window in any way.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="fa452-156">Se questo flag è impostato, l'applicazione deve supportare completamente tutti gli eventi di gestione dello stato attivo, ad esempio ALT+TAB e gli eventi clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="fa452-156">If this flag is set, the application must fully support all focus management events, such as ALT+TAB and mouse click events.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa452-157">D3DCREATE_PUREDEVICE</span><span class="sxs-lookup"><span data-stu-id="fa452-157">D3DCREATE_PUREDEVICE</span></span></td>
<td><span data-ttu-id="fa452-158">Specifica che Direct3D non supporta chiamate Get\* per qualsiasi elemento che può essere archiviato in blocchi di stato.</span><span class="sxs-lookup"><span data-stu-id="fa452-158">Specifies that Direct3D does not support Get\* calls for anything that can be stored in state blocks.</span></span> <span data-ttu-id="fa452-159">Indica inoltre a Direct3D di non fornire servizi di emulazione per l'elaborazione dei vertici.</span><span class="sxs-lookup"><span data-stu-id="fa452-159">It also tells Direct3D not to provide any emulation services for vertex processing.</span></span> <span data-ttu-id="fa452-160">Ciò significa che se il dispositivo non supporta l'elaborazione dei vertici, l'applicazione può usare solo vertici post-trasformati.</span><span class="sxs-lookup"><span data-stu-id="fa452-160">This means that if the device does not support vertex processing, then the application can use only post-transformed vertices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa452-161">D3DCREATE_SCREENSAVER</span><span class="sxs-lookup"><span data-stu-id="fa452-161">D3DCREATE_SCREENSAVER</span></span></td>
<td><span data-ttu-id="fa452-162">Consente gli screensaver durante un'applicazione a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="fa452-162">Allows screensavers during a fullscreen application.</span></span> <span data-ttu-id="fa452-163">Senza questo flag, Direct3D disabilita gli screensaver per tutto il tempo in cui l'applicazione chiamante è a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="fa452-163">Without this flag, Direct3D will disable screensavers for as long as the calling application is fullscreen.</span></span> <span data-ttu-id="fa452-164">Se l'applicazione chiamante è già uno screensaver, questo flag non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="fa452-164">If the calling application is already a screensaver, this flag has no effect.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa452-165">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="fa452-165">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="fa452-166">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="fa452-166">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fa452-167">D3DCREATE \_ HARDWARE \_ VERTEXPROCESSING, D3DCREATE \_ MIXED \_ VERTEXPROCESSING e D3DCREATE SOFTWARE VERTEXPROCESSING sono flag che si \_ \_ escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="fa452-167">D3DCREATE\_HARDWARE\_VERTEXPROCESSING, D3DCREATE\_MIXED\_VERTEXPROCESSING, and D3DCREATE\_SOFTWARE\_VERTEXPROCESSING are mutually exclusive flags.</span></span> <span data-ttu-id="fa452-168">Quando si chiama [**CreateDevice,**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)è necessario specificare almeno uno di questi flag di elaborazione dei vertici.</span><span class="sxs-lookup"><span data-stu-id="fa452-168">At least one of these vertex processing flags must be specified when calling [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span>

## <a name="constant-information"></a><span data-ttu-id="fa452-169">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="fa452-169">Constant Information</span></span>



| <span data-ttu-id="fa452-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa452-170">Requirement</span></span>                         |  <span data-ttu-id="fa452-171">Valore</span><span class="sxs-lookup"><span data-stu-id="fa452-171">Value</span></span>          |
|--------------------------|------------|
| <span data-ttu-id="fa452-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa452-172">Header</span></span>                   | <span data-ttu-id="fa452-173">D3D9.h</span><span class="sxs-lookup"><span data-stu-id="fa452-173">D3D9.h</span></span>     |
| <span data-ttu-id="fa452-174">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="fa452-174">Minimum operating system</span></span> | <span data-ttu-id="fa452-175">Windows 98</span><span class="sxs-lookup"><span data-stu-id="fa452-175">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fa452-176">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa452-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa452-177">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="fa452-177">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
