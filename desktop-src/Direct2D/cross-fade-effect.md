---
title: Effetto dissolvenza incrociata
description: Questo effetto combina due immagini aggiungendo pixel ponderati dalle immagini di input. Dispone di due input, denominato destinazione e origine.
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517728"
---
# <a name="cross-fade-effect"></a><span data-ttu-id="ac15f-104">Effetto dissolvenza incrociata</span><span class="sxs-lookup"><span data-stu-id="ac15f-104">Cross-fade effect</span></span>

<span data-ttu-id="ac15f-105">Questo effetto combina due immagini aggiungendo pixel ponderati dalle immagini di input.</span><span class="sxs-lookup"><span data-stu-id="ac15f-105">This effect combines two images by adding weighted pixels from input images.</span></span> <span data-ttu-id="ac15f-106">Dispone di due input, denominato destinazione e origine.</span><span class="sxs-lookup"><span data-stu-id="ac15f-106">It has two inputs, named Destination and Source.</span></span>

<span data-ttu-id="ac15f-107">La formula Cross Fade è **output = Weight \* Destination + (1-Weight) \* source**.</span><span class="sxs-lookup"><span data-stu-id="ac15f-107">The cross fade formula is **output = weight \* Destination + (1 - weight) \* Source**.</span></span>

<span data-ttu-id="ac15f-108">Il CLSID per questo effetto è CLSID \_ D2D1CrossFade.</span><span class="sxs-lookup"><span data-stu-id="ac15f-108">The CLSID for this effect is CLSID\_D2D1CrossFade.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="ac15f-109">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="ac15f-109">Effect properties</span></span>

| <span data-ttu-id="ac15f-110">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="ac15f-110">Display name and index enumeration</span></span>             | <span data-ttu-id="ac15f-111">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="ac15f-111">Type and default value</span></span> | <span data-ttu-id="ac15f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac15f-112">Description</span></span>                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac15f-113">\_Peso della \_ prop incrociata WeightD2D1 \_</span><span class="sxs-lookup"><span data-stu-id="ac15f-113">WeightD2D1\_CROSSFADE\_PROP\_WEIGHT</span></span><br/> | <span data-ttu-id="ac15f-114">FLOAT 0,5 f</span><span class="sxs-lookup"><span data-stu-id="ac15f-114">FLOAT0.5f</span></span><br/>   | <span data-ttu-id="ac15f-115">Quanto pesare i valori dei colori dell'immagine di origine rispetto all'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ac15f-115">How much to weigh the source image color values versus the destination image.</span></span> <span data-ttu-id="ac15f-116">Il valore minimo è 0,0 f (usare esclusivamente l'immagine di destinazione per determinare l'output) e il valore massimo è 1,0 f (usare esclusivamente l'immagine di origine per determinare l'output).</span><span class="sxs-lookup"><span data-stu-id="ac15f-116">The minimum value is 0.0f (exclusively use the destination image to determine the output) and the maximum value is 1.0f (exclusively use the source image to determine the output).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ac15f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac15f-117">Requirements</span></span>



| <span data-ttu-id="ac15f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac15f-118">Requirement</span></span> | <span data-ttu-id="ac15f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ac15f-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="ac15f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac15f-120">Minimum supported client</span></span> | <span data-ttu-id="ac15f-121">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ac15f-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ac15f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac15f-122">Minimum supported server</span></span> | <span data-ttu-id="ac15f-123">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ac15f-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ac15f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac15f-124">Header</span></span>                   | <span data-ttu-id="ac15f-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="ac15f-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="ac15f-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="ac15f-126">Library</span></span>                  | <span data-ttu-id="ac15f-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ac15f-127">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="ac15f-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ac15f-128">Related topics</span></span>

* [<span data-ttu-id="ac15f-129">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="ac15f-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
