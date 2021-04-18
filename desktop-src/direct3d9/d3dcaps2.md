---
description: Flag capacità driver.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953e73c0ea6b079a6b8f0658790c749b4f30a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305053"
---
# <a name="d3dcaps2"></a><span data-ttu-id="264fe-103">D3DCAPS2</span><span class="sxs-lookup"><span data-stu-id="264fe-103">D3DCAPS2</span></span>

<span data-ttu-id="264fe-104">Flag capacità driver.</span><span class="sxs-lookup"><span data-stu-id="264fe-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="264fe-105">#definire</span><span class="sxs-lookup"><span data-stu-id="264fe-105">#define</span></span></td>
<td><span data-ttu-id="264fe-106">Valore</span><span class="sxs-lookup"><span data-stu-id="264fe-106">Value</span></span></td>
<td><span data-ttu-id="264fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="264fe-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="264fe-108">D3DCAPS2_CANAUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="264fe-108">D3DCAPS2_CANAUTOGENMIPMAP</span></span></td>
<td><span data-ttu-id="264fe-109">0x40000000L</span><span class="sxs-lookup"><span data-stu-id="264fe-109">0x40000000L</span></span></td>
<td><span data-ttu-id="264fe-110">Il driver è in grado di generare automaticamente mipmap.</span><span class="sxs-lookup"><span data-stu-id="264fe-110">The driver is capable of automatically generating mipmaps.</span></span> <span data-ttu-id="264fe-111">Per ulteriori informazioni, vedere <a href="automatic-generation-of-mipmaps.md">generazione automatica di mipmap (Direct3D 9)</a>.</span><span class="sxs-lookup"><span data-stu-id="264fe-111">For more information, see <a href="automatic-generation-of-mipmaps.md">Automatic Generation of Mipmaps (Direct3D 9)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="264fe-112">D3DCAPS2_CANCALIBRATEGAMMA</span><span class="sxs-lookup"><span data-stu-id="264fe-112">D3DCAPS2_CANCALIBRATEGAMMA</span></span></td>
<td><span data-ttu-id="264fe-113">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="264fe-113">0x00100000L</span></span></td>
<td><span data-ttu-id="264fe-114">Nel sistema è installato un calibratore in grado di regolare automaticamente la rampa gamma, in modo che il risultato sia identico in tutti i sistemi con un calibratore.</span><span class="sxs-lookup"><span data-stu-id="264fe-114">The system has a calibrator installed that can automatically adjust the gamma ramp so that the result is identical on all systems that have a calibrator.</span></span> <span data-ttu-id="264fe-115">Per richiamare il calibratore quando si impostano nuovi livelli gamma, usare il flag D3DSGR_CALIBRATE quando si chiama <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="264fe-115">To invoke the calibrator when setting new gamma levels, use the D3DSGR_CALIBRATE flag when calling <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span></span> <span data-ttu-id="264fe-116">La calibratura delle rampe gamma comporta un sovraccarico di elaborazione e non deve essere usata di frequente.</span><span class="sxs-lookup"><span data-stu-id="264fe-116">Calibrating gamma ramps incurs some processing overhead and should not be used frequently.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="264fe-117">D3DCAPS2_CANSHARERESOURCE</span><span class="sxs-lookup"><span data-stu-id="264fe-117">D3DCAPS2_CANSHARERESOURCE</span></span></td>
<td><span data-ttu-id="264fe-118">0x80000000L</span><span class="sxs-lookup"><span data-stu-id="264fe-118">0x80000000L</span></span></td>
<td><span data-ttu-id="264fe-119">Il dispositivo può creare risorse condivisibili.</span><span class="sxs-lookup"><span data-stu-id="264fe-119">The device can create sharable resources.</span></span> <span data-ttu-id="264fe-120">I metodi per la creazione di risorse possono impostare valori non NULL per i parametri <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="264fe-120">Methods that create resources can set non-NULL values for their <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> parameters.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="264fe-121">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="264fe-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="264fe-122">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="264fe-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="264fe-123">D3DCAPS2_CANMANAGERESOURCE</span><span class="sxs-lookup"><span data-stu-id="264fe-123">D3DCAPS2_CANMANAGERESOURCE</span></span></td>
<td><span data-ttu-id="264fe-124">0x10000000L</span><span class="sxs-lookup"><span data-stu-id="264fe-124">0x10000000L</span></span></td>
<td><span data-ttu-id="264fe-125">Il driver è in grado di gestire le risorse.</span><span class="sxs-lookup"><span data-stu-id="264fe-125">The driver is capable of managing resources.</span></span> <span data-ttu-id="264fe-126">In questi driver D3DPOOL_MANAGED risorse verranno gestite dal driver.</span><span class="sxs-lookup"><span data-stu-id="264fe-126">On such drivers, D3DPOOL_MANAGED resources will be managed by the driver.</span></span> <span data-ttu-id="264fe-127">Per fare in modo che Direct3D esegua l'override del driver affinché Direct3D gestisca le risorse, usare il flag D3DCREATE_DISABLE_DRIVER_MANAGEMENT quando si chiama <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="264fe-127">To have Direct3D override the driver so that Direct3D manages resources, use the D3DCREATE_DISABLE_DRIVER_MANAGEMENT flag when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="264fe-128">D3DCAPS2_DYNAMICTEXTURES</span><span class="sxs-lookup"><span data-stu-id="264fe-128">D3DCAPS2_DYNAMICTEXTURES</span></span></td>
<td><span data-ttu-id="264fe-129">0x20000000L</span><span class="sxs-lookup"><span data-stu-id="264fe-129">0x20000000L</span></span></td>
<td><span data-ttu-id="264fe-130">Il driver supporta le trame dinamiche.</span><span class="sxs-lookup"><span data-stu-id="264fe-130">The driver supports dynamic textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="264fe-131">D3DCAPS2_FULLSCREENGAMMA</span><span class="sxs-lookup"><span data-stu-id="264fe-131">D3DCAPS2_FULLSCREENGAMMA</span></span></td>
<td><span data-ttu-id="264fe-132">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="264fe-132">0x00020000L</span></span></td>
<td><span data-ttu-id="264fe-133">Il driver supporta la regolazione della rampa dinamica gamma in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="264fe-133">The driver supports dynamic gamma ramp adjustment in full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="264fe-134">D3DCAPS2_RESERVED</span><span class="sxs-lookup"><span data-stu-id="264fe-134">D3DCAPS2_RESERVED</span></span></td>
<td><span data-ttu-id="264fe-135">0x02000000L</span><span class="sxs-lookup"><span data-stu-id="264fe-135">0x02000000L</span></span></td>
<td><span data-ttu-id="264fe-136">Riservati non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="264fe-136">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="264fe-137">Queste costanti vengono usate dal membro D3CAPS2 di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="264fe-137">These constants are used by the D3CAPS2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="264fe-138">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="264fe-138">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="264fe-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="264fe-139">Header</span></span>                   | <span data-ttu-id="264fe-140">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="264fe-140">d3d9caps.h</span></span> |
| <span data-ttu-id="264fe-141">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="264fe-141">Minimum operating system</span></span> | <span data-ttu-id="264fe-142">Windows 98</span><span class="sxs-lookup"><span data-stu-id="264fe-142">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="264fe-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="264fe-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="264fe-144">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="264fe-144">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
