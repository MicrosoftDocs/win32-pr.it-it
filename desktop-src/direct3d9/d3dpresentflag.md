---
description: Costanti utilizzate dai parametri D3DPRESENT \_ .
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3b7fe950a6fe09425aa47a79ce8f803eb81298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304792"
---
# <a name="d3dpresentflag"></a><span data-ttu-id="9cf7f-103">D3DPRESENTFLAG</span><span class="sxs-lookup"><span data-stu-id="9cf7f-103">D3DPRESENTFLAG</span></span>

<span data-ttu-id="9cf7f-104">Costanti utilizzate dai [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9cf7f-104">Constants used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cf7f-105">#definire</span><span class="sxs-lookup"><span data-stu-id="9cf7f-105">#define</span></span></td>
<td><span data-ttu-id="9cf7f-106">Valore</span><span class="sxs-lookup"><span data-stu-id="9cf7f-106">Value</span></span></td>
<td><span data-ttu-id="9cf7f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cf7f-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cf7f-108">D3DPRESENTFLAG_DEVICECLIP</span><span class="sxs-lookup"><span data-stu-id="9cf7f-108">D3DPRESENTFLAG_DEVICECLIP</span></span></td>
<td><span data-ttu-id="9cf7f-109">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9cf7f-109">0x00000004</span></span></td>
<td><span data-ttu-id="9cf7f-110">Ritagliare un blit <a href="/windows/desktop/api"><strong>presente</strong></a> nella finestra dell'area client della finestra, all'interno dell'area dello schermo del monitor della scheda video che ha creato il dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-110">Clip a windowed <a href="/windows/desktop/api"><strong>Present</strong></a> blit into the window client area, within the monitor screen area of the video adapter that created the Direct3D device.</span></span> <span data-ttu-id="9cf7f-111">D3DPRESENTFLAG_DEVICECLIP non è valido con D3DSWAPEFFECT_FLIPEX.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-111">D3DPRESENTFLAG_DEVICECLIP is not valid with D3DSWAPEFFECT_FLIPEX.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cf7f-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="9cf7f-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span></span></td>
<td><span data-ttu-id="9cf7f-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9cf7f-113">0x00000002</span></span></td>
<td><span data-ttu-id="9cf7f-114">Impostare questo flag quando si crea il dispositivo o la catena di scambio per abilitare l'eliminazione del buffer z.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-114">Set this flag when the device or swap chain is created to enable z-buffer discarding.</span></span> <span data-ttu-id="9cf7f-115">Se questo flag è impostato, il contenuto del buffer depth stencil non sarà valido dopo la chiamata a <a href="/windows/desktop/api"><strong>present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie di profondità diversa.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-115">If this flag is set, the contents of the depth stencil buffer will be invalid after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span> <span data-ttu-id="9cf7f-116">L'eliminazione dei dati del buffer z può migliorare le prestazioni e dipende dal driver.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-116">Discarding z-buffer data can increase performance and is driver dependent.</span></span> <span data-ttu-id="9cf7f-117">Il runtime di debug imporrà l'eliminazione deselezionando il buffer z su un valore costante dopo la chiamata di <a href="/windows/desktop/api"><strong>present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie di profondità diversa.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-117">The debug runtime will enforce discarding by clearing the z-buffer to some constant value after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span><br/> <span data-ttu-id="9cf7f-118">L'eliminazione dei dati del buffer z non è valida per tutti i formati bloccabili, D3DFMT_D16_LOCKABLE e D3DFMT_D32F_LOCKABLE.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-118">Discarding z-buffer data is illegal for all lockable formats, D3DFMT_D16_LOCKABLE and D3DFMT_D32F_LOCKABLE.</span></span> <span data-ttu-id="9cf7f-119">Qualsiasi uso di <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> che specifica un formato bloccabile e l'eliminazione del buffer z avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-119">Any use of <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> specifying a lockable format and z-buffer discarding will fail.</span></span> <span data-ttu-id="9cf7f-120">Per ulteriori informazioni sui formati, vedere <a href="d3dformat.md">D3DFORMAT</a>.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-120">For more information about formats, see <a href="d3dformat.md">D3DFORMAT</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cf7f-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="9cf7f-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span></span></td>
<td><span data-ttu-id="9cf7f-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cf7f-122">0x00000001</span></span></td>
<td><span data-ttu-id="9cf7f-123">Impostare questo flag se l'applicazione richiede la possibilità di bloccare direttamente il buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-123">Set this flag if the application requires the ability to lock the back buffer directly.</span></span> <span data-ttu-id="9cf7f-124">Si noti che i buffer indietro non sono bloccabili, a meno che l'applicazione non specifichi D3DPRESENTFLAG_LOCKABLE_BACKBUFFER quando si chiama <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> o <a href="/windows/desktop/api"><strong>Reset</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-124">Note that back buffers are not lockable unless the application specifies D3DPRESENTFLAG_LOCKABLE_BACKBUFFER when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> or <a href="/windows/desktop/api"><strong>Reset</strong></a>.</span></span> <span data-ttu-id="9cf7f-125">I buffer back bloccabili comportano un costo in termini di prestazioni in alcune configurazioni hardware grafiche.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-125">Lockable back buffers incur a performance cost on some graphics hardware configurations.</span></span> <span data-ttu-id="9cf7f-126">L'esecuzione di un'operazione di blocco (o l'utilizzo di <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> per la scrittura) sul buffer nascosto blocca le prestazioni in molte schede.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-126">Performing a lock operation (or using <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> to write) on the lockable back buffer decreases performance on many cards.</span></span> <span data-ttu-id="9cf7f-127">In questo caso, è consigliabile usare triangoli con trama per spostare i dati nel buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-127">In this case, consider using textured triangles to move data to the back buffer.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cf7f-128">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="9cf7f-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="9cf7f-129">In Direct3D9Ex non è possibile impostare questo flag se il D3DSWAPEFFECT è D3DSWAPEFFECT_FLIPEX, perché il modello Flip consente al Gestione finestre desktop di accedere al buffer nascosto di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-129">In Direct3D9Ex this flag cannot be set if the D3DSWAPEFFECT is D3DSWAPEFFECT_FLIPEX, since the flip model enables the Desktop Window Manager to access an application's back buffer.</span></span> <span data-ttu-id="9cf7f-130">Una superficie condivisa tra processi non deve essere bloccata.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-130">A cross-process shared-surface should not be locked.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cf7f-131">D3DPRESENTFLAG_NOAUTOROTATE</span><span class="sxs-lookup"><span data-stu-id="9cf7f-131">D3DPRESENTFLAG_NOAUTOROTATE</span></span></td>
<td><span data-ttu-id="9cf7f-132">0x00000020</span><span class="sxs-lookup"><span data-stu-id="9cf7f-132">0x00000020</span></span></td>
<td><span data-ttu-id="9cf7f-133">I monitoraggi ruotati vengono gestiti automaticamente con una copia girevole durante la presentazione, operazione non molto efficiente.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-133">Rotated monitors are handled automatically with a rotating copy during presentation, which is not very efficient.</span></span> <span data-ttu-id="9cf7f-134">Questo flag indica che l'applicazione eseguirà la rotazione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-134">This flag means the application will perform it's own display rotation.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cf7f-135">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="9cf7f-135">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="9cf7f-136">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-136">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="9cf7f-137">Le applicazioni possono ottenere la propria rotazione possibilmente utilizzando una matrice di viste ruotata.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-137">Applications can achieve their own rotation possibly by using a rotated view matrix.</span></span> <span data-ttu-id="9cf7f-138">I metodi <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> e <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> devono essere utilizzati per individuare l'impostazione di rotazione corrente.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-138">The methods <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> should be used to to find the current rotation setting.</span></span> <span data-ttu-id="9cf7f-139">I parametri della larghezza e dell'altezza del buffer in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> e <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> devono usare l'orientamento orizzontale, mentre la struttura della modalità di visualizzazione a schermo intero deve corrispondere a quella restituita da <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> , ad esempio la larghezza e l'altezza vengono scambiate quando si ruotano 90 e 270 gradi.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-139">The backbuffer Width and Height parameters in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> must be use landscape orientation, while the fullscreen display mode structure should be the same as what is returned from <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (i.e. Width and Height are swapped when rotated 90 and 270 degrees).</span></span></p>
<p><span data-ttu-id="9cf7f-140">Quando si usa il blocco su destinazioni di rendering ruotate, i presupposti dell'angolo superiore sinistro non sono più contenuta true, la destinazione di rendering SURFACE_DESC rimarrà orizzontale (in base a quanto previsto dai parametri di creazione) e la finestra GDI, le coordinate del mouse e tale necessità di essere convertite correttamente quando vengono usate con la destinazione e la scena di rendering Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-140">When using Lock on rotated render targets, upper-left corner assumptions no longer hold true, the render target SURFACE_DESC will remain landscape (as implied by the creation parameters), and GDI window, mouse coordinates, and such need to be properly translated when used with the Direct3D render target and scene.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cf7f-141">D3DPRESENTFLAG_UNPRUNEDMODE</span><span class="sxs-lookup"><span data-stu-id="9cf7f-141">D3DPRESENTFLAG_UNPRUNEDMODE</span></span></td>
<td><span data-ttu-id="9cf7f-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="9cf7f-142">0x00000040</span></span></td>
<td><span data-ttu-id="9cf7f-143">Utilizzare questo flag per specificare qualsiasi modalità di visualizzazione non ELABORAta enumerata dalla scheda video anche se Direct3D potrebbe indicare che la modalità non è valida.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-143">Use this flag to specify any RAW display mode enumerated by the display adapter even though Direct3D may have indicated the mode is invalid.</span></span> <span data-ttu-id="9cf7f-144">L'applicazione deve implementare questa operazione in modo affidabile, nel caso in cui la modalità desiderata non sia effettivamente valida.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-144">The application should implement this in a robust manner in case the desired mode really is invalid.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cf7f-145">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="9cf7f-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="9cf7f-146">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-146">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cf7f-147">D3DPRESENTFLAG_VIDEO</span><span class="sxs-lookup"><span data-stu-id="9cf7f-147">D3DPRESENTFLAG_VIDEO</span></span></td>
<td><span data-ttu-id="9cf7f-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cf7f-148">0x00000010</span></span></td>
<td><span data-ttu-id="9cf7f-149">Si tratta di un suggerimento per il driver che i buffer indietro conterranno dati video.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-149">This is a hint to the driver that the back buffers will contain video data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cf7f-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span><span class="sxs-lookup"><span data-stu-id="9cf7f-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span></span></td>
<td><span data-ttu-id="9cf7f-151">0x00000080</span><span class="sxs-lookup"><span data-stu-id="9cf7f-151">0x00000080</span></span></td>
<td><span data-ttu-id="9cf7f-152">Specifica se la sovrimpressione è di intervallo completo RGB o RGB a intervalli limitati.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-152">Specifies whether the overlay is full range RGB or limited range RGB.</span></span> <span data-ttu-id="9cf7f-153">L'impostazione di questo flag indica un intervallo limitato di RGB.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-153">Setting this flag indicates limited range RGB.</span></span> <span data-ttu-id="9cf7f-154">In RGB con intervallo limitato, l'intervallo RGB viene compresso in modo che 16:16:16 sia nero e 235:235:235 sia bianco.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-154">In limited range RGB, the RGB range is compressed such that 16:16:16 is black and 235:235:235 is white.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cf7f-155">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="9cf7f-155">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="9cf7f-156">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-156">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cf7f-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span><span class="sxs-lookup"><span data-stu-id="9cf7f-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span></span></td>
<td><span data-ttu-id="9cf7f-158">0x00000100</span><span class="sxs-lookup"><span data-stu-id="9cf7f-158">0x00000100</span></span></td>
<td><span data-ttu-id="9cf7f-159">Specifica se la sovrimpressione è BT. 601 o BT. 709.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-159">Specifies whether the overlay is BT.601 or BT.709.</span></span> <span data-ttu-id="9cf7f-160">L'impostazione di questo flag indica BT. 709 per la TV ad alta definizione (HDTV).</span><span class="sxs-lookup"><span data-stu-id="9cf7f-160">Setting this flag indicates BT.709, for high-definition TV (HDTV).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cf7f-161">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="9cf7f-161">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="9cf7f-162">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-162">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cf7f-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span><span class="sxs-lookup"><span data-stu-id="9cf7f-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span></span></td>
<td><span data-ttu-id="9cf7f-164">0x00000200</span><span class="sxs-lookup"><span data-stu-id="9cf7f-164">0x00000200</span></span></td>
<td><span data-ttu-id="9cf7f-165">Specifica se la sovrimpressione è YCbCr convenzionale o YCbCr esteso (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="9cf7f-165">Specifies whether the overlay is conventional YCbCr or extended YCbCr (xvYCC).</span></span> <span data-ttu-id="9cf7f-166">L'impostazione di questo flag indica YCbCr esteso (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="9cf7f-166">Setting this flag indicates extended YCbCr (xvYCC).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cf7f-167">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="9cf7f-167">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="9cf7f-168">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-168">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cf7f-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span><span class="sxs-lookup"><span data-stu-id="9cf7f-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span></span></td>
<td><span data-ttu-id="9cf7f-170">0x00000400</span><span class="sxs-lookup"><span data-stu-id="9cf7f-170">0x00000400</span></span></td>
<td><span data-ttu-id="9cf7f-171">L'impostazione di questo flag indica che il presentazione catena contiene contenuto protetto e fa in modo che il runtime limiti l'accesso al presentazione catena in modo che solo il desktop di Windows Manager (DWM) possa usare presentazione catena.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-171">Setting this flag indicates that the swapchain contains protected content and automatically causes the runtime to restrict access to the swapchain so that only the Desktop Windows Manager (DWM) can use the swapchain.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cf7f-172">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="9cf7f-172">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="9cf7f-173">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-173">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cf7f-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span><span class="sxs-lookup"><span data-stu-id="9cf7f-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span></span></td>
<td><span data-ttu-id="9cf7f-175">0x00000800</span><span class="sxs-lookup"><span data-stu-id="9cf7f-175">0x00000800</span></span></td>
<td><span data-ttu-id="9cf7f-176">L'impostazione di questo flag indica che il driver deve limitare l'accesso alle risorse condivise create per l'interazione con DWM.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-176">Setting this flag indicates that the driver should restrict access to any shared resources that are created for DWM interaction.</span></span> <span data-ttu-id="9cf7f-177">Il chiamante deve creare un canale autenticato con il driver.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-177">The caller must create an authenticated channel with the driver.</span></span> <span data-ttu-id="9cf7f-178">Il driver deve quindi consentire l'accesso ai processi che tentano di aprire tali risorse condivise.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-178">The driver should then allow access to processes that attempt to open those shared resources.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cf7f-179">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="9cf7f-179">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="9cf7f-180">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="9cf7f-180">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9cf7f-181">Queste costanti vengono usate dai [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9cf7f-181">These constants are used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="9cf7f-182">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="9cf7f-182">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="9cf7f-183">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9cf7f-183">Header</span></span>                   | <span data-ttu-id="9cf7f-184">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="9cf7f-184">d3d9types.h</span></span> |
| <span data-ttu-id="9cf7f-185">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="9cf7f-185">Minimum operating system</span></span> | <span data-ttu-id="9cf7f-186">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9cf7f-186">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="9cf7f-187">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9cf7f-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cf7f-188">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="9cf7f-188">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




