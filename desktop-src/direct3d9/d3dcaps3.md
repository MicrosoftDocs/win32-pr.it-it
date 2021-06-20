---
description: Vedere un elenco di flag di funzionalità del driver D3DCAPS3. Include le definizioni, i valori e le descrizioni con collegamenti alle API.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b28614b2b2ea3c20f828b39f2b8926cb484a88c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408264"
---
# <a name="d3dcaps3"></a><span data-ttu-id="6a29f-104">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="6a29f-104">D3DCAPS3</span></span>

<span data-ttu-id="6a29f-105">Flag di funzionalità del driver.</span><span class="sxs-lookup"><span data-stu-id="6a29f-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6a29f-106">#Definire</span><span class="sxs-lookup"><span data-stu-id="6a29f-106">#define</span></span></td>
<td><span data-ttu-id="6a29f-107">Valore</span><span class="sxs-lookup"><span data-stu-id="6a29f-107">Value</span></span></td>
<td><span data-ttu-id="6a29f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a29f-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a29f-109">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="6a29f-109">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="6a29f-110">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="6a29f-110">0x00000020L</span></span></td>
<td><span data-ttu-id="6a29f-111">Indica che il dispositivo può rispettare lo stato D3DRS_ALPHABLENDENABLE rendering in modalità schermo intero quando si usa l'effetto di scambio FLIP o DISCARD.</span><span class="sxs-lookup"><span data-stu-id="6a29f-111">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="6a29f-112">Questo vale solo quando gli D3DRS_SRCBLEND o D3DRS_DESTBLEND sono impostati su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6a29f-112">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="6a29f-113">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="6a29f-113">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="6a29f-114">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="6a29f-114">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="6a29f-115">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="6a29f-115">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="6a29f-116">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="6a29f-116">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a29f-117">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="6a29f-117">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="6a29f-118">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="6a29f-118">0x00000100L</span></span></td>
<td><span data-ttu-id="6a29f-119">Il dispositivo può accelerare una copia della memoria dalla memoria di sistema alla memoria video locale.</span><span class="sxs-lookup"><span data-stu-id="6a29f-119">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="6a29f-120">Questo limite garantisce che le <a href="/windows/desktop/api"><strong>chiamate UpdateSurface</strong></a> <a href="/windows/desktop/api"><strong>e UpdateTexture</strong></a> saranno accelerate dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="6a29f-120">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="6a29f-121">Se questo limite è assente, queste chiamate avranno esito positivo ma saranno più lente.</span><span class="sxs-lookup"><span data-stu-id="6a29f-121">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a29f-122">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="6a29f-122">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="6a29f-123">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="6a29f-123">0x00000200L</span></span></td>
<td><span data-ttu-id="6a29f-124">Il dispositivo può accelerare una copia della memoria dalla memoria video locale alla memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="6a29f-124">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="6a29f-125">Questo limite garantisce che le <a href="/windows/desktop/api"><strong>chiamate GetRenderTargetData</strong></a> saranno accelerate dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="6a29f-125">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="6a29f-126">Se questo limite è assente, questa chiamata avrà esito positivo ma sarà più lenta.</span><span class="sxs-lookup"><span data-stu-id="6a29f-126">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a29f-127">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="6a29f-127">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="6a29f-128">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="6a29f-128">0x00000400L</span></span></td>
<td><span data-ttu-id="6a29f-129">Il driver video supporta DXVA-HD DDI.</span><span class="sxs-lookup"><span data-stu-id="6a29f-129">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="6a29f-130">Per altre informazioni su DXVA-HD DDI, vedere Processing High-Definition Video (Elaborazione <a href="https://msdn.microsoft.com/library/dd835176.aspx">di High-Definition video).</a></span><span class="sxs-lookup"><span data-stu-id="6a29f-130">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6a29f-131">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="6a29f-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="6a29f-132">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="6a29f-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a29f-133">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="6a29f-133">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="6a29f-134">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="6a29f-134">0x00000080L</span></span></td>
<td><span data-ttu-id="6a29f-135">Indica che il dispositivo può eseguire la correzione gamma da un buffer nascosto con finestra (contenente contenuto lineare) a un desktop sRGB.</span><span class="sxs-lookup"><span data-stu-id="6a29f-135">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a29f-136">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="6a29f-136">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="6a29f-137">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="6a29f-137">0x8000001fL</span></span></td>
<td><span data-ttu-id="6a29f-138">Riservato; non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="6a29f-138">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6a29f-139">Queste costanti vengono usate dal membro D3CAPS3 di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="6a29f-139">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="6a29f-140">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="6a29f-140">Constant Information</span></span>



|  <span data-ttu-id="6a29f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a29f-141">Requirement</span></span>                        | <span data-ttu-id="6a29f-142">Valore</span><span class="sxs-lookup"><span data-stu-id="6a29f-142">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="6a29f-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a29f-143">Header</span></span>                   | <span data-ttu-id="6a29f-144">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="6a29f-144">d3d9caps.h</span></span> |
| <span data-ttu-id="6a29f-145">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="6a29f-145">Minimum operating system</span></span> | <span data-ttu-id="6a29f-146">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6a29f-146">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6a29f-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a29f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a29f-148">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="6a29f-148">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




