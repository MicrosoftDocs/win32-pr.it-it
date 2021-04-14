---
description: Combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2ffff3d1dcc1f68912847b9ce1677c2031189c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401502"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="6cb1a-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="6cb1a-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="6cb1a-104">Combinazione di uno o più flag che controllano il comportamento di creazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6cb1a-104">A combination of one or more flags that control the device create behavior.</span></span>



|                                         |                                                                                                                                                                                                    |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb1a-105">\#definire</span><span class="sxs-lookup"><span data-stu-id="6cb1a-105">\#define</span></span>                                | <span data-ttu-id="6cb1a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cb1a-106">Description</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="6cb1a-107">\_DIRECTIONALLIGHTS D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="6cb1a-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="6cb1a-108">Il dispositivo può eseguire luci direzionali.</span><span class="sxs-lookup"><span data-stu-id="6cb1a-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="6cb1a-109">\_LOCALVIEWER D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="6cb1a-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="6cb1a-110">Il dispositivo può eseguire il visualizzatore locale.</span><span class="sxs-lookup"><span data-stu-id="6cb1a-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="6cb1a-111">\_MATERIALSOURCE7 D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="6cb1a-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="6cb1a-112">Quando questo limite è impostato, il dispositivo supporta gli Stati del materiale colore: D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE e D3DRS SPECULARMATERIALSOURCE \_ .</span><span class="sxs-lookup"><span data-stu-id="6cb1a-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="6cb1a-113">D3DVTXPCAPS \_ No \_ TEXGEN \_ NONLOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="6cb1a-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="6cb1a-114">Il dispositivo non supporta la generazione di trama in modalità visualizzatore non locale.</span><span class="sxs-lookup"><span data-stu-id="6cb1a-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="6cb1a-115">\_POSITIONALLIGHTS D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="6cb1a-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="6cb1a-116">Il dispositivo può eseguire luci posizionali (include punto e punto).</span><span class="sxs-lookup"><span data-stu-id="6cb1a-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="6cb1a-117">\_TEXGEN D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="6cb1a-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="6cb1a-118">Il dispositivo può eseguire texgen.</span><span class="sxs-lookup"><span data-stu-id="6cb1a-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="6cb1a-119">D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="6cb1a-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="6cb1a-120">Il dispositivo supporta D3DTSS \_ TCI \_ SPHEREMAP.</span><span class="sxs-lookup"><span data-stu-id="6cb1a-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="6cb1a-121">\_Interpolazione D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="6cb1a-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="6cb1a-122">Il dispositivo può eseguire l'interpolazione dei vertici.</span><span class="sxs-lookup"><span data-stu-id="6cb1a-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="6cb1a-123">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="6cb1a-123">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="6cb1a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6cb1a-124">Header</span></span>                   | <span data-ttu-id="6cb1a-125">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="6cb1a-125">d3d9caps.h</span></span> |
| <span data-ttu-id="6cb1a-126">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="6cb1a-126">Minimum operating system</span></span> | <span data-ttu-id="6cb1a-127">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6cb1a-127">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6cb1a-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6cb1a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cb1a-129">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="6cb1a-129">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



