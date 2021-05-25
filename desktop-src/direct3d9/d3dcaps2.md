---
description: Vedere un elenco di flag di funzionalità del driver. Include definizioni, valori e descrizioni con collegamenti alle API.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f209e840450b834c3a69593d1297f2cba9ee43c0
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343376"
---
# <a name="d3dcaps2"></a><span data-ttu-id="8cf5a-104">D3DCAPS2</span><span class="sxs-lookup"><span data-stu-id="8cf5a-104">D3DCAPS2</span></span>

<span data-ttu-id="8cf5a-105">Flag di funzionalità del driver.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8cf5a-106">#Definire</span><span class="sxs-lookup"><span data-stu-id="8cf5a-106">#define</span></span></td>
<td><span data-ttu-id="8cf5a-107">Valore</span><span class="sxs-lookup"><span data-stu-id="8cf5a-107">Value</span></span></td>
<td><span data-ttu-id="8cf5a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cf5a-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cf5a-109">D3DCAPS2_CANAUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="8cf5a-109">D3DCAPS2_CANAUTOGENMIPMAP</span></span></td>
<td><span data-ttu-id="8cf5a-110">0x40000000L</span><span class="sxs-lookup"><span data-stu-id="8cf5a-110">0x40000000L</span></span></td>
<td><span data-ttu-id="8cf5a-111">Il driver è in grado di generare automaticamente mipmap.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-111">The driver is capable of automatically generating mipmaps.</span></span> <span data-ttu-id="8cf5a-112">Per altre informazioni, vedere <a href="automatic-generation-of-mipmaps.md">Generazione automatica di mipmap (Direct3D 9).</a></span><span class="sxs-lookup"><span data-stu-id="8cf5a-112">For more information, see <a href="automatic-generation-of-mipmaps.md">Automatic Generation of Mipmaps (Direct3D 9)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cf5a-113">D3DCAPS2_CANCALIBRATEGAMMA</span><span class="sxs-lookup"><span data-stu-id="8cf5a-113">D3DCAPS2_CANCALIBRATEGAMMA</span></span></td>
<td><span data-ttu-id="8cf5a-114">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="8cf5a-114">0x00100000L</span></span></td>
<td><span data-ttu-id="8cf5a-115">Nel sistema è installato un calibratore in grado di regolare automaticamente la rampa gamma in modo che il risultato sia identico in tutti i sistemi con calibrazione.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-115">The system has a calibrator installed that can automatically adjust the gamma ramp so that the result is identical on all systems that have a calibrator.</span></span> <span data-ttu-id="8cf5a-116">Per richiamare il calibratore quando si impostano nuovi livelli gamma, usare il flag D3DSGR_CALIBRATE quando si <a href="/windows/desktop/api"><strong>chiama SetGammaRamp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-116">To invoke the calibrator when setting new gamma levels, use the D3DSGR_CALIBRATE flag when calling <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span></span> <span data-ttu-id="8cf5a-117">La calibrazione delle rampe gamma comporta un sovraccarico di elaborazione e non deve essere usata di frequente.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-117">Calibrating gamma ramps incurs some processing overhead and should not be used frequently.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cf5a-118">D3DCAPS2_CANSHARERESOURCE</span><span class="sxs-lookup"><span data-stu-id="8cf5a-118">D3DCAPS2_CANSHARERESOURCE</span></span></td>
<td><span data-ttu-id="8cf5a-119">0x80000000L</span><span class="sxs-lookup"><span data-stu-id="8cf5a-119">0x80000000L</span></span></td>
<td><span data-ttu-id="8cf5a-120">Il dispositivo può creare risorse condivise.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-120">The device can create sharable resources.</span></span> <span data-ttu-id="8cf5a-121">I metodi che creano risorse possono impostare valori non NULL per i <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>parametri pSharedHandle.</strong></a></span><span class="sxs-lookup"><span data-stu-id="8cf5a-121">Methods that create resources can set non-NULL values for their <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> parameters.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8cf5a-122">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="8cf5a-122">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="8cf5a-123">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-123">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cf5a-124">D3DCAPS2_CANMANAGERESOURCE</span><span class="sxs-lookup"><span data-stu-id="8cf5a-124">D3DCAPS2_CANMANAGERESOURCE</span></span></td>
<td><span data-ttu-id="8cf5a-125">0x10000000L</span><span class="sxs-lookup"><span data-stu-id="8cf5a-125">0x10000000L</span></span></td>
<td><span data-ttu-id="8cf5a-126">Il driver è in grado di gestire le risorse.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-126">The driver is capable of managing resources.</span></span> <span data-ttu-id="8cf5a-127">Su tali driver, D3DPOOL_MANAGED risorse verranno gestite dal driver.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-127">On such drivers, D3DPOOL_MANAGED resources will be managed by the driver.</span></span> <span data-ttu-id="8cf5a-128">Per fare in modo che Direct3D ese sostituisca il driver in modo che Direct3D gestirà le risorse, usare il flag D3DCREATE_DISABLE_DRIVER_MANAGEMENT quando si chiama <a href="/windows/desktop/api"><strong>CreateDevice.</strong></a></span><span class="sxs-lookup"><span data-stu-id="8cf5a-128">To have Direct3D override the driver so that Direct3D manages resources, use the D3DCREATE_DISABLE_DRIVER_MANAGEMENT flag when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cf5a-129">D3DCAPS2_DYNAMICTEXTURES</span><span class="sxs-lookup"><span data-stu-id="8cf5a-129">D3DCAPS2_DYNAMICTEXTURES</span></span></td>
<td><span data-ttu-id="8cf5a-130">0x20000000L</span><span class="sxs-lookup"><span data-stu-id="8cf5a-130">0x20000000L</span></span></td>
<td><span data-ttu-id="8cf5a-131">Il driver supporta trame dinamiche.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-131">The driver supports dynamic textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cf5a-132">D3DCAPS2_FULLSCREENGAMMA</span><span class="sxs-lookup"><span data-stu-id="8cf5a-132">D3DCAPS2_FULLSCREENGAMMA</span></span></td>
<td><span data-ttu-id="8cf5a-133">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="8cf5a-133">0x00020000L</span></span></td>
<td><span data-ttu-id="8cf5a-134">Il driver supporta la regolazione dinamica della rampa gamma in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-134">The driver supports dynamic gamma ramp adjustment in full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cf5a-135">D3DCAPS2_RESERVED</span><span class="sxs-lookup"><span data-stu-id="8cf5a-135">D3DCAPS2_RESERVED</span></span></td>
<td><span data-ttu-id="8cf5a-136">0x02000000L</span><span class="sxs-lookup"><span data-stu-id="8cf5a-136">0x02000000L</span></span></td>
<td><span data-ttu-id="8cf5a-137">Riservato; non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8cf5a-138">Queste costanti vengono usate dal membro D3CAPS2 di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="8cf5a-138">These constants are used by the D3CAPS2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="8cf5a-139">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="8cf5a-139">Constant Information</span></span>



|  <span data-ttu-id="8cf5a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cf5a-140">Requirement</span></span>                        | <span data-ttu-id="8cf5a-141">Valore</span><span class="sxs-lookup"><span data-stu-id="8cf5a-141">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="8cf5a-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8cf5a-142">Header</span></span>                   | <span data-ttu-id="8cf5a-143">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="8cf5a-143">d3d9caps.h</span></span> |
| <span data-ttu-id="8cf5a-144">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="8cf5a-144">Minimum operating system</span></span> | <span data-ttu-id="8cf5a-145">Windows 98</span><span class="sxs-lookup"><span data-stu-id="8cf5a-145">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8cf5a-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8cf5a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cf5a-147">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="8cf5a-147">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
