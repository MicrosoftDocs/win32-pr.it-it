---
description: Flag capacità driver.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a165ff1d550612ba302c94a0b8181affe040921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305052"
---
# <a name="d3dcaps3"></a><span data-ttu-id="53356-103">D3DCAPS3</span><span class="sxs-lookup"><span data-stu-id="53356-103">D3DCAPS3</span></span>

<span data-ttu-id="53356-104">Flag capacità driver.</span><span class="sxs-lookup"><span data-stu-id="53356-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53356-105">#definire</span><span class="sxs-lookup"><span data-stu-id="53356-105">#define</span></span></td>
<td><span data-ttu-id="53356-106">Valore</span><span class="sxs-lookup"><span data-stu-id="53356-106">Value</span></span></td>
<td><span data-ttu-id="53356-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53356-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53356-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span><span class="sxs-lookup"><span data-stu-id="53356-108">D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</span></span></td>
<td><span data-ttu-id="53356-109">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="53356-109">0x00000020L</span></span></td>
<td><span data-ttu-id="53356-110">Indica che il dispositivo può rispettare lo stato di rendering D3DRS_ALPHABLENDENABLE in modalità schermo intero, mentre si utilizza l'effetto di swapping FLIP o scarto.</span><span class="sxs-lookup"><span data-stu-id="53356-110">Indicates that the device can respect the D3DRS_ALPHABLENDENABLE render state in full-screen mode while using the FLIP or DISCARD swap effect.</span></span> <span data-ttu-id="53356-111">Questo vale solo quando gli Stati D3DRS_SRCBLEND o D3DRS_DESTBLEND sono impostati su uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="53356-111">This only applies when the D3DRS_SRCBLEND or D3DRS_DESTBLEND states are set to one of the following:</span></span>
<ul>
<li><span data-ttu-id="53356-112">D3DBLEND_DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="53356-112">D3DBLEND_DESTALPHA</span></span></li>
<li><span data-ttu-id="53356-113">D3DBLEND_INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="53356-113">D3DBLEND_INVDESTALPHA</span></span></li>
<li><span data-ttu-id="53356-114">D3DBLEND_DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="53356-114">D3DBLEND_DESTCOLOR</span></span></li>
<li><span data-ttu-id="53356-115">D3DBLEND_INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="53356-115">D3DBLEND_INVDESTCOLOR</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53356-116">D3DCAPS3_COPY_TO_VIDMEM</span><span class="sxs-lookup"><span data-stu-id="53356-116">D3DCAPS3_COPY_TO_VIDMEM</span></span></td>
<td><span data-ttu-id="53356-117">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="53356-117">0x00000100L</span></span></td>
<td><span data-ttu-id="53356-118">Il dispositivo può accelerare una copia di memoria dalla memoria di sistema alla memoria video locale.</span><span class="sxs-lookup"><span data-stu-id="53356-118">Device can accelerate a memory copy from system memory to local video memory.</span></span> <span data-ttu-id="53356-119">Questo limite garantisce che le chiamate a <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> e <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> saranno accelerate dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="53356-119">This cap guarantees that <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> and <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="53356-120">Se questo limite è assente, queste chiamate riusciranno ma saranno più lente.</span><span class="sxs-lookup"><span data-stu-id="53356-120">If this cap is absent, these calls will succeed but will be slower.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53356-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="53356-121">D3DCAPS3_COPY_TO_SYSTEMMEM</span></span></td>
<td><span data-ttu-id="53356-122">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="53356-122">0x00000200L</span></span></td>
<td><span data-ttu-id="53356-123">Il dispositivo può accelerare una copia di memoria dalla memoria video locale alla memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="53356-123">Device can accelerate a memory copy from local video memory to system memory.</span></span> <span data-ttu-id="53356-124">Questo limite garantisce che le chiamate di <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> saranno accelerate dall'hardware.</span><span class="sxs-lookup"><span data-stu-id="53356-124">This cap guarantees that <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> calls will be hardware accelerated.</span></span> <span data-ttu-id="53356-125">Se questo limite è assente, la chiamata avrà esito positivo ma sarà più lenta.</span><span class="sxs-lookup"><span data-stu-id="53356-125">If this cap is absent, this call will succeed but will be slower.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53356-126">D3DCAPS3_DXVAHD</span><span class="sxs-lookup"><span data-stu-id="53356-126">D3DCAPS3_DXVAHD</span></span></td>
<td><span data-ttu-id="53356-127">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="53356-127">0x00000400L</span></span></td>
<td><span data-ttu-id="53356-128">Il driver di visualizzazione supporta l'interfaccia DDI DXVA-HD.</span><span class="sxs-lookup"><span data-stu-id="53356-128">The display driver supports the DXVA-HD DDI.</span></span> <span data-ttu-id="53356-129">Per altre informazioni su DXVA-HD DDI, vedere <a href="https://msdn.microsoft.com/library/dd835176.aspx">elaborazione High-Definition video</a>.</span><span class="sxs-lookup"><span data-stu-id="53356-129">For more information about DXVA-HD DDI, see <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53356-130">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="53356-130">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="53356-131">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="53356-131">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53356-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span><span class="sxs-lookup"><span data-stu-id="53356-132">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</span></span></td>
<td><span data-ttu-id="53356-133">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="53356-133">0x00000080L</span></span></td>
<td><span data-ttu-id="53356-134">Indica che il dispositivo può eseguire la correzione gamma da un buffer nascosto a finestra (contenente contenuto lineare) a un desktop sRGB.</span><span class="sxs-lookup"><span data-stu-id="53356-134">Indicates that the device can perform gamma correction from a windowed back buffer (containing linear content) to an sRGB desktop.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53356-135">D3DCAPS3_RESERVED</span><span class="sxs-lookup"><span data-stu-id="53356-135">D3DCAPS3_RESERVED</span></span></td>
<td><span data-ttu-id="53356-136">0x8000001fL</span><span class="sxs-lookup"><span data-stu-id="53356-136">0x8000001fL</span></span></td>
<td><span data-ttu-id="53356-137">Riservati non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="53356-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="53356-138">Queste costanti vengono usate dal membro D3CAPS3 di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="53356-138">These constants are used by the D3CAPS3 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="53356-139">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="53356-139">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="53356-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53356-140">Header</span></span>                   | <span data-ttu-id="53356-141">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="53356-141">d3d9caps.h</span></span> |
| <span data-ttu-id="53356-142">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="53356-142">Minimum operating system</span></span> | <span data-ttu-id="53356-143">Windows 98</span><span class="sxs-lookup"><span data-stu-id="53356-143">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="53356-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53356-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53356-145">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="53356-145">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




