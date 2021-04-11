---
title: Effetto tinta
description: Questo effetto colora l'immagine di origine moltiplicando l'immagine di origine in base al colore specificato. Ha un singolo input.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964149"
---
# <a name="tint-effect"></a><span data-ttu-id="c5451-104">Effetto tinta</span><span class="sxs-lookup"><span data-stu-id="c5451-104">Tint effect</span></span>

<span data-ttu-id="c5451-105">Questo effetto colora l'immagine di origine moltiplicando l'immagine di origine in base al colore specificato.</span><span class="sxs-lookup"><span data-stu-id="c5451-105">This effect tints the source image by multiplying the source image by the specified color.</span></span> <span data-ttu-id="c5451-106">Ha un singolo input.</span><span class="sxs-lookup"><span data-stu-id="c5451-106">It has a single input.</span></span>

<span data-ttu-id="c5451-107">Il CLSID per questo effetto è CLSID \_ D2D1Tint.</span><span class="sxs-lookup"><span data-stu-id="c5451-107">The CLSID for this effect is CLSID\_D2D1Tint.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="c5451-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="c5451-108">Effect properties</span></span>



| <span data-ttu-id="c5451-109">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="c5451-109">Display name and index enumeration</span></span>                    | <span data-ttu-id="c5451-110">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="c5451-110">Type and default value</span></span>                              | <span data-ttu-id="c5451-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5451-111">Description</span></span>                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c5451-112">\_Colore della \_ prop tinta ColorD2D1 \_</span><span class="sxs-lookup"><span data-stu-id="c5451-112">ColorD2D1\_TINT\_PROP\_COLOR</span></span><br/>               | <span data-ttu-id="c5451-113">D2D1 \_ vector \_ 4F (1.0 f, 1.0 f, 1.0 f, 1.0 f)</span><span class="sxs-lookup"><span data-stu-id="c5451-113">D2D1\_VECTOR\_4F(1.0f, 1.0f, 1.0f, 1.0f)</span></span><br/> | <span data-ttu-id="c5451-114">I colori dell'immagine di origine vengono moltiplicati per questo valore.</span><span class="sxs-lookup"><span data-stu-id="c5451-114">Colors from the source image are multiplied by this value.</span></span>       |
| <span data-ttu-id="c5451-115">\_Output morsetto ClampOutputD2D1 tinta \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="c5451-115">ClampOutputD2D1\_TINT\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="c5451-116">BOOLFALSE</span><span class="sxs-lookup"><span data-stu-id="c5451-116">BOOLFALSE</span></span><br/>                                | <span data-ttu-id="c5451-117">Indica se bloccare o meno i valori di output nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="c5451-117">Whether or not to clamp the output values to the range \[0, 1\].</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c5451-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5451-118">Requirements</span></span>



| <span data-ttu-id="c5451-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5451-119">Requirement</span></span> | <span data-ttu-id="c5451-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c5451-120">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="c5451-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5451-121">Minimum supported client</span></span> | <span data-ttu-id="c5451-122">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c5451-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c5451-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5451-123">Minimum supported server</span></span> | <span data-ttu-id="c5451-124">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c5451-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c5451-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5451-125">Header</span></span>                   | <span data-ttu-id="c5451-126">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="c5451-126">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="c5451-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="c5451-127">Library</span></span>                  | <span data-ttu-id="c5451-128">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="c5451-128">d2d1.lib, dxguid.lib</span></span>                              |



 ## <a name="related-topics"></a><span data-ttu-id="c5451-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5451-129">Related topics</span></span>

* [<span data-ttu-id="c5451-130">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="c5451-130">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
