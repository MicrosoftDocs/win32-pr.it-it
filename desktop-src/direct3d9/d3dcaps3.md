---
description: Flag di funzionalità del driver.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda81aa7f77dcaf03eb06b357ebfb91b4956f6d4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343366"
---
# <a name="d3dcaps3"></a><span data-ttu-id="2f0c5-103">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="2f0c5-103">D3DCAPS3</span></span>

<span data-ttu-id="2f0c5-104">Flag di funzionalità del driver.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f0c5-105">#Definire</span><span class="sxs-lookup"><span data-stu-id="2f0c5-105">#define</span></span></td>
<td><span data-ttu-id="2f0c5-106">Valore</span><span class="sxs-lookup"><span data-stu-id="2f0c5-106">Value</span></span></td>
<td><span data-ttu-id="2f0c5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f0c5-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f0c5-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="2f0c5-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="2f0c5-109">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="2f0c5-109">0x00000020L</span></span></td>
<td><span data-ttu-id="2f0c5-110">Indica che il dispositivo può rispettare lo stato D3DRS_ALPHABLENDENABLE rendering in modalità schermo intero quando si usa l'effetto di scambio FLIP o DISCARD.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-110">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="2f0c5-111">Questo vale solo quando gli D3DRS_SRCBLEND o D3DRS_DESTBLEND sono impostati su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f0c5-111">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="2f0c5-112">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="2f0c5-112">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="2f0c5-113">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="2f0c5-113">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="2f0c5-114">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="2f0c5-114">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="2f0c5-115">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="2f0c5-115">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f0c5-116">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="2f0c5-116">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="2f0c5-117">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="2f0c5-117">0x00000100L</span></span></td>
<td><span data-ttu-id="2f0c5-118">Il dispositivo può accelerare una copia della memoria dalla memoria di sistema alla memoria video locale.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-118">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="2f0c5-119">Questo limite garantisce che le <a href="/windows/desktop/api"><strong>chiamate UpdateSurface</strong></a> <a href="/windows/desktop/api"><strong>e UpdateTexture</strong></a> saranno accelerate dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-119">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="2f0c5-120">Se questo limite è assente, queste chiamate avranno esito positivo ma saranno più lente.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-120">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f0c5-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="2f0c5-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="2f0c5-122">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="2f0c5-122">0x00000200L</span></span></td>
<td><span data-ttu-id="2f0c5-123">Il dispositivo può accelerare una copia della memoria dalla memoria video locale alla memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-123">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="2f0c5-124">Questo limite garantisce che <a href="/windows/desktop/api"><strong>le chiamate GetRenderTargetData</strong></a> saranno accelerate dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-124">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="2f0c5-125">Se questo limite è assente, questa chiamata avrà esito positivo, ma sarà più lenta.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-125">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f0c5-126">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="2f0c5-126">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="2f0c5-127">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="2f0c5-127">0x00000400L</span></span></td>
<td><span data-ttu-id="2f0c5-128">Il driver di visualizzazione supporta DXVA-HD DDI.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-128">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="2f0c5-129">Per altre informazioni su DXVA-HD DDI, vedere <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-129">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f0c5-130">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="2f0c5-130">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="2f0c5-131">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-131">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f0c5-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="2f0c5-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="2f0c5-133">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="2f0c5-133">0x00000080L</span></span></td>
<td><span data-ttu-id="2f0c5-134">Indica che il dispositivo può eseguire la correzione gamma da un buffer nascosto con finestra (contenente contenuto lineare) a un desktop sRGB.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-134">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f0c5-135">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="2f0c5-135">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="2f0c5-136">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="2f0c5-136">0x8000001fL</span></span></td>
<td><span data-ttu-id="2f0c5-137">Riservato; non usato.</span><span class="sxs-lookup"><span data-stu-id="2f0c5-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2f0c5-138">Queste costanti vengono usate dal membro D3CAPS3 di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="2f0c5-138">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="2f0c5-139">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="2f0c5-139">Constant Information</span></span>



|  <span data-ttu-id="2f0c5-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f0c5-140">Requirement</span></span>                        | <span data-ttu-id="2f0c5-141">Valore</span><span class="sxs-lookup"><span data-stu-id="2f0c5-141">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="2f0c5-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f0c5-142">Header</span></span>                   | <span data-ttu-id="2f0c5-143">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="2f0c5-143">d3d9caps.h</span></span> |
| <span data-ttu-id="2f0c5-144">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="2f0c5-144">Minimum operating system</span></span> | <span data-ttu-id="2f0c5-145">Windows 98</span><span class="sxs-lookup"><span data-stu-id="2f0c5-145">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2f0c5-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f0c5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f0c5-147">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="2f0c5-147">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




