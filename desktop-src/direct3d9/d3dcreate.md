---
description: Combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14de345d6cb6d164ee5cd3067e1f38ff66d9795d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966239"
---
# <a name="d3dcreate"></a><span data-ttu-id="37a5d-103">D3DCREATE</span><span class="sxs-lookup"><span data-stu-id="37a5d-103">D3DCREATE</span></span>

<span data-ttu-id="37a5d-104">Combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37a5d-104">A combination of one or more flags that control the device create behavior.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a5d-105">#definire</span><span class="sxs-lookup"><span data-stu-id="37a5d-105">#define</span></span></td>
<td><span data-ttu-id="37a5d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37a5d-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a5d-107">D3DCREATE_ADAPTERGROUP_DEVICE</span><span class="sxs-lookup"><span data-stu-id="37a5d-107">D3DCREATE_ADAPTERGROUP_DEVICE</span></span></td>
<td><span data-ttu-id="37a5d-108">L'applicazione chiede al dispositivo di guidare tutte le intestazioni di proprietà dell'adapter master.</span><span class="sxs-lookup"><span data-stu-id="37a5d-108">Application asks the device to drive all the heads that this master adapter owns.</span></span> <span data-ttu-id="37a5d-109">Il flag non è valido per gli adapter non master.</span><span class="sxs-lookup"><span data-stu-id="37a5d-109">The flag is illegal on nonmaster adapters.</span></span> <span data-ttu-id="37a5d-110">Se questo flag è impostato, i parametri di presentazione passati a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> devono puntare a una matrice di <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37a5d-110">If this flag is set, the presentation parameters passed to <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> should point to an array of <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span></span> <span data-ttu-id="37a5d-111">Il numero di elementi in <strong>D3DPRESENT_PARAMETERS</strong> deve essere uguale al numero di schede definito dal membro NumberOfAdaptersInGroup della struttura <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="37a5d-111">The number of elements in <strong>D3DPRESENT_PARAMETERS</strong> should equal the number of adapters defined by the NumberOfAdaptersInGroup member of the <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> structure.</span></span> <span data-ttu-id="37a5d-112">Il runtime di DirectX assegnerà ogni elemento a ogni intestazione nell'ordine numerico specificato dal membro AdapterOrdinalInGroup di <strong>D3DCAPS9</strong>.</span><span class="sxs-lookup"><span data-stu-id="37a5d-112">The DirectX runtime will assign each element to each head in the numerical order specified by the AdapterOrdinalInGroup member of <strong>D3DCAPS9</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a5d-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="37a5d-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span></span></td>
<td><span data-ttu-id="37a5d-114">Direct3D gestirà le risorse al posto del driver.</span><span class="sxs-lookup"><span data-stu-id="37a5d-114">Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="37a5d-115">Le chiamate Direct3D non avranno esito negativo per errori di risorse, ad esempio memoria video insufficiente.</span><span class="sxs-lookup"><span data-stu-id="37a5d-115">Direct3D calls will not fail for resource errors such as insufficient video memory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a5d-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span><span class="sxs-lookup"><span data-stu-id="37a5d-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span></span></td>
<td><span data-ttu-id="37a5d-117">Come D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D gestirà le risorse al posto del driver.</span><span class="sxs-lookup"><span data-stu-id="37a5d-117">Like D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="37a5d-118">A differenza di D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX restituirà errori per le condizioni, ad esempio la memoria video insufficiente.</span><span class="sxs-lookup"><span data-stu-id="37a5d-118">Unlike D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX will return errors for conditions such as insufficient video memory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a5d-119">D3DCREATE_DISABLE_PRINTSCREEN</span><span class="sxs-lookup"><span data-stu-id="37a5d-119">D3DCREATE_DISABLE_PRINTSCREEN</span></span></td>
<td><span data-ttu-id="37a5d-120">Fa in modo che il runtime non registri i tasti di scelta rapida per printscreen, Ctrl-Printscreen e Alt-Printscreen per acquisire il contenuto del desktop o della finestra.</span><span class="sxs-lookup"><span data-stu-id="37a5d-120">Causes the runtime not register hotkeys for Printscreen, Ctrl-Printscreen and Alt-Printscreen to capture the desktop or window content.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a5d-121">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="37a5d-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="37a5d-122">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="37a5d-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a5d-123">D3DCREATE_DISABLE_PSGP_THREADING</span><span class="sxs-lookup"><span data-stu-id="37a5d-123">D3DCREATE_DISABLE_PSGP_THREADING</span></span></td>
<td><span data-ttu-id="37a5d-124">Limitare il calcolo al thread principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="37a5d-124">Restrict computation to the main application thread.</span></span> <span data-ttu-id="37a5d-125">Se il flag non è impostato, il runtime può eseguire l'elaborazione dei vertici software e altri calcoli nel thread di lavoro per migliorare le prestazioni nei sistemi a più processori.</span><span class="sxs-lookup"><span data-stu-id="37a5d-125">If the flag is not set, the runtime may perform software vertex processing and other computations in worker thread to improve performance on multi-processor systems.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a5d-126">Differenze tra Windows XP e Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="37a5d-126">Differences between Windows XP and Windows Vista:</span></span><br/> <span data-ttu-id="37a5d-127">Questo flag è disponibile in Windows Vista, Windows Server 2008 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="37a5d-127">This flag is available on Windows Vista, Windows Server 2008, and Windows 7.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a5d-128">D3DCREATE_ENABLE_PRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="37a5d-128">D3DCREATE_ENABLE_PRESENTSTATS</span></span></td>
<td><span data-ttu-id="37a5d-129">Consente la raccolta di statistiche presenti sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37a5d-129">Enables the gathering of present statistics on the device.</span></span> <span data-ttu-id="37a5d-130">Le chiamate a <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> restituiranno dati validi.</span><span class="sxs-lookup"><span data-stu-id="37a5d-130">Calls to <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> will return valid data.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a5d-131">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="37a5d-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="37a5d-132">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="37a5d-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a5d-133">D3DCREATE_FPU_PRESERVE</span><span class="sxs-lookup"><span data-stu-id="37a5d-133">D3DCREATE_FPU_PRESERVE</span></span></td>
<td><span data-ttu-id="37a5d-134">Impostare la precisione per i calcoli a virgola mobile Direct3D sulla precisione usata dal thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="37a5d-134">Set the precision for Direct3D floating-point calculations to the precision used by the calling thread.</span></span> <span data-ttu-id="37a5d-135">Se non si specifica questo flag, Direct3D esegue per impostazione predefinita la modalità round-to-precisione singola per due motivi:</span><span class="sxs-lookup"><span data-stu-id="37a5d-135">If you do not specify this flag, Direct3D defaults to single-precision round-to-nearest mode for two reasons:</span></span>
<ul>
<li><span data-ttu-id="37a5d-136">La modalità a precisione doppia ridurrà le prestazioni di Direct3D.</span><span class="sxs-lookup"><span data-stu-id="37a5d-136">Double-precision mode will reduce Direct3D performance.</span></span></li>
<li><span data-ttu-id="37a5d-137">Parti di Direct3D presupporre che le eccezioni di unità a virgola mobile siano mascherate; annullare il mascheramento di queste eccezioni può causare un comportamento indefinito.</span><span class="sxs-lookup"><span data-stu-id="37a5d-137">Portions of Direct3D assume floating-point unit exceptions are masked; unmasking these exceptions may result in undefined behavior.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a5d-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="37a5d-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="37a5d-139">Specifica l'elaborazione del vertice hardware.</span><span class="sxs-lookup"><span data-stu-id="37a5d-139">Specifies hardware vertex processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a5d-140">D3DCREATE_MIXED_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="37a5d-140">D3DCREATE_MIXED_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="37a5d-141">Specifica l'elaborazione del vertice mista (software e hardware).</span><span class="sxs-lookup"><span data-stu-id="37a5d-141">Specifies mixed (both software and hardware) vertex processing.</span></span> <span data-ttu-id="37a5d-142">Per Windows 10, versione 1607 e successive, non è consigliabile usare questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="37a5d-142">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="37a5d-143">Vedere D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="37a5d-143">See D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a5d-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="37a5d-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="37a5d-145">Specifica l'elaborazione dei vertici software.</span><span class="sxs-lookup"><span data-stu-id="37a5d-145">Specifies software vertex processing.</span></span> <span data-ttu-id="37a5d-146">Per Windows 10, versione 1607 e successive, non è consigliabile usare questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="37a5d-146">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="37a5d-147">Usare D3DCREATE_HARDWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="37a5d-147">Use D3DCREATE_HARDWARE_VERTEXPROCESSING.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a5d-148">A meno che l'elaborazione dei vertici hardware non sia disponibile, l'utilizzo dell'elaborazione dei vertici software non è consigliato in Windows 10, versione 1607 (e versioni successive) perché l'efficienza dell'elaborazione dei vertici software è stata notevolmente ridotta migliorando la sicurezza dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="37a5d-148">Unless hardware vertex processing is not available, the usage of software vertex processing is not recommended in Windows 10, version 1607 (and later versions) because the efficiency of software vertex processing was significantly reduced while improving the security of the implementation.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a5d-149">D3DCREATE_MULTITHREADED</span><span class="sxs-lookup"><span data-stu-id="37a5d-149">D3DCREATE_MULTITHREADED</span></span></td>
<td><span data-ttu-id="37a5d-150">Indica che l'applicazione richiede che Direct3D sia multithread safe.</span><span class="sxs-lookup"><span data-stu-id="37a5d-150">Indicates that the application requests Direct3D to be multithread safe.</span></span> <span data-ttu-id="37a5d-151">In questo modo un thread Direct3D assume la proprietà della <a href="/windows/desktop/Sync/critical-section-objects">sezione critica</a> globale con maggiore frequenza, che può influire negativamente sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="37a5d-151">This makes a Direct3D thread take ownership of its global <a href="/windows/desktop/Sync/critical-section-objects">critical section</a> more frequently, which can degrade performance.</span></span> <span data-ttu-id="37a5d-152">Se un'applicazione elabora i messaggi della finestra in un thread durante l'esecuzione di chiamate API Direct3D in un altro thread, l'applicazione deve usare questo flag durante la creazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37a5d-152">If an application processes window messages in one thread while making Direct3D API calls in another, the application must use this flag when creating the device.</span></span> <span data-ttu-id="37a5d-153">Questa finestra deve anche essere eliminata prima di scaricare d3d9.dll.</span><span class="sxs-lookup"><span data-stu-id="37a5d-153">This window must also be destroyed before unloading d3d9.dll.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a5d-154">D3DCREATE_NOWINDOWCHANGES</span><span class="sxs-lookup"><span data-stu-id="37a5d-154">D3DCREATE_NOWINDOWCHANGES</span></span></td>
<td><span data-ttu-id="37a5d-155">Indica che Direct3D non deve modificare la finestra di stato attivo in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="37a5d-155">Indicates that Direct3D must not alter the focus window in any way.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="37a5d-156">Se questo flag è impostato, l'applicazione deve supportare completamente tutti gli eventi di gestione dello stato attivo, ad esempio gli eventi ALT + TAB e clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="37a5d-156">If this flag is set, the application must fully support all focus management events, such as ALT+TAB and mouse click events.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37a5d-157">D3DCREATE_PUREDEVICE</span><span class="sxs-lookup"><span data-stu-id="37a5d-157">D3DCREATE_PUREDEVICE</span></span></td>
<td><span data-ttu-id="37a5d-158">Specifica che Direct3D non supporta le chiamate Get \* per qualsiasi elemento che può essere archiviato nei blocchi di stato.</span><span class="sxs-lookup"><span data-stu-id="37a5d-158">Specifies that Direct3D does not support Get\* calls for anything that can be stored in state blocks.</span></span> <span data-ttu-id="37a5d-159">Indica inoltre a Direct3D di non fornire alcun servizio di emulazione per l'elaborazione dei vertici.</span><span class="sxs-lookup"><span data-stu-id="37a5d-159">It also tells Direct3D not to provide any emulation services for vertex processing.</span></span> <span data-ttu-id="37a5d-160">Ciò significa che se il dispositivo non supporta l'elaborazione dei vertici, l'applicazione può usare solo i vertici post-trasformati.</span><span class="sxs-lookup"><span data-stu-id="37a5d-160">This means that if the device does not support vertex processing, then the application can use only post-transformed vertices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37a5d-161">D3DCREATE_SCREENSAVER</span><span class="sxs-lookup"><span data-stu-id="37a5d-161">D3DCREATE_SCREENSAVER</span></span></td>
<td><span data-ttu-id="37a5d-162">Consente lo screen saver durante un'applicazione a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="37a5d-162">Allows screensavers during a fullscreen application.</span></span> <span data-ttu-id="37a5d-163">Senza questo flag, Direct3D Disabilita gli screensaver fino a quando l'applicazione chiamante è a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="37a5d-163">Without this flag, Direct3D will disable screensavers for as long as the calling application is fullscreen.</span></span> <span data-ttu-id="37a5d-164">Se l'applicazione chiamante è già un salvaschermo, questo flag non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="37a5d-164">If the calling application is already a screensaver, this flag has no effect.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37a5d-165">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="37a5d-165">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="37a5d-166">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="37a5d-166">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="37a5d-167">D3DCREATE \_ hardware \_ VERTEXPROCESSING, D3DCREATE \_ mixed \_ VERTEXPROCESSING e D3DCREATE \_ software VERTEXPROCESSING \_ sono flag che si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="37a5d-167">D3DCREATE\_HARDWARE\_VERTEXPROCESSING, D3DCREATE\_MIXED\_VERTEXPROCESSING, and D3DCREATE\_SOFTWARE\_VERTEXPROCESSING are mutually exclusive flags.</span></span> <span data-ttu-id="37a5d-168">È necessario specificare almeno uno di questi flag di elaborazione dei vertici quando si chiama [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span><span class="sxs-lookup"><span data-stu-id="37a5d-168">At least one of these vertex processing flags must be specified when calling [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span>

## <a name="constant-information"></a><span data-ttu-id="37a5d-169">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="37a5d-169">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="37a5d-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37a5d-170">Header</span></span>                   | <span data-ttu-id="37a5d-171">D3D9. h</span><span class="sxs-lookup"><span data-stu-id="37a5d-171">D3D9.h</span></span>     |
| <span data-ttu-id="37a5d-172">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="37a5d-172">Minimum operating system</span></span> | <span data-ttu-id="37a5d-173">Windows 98</span><span class="sxs-lookup"><span data-stu-id="37a5d-173">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="37a5d-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="37a5d-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37a5d-175">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="37a5d-175">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
