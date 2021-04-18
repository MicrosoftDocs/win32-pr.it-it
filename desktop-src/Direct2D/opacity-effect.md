---
title: Effetto opacità
description: Questo effetto regola l'opacità di un'immagine moltiplicando il canale alfa dell'input in base al valore di opacità specificato. Ha un singolo input.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302034"
---
# <a name="opacity-effect"></a><span data-ttu-id="c87a1-104">Effetto opacità</span><span class="sxs-lookup"><span data-stu-id="c87a1-104">Opacity effect</span></span>

<span data-ttu-id="c87a1-105">Questo effetto regola l'opacità di un'immagine moltiplicando il canale alfa dell'input in base al valore di opacità specificato.</span><span class="sxs-lookup"><span data-stu-id="c87a1-105">This effect adjusts the opacity of an image by multiplying the alpha channel of the input by the specified opacity value.</span></span> <span data-ttu-id="c87a1-106">Ha un singolo input.</span><span class="sxs-lookup"><span data-stu-id="c87a1-106">It has a single input.</span></span>

<span data-ttu-id="c87a1-107">Il CLSID per questo effetto è CLSID \_ D2D1Opacity.</span><span class="sxs-lookup"><span data-stu-id="c87a1-107">The CLSID for this effect is CLSID\_D2D1Opacity.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="c87a1-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="c87a1-108">Effect properties</span></span>



| <span data-ttu-id="c87a1-109">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="c87a1-109">Display name and index enumeration</span></span>              | <span data-ttu-id="c87a1-110">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="c87a1-110">Type and default value</span></span> | <span data-ttu-id="c87a1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c87a1-111">Description</span></span>                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c87a1-112">Opacità \_ della \_ prop \_ Opacity d2d1 Opacity</span><span class="sxs-lookup"><span data-stu-id="c87a1-112">Opacity D2D1\_OPACITY\_PROP\_OPACITY</span></span><br/> | <span data-ttu-id="c87a1-113">FLOAT 1.0 f</span><span class="sxs-lookup"><span data-stu-id="c87a1-113">FLOAT1.0f</span></span><br/>   | <span data-ttu-id="c87a1-114">Moltiplicatore per il canale alfa dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="c87a1-114">The multiplier to the input image's alpha channel.</span></span> <span data-ttu-id="c87a1-115">Il valore minimo è 0,0 f e il valore massimo è 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="c87a1-115">The minimum value is 0.0f and the maximum value is 1.0f.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c87a1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c87a1-116">Requirements</span></span>



| <span data-ttu-id="c87a1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c87a1-117">Requirement</span></span> | <span data-ttu-id="c87a1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c87a1-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="c87a1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c87a1-119">Minimum supported client</span></span> | <span data-ttu-id="c87a1-120">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c87a1-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c87a1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c87a1-121">Minimum supported server</span></span> | <span data-ttu-id="c87a1-122">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="c87a1-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c87a1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c87a1-123">Header</span></span>                   | <span data-ttu-id="c87a1-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="c87a1-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="c87a1-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="c87a1-125">Library</span></span>                  | <span data-ttu-id="c87a1-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="c87a1-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="c87a1-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c87a1-127">Related topics</span></span>

* [<span data-ttu-id="c87a1-128">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="c87a1-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
