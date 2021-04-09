---
title: Effetto scala di grigi
description: Converte un'immagine in grigio monocromatico.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc3cb6a807d282649a2826713cdf48fa966d9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741970"
---
# <a name="grayscale-effect"></a><span data-ttu-id="f69b4-103">Effetto scala di grigi</span><span class="sxs-lookup"><span data-stu-id="f69b4-103">Grayscale effect</span></span>

<span data-ttu-id="f69b4-104">Converte un'immagine in grigio monocromatico.</span><span class="sxs-lookup"><span data-stu-id="f69b4-104">Converts an image to monochromatic gray.</span></span>

<span data-ttu-id="f69b4-105">La scala di grigi usa l'effetto della matrice di colori per la conversione in scala di grigi, usando la matrice seguente:</span><span class="sxs-lookup"><span data-stu-id="f69b4-105">Grayscale uses the color matrix effect to convert to grayscale, using the following matrix:</span></span>

![matrice di conversione](images/grayscale-effect-matrix.png)

<span data-ttu-id="f69b4-107">Il CLSID per questo effetto è CLSID \_ D2D1Grayscale.</span><span class="sxs-lookup"><span data-stu-id="f69b4-107">The CLSID for this effect is CLSID\_D2D1Grayscale.</span></span>

-   [<span data-ttu-id="f69b4-108">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="f69b4-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="f69b4-109">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="f69b4-109">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="f69b4-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f69b4-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f69b4-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f69b4-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="f69b4-112">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="f69b4-112">Example image</span></span>

![esempio di output di effetto](images/grayscale-effect.png)

## <a name="effect-properties"></a><span data-ttu-id="f69b4-114">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="f69b4-114">Effect properties</span></span>

<span data-ttu-id="f69b4-115">Questo effetto non ha proprietà.</span><span class="sxs-lookup"><span data-stu-id="f69b4-115">This effect has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="f69b4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f69b4-116">Requirements</span></span>



| <span data-ttu-id="f69b4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f69b4-117">Requirement</span></span> | <span data-ttu-id="f69b4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f69b4-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="f69b4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f69b4-119">Minimum supported client</span></span> | <span data-ttu-id="f69b4-120">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="f69b4-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f69b4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f69b4-121">Minimum supported server</span></span> | <span data-ttu-id="f69b4-122">App \[ Windows 10 desktop app \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="f69b4-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f69b4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f69b4-123">Header</span></span>                   | <span data-ttu-id="f69b4-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="f69b4-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="f69b4-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f69b4-125">Library</span></span>                  | <span data-ttu-id="f69b4-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="f69b4-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="f69b4-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f69b4-127">Related topics</span></span>

* [<span data-ttu-id="f69b4-128">Interfaccia ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="f69b4-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
