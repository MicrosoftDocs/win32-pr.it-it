---
description: Effetto Setter Alpha
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Effetto Setter Alpha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746370"
---
# <a name="alpha-setter-effect"></a><span data-ttu-id="b1eab-103">Effetto Setter Alpha</span><span class="sxs-lookup"><span data-stu-id="b1eab-103">Alpha Setter Effect</span></span>

> [!Note]  
> <span data-ttu-id="b1eab-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b1eab-104">\[Deprecated.</span></span> <span data-ttu-id="b1eab-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b1eab-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b1eab-106">L'effetto Alpha Setter imposta i bit alfa su un'immagine video.</span><span class="sxs-lookup"><span data-stu-id="b1eab-106">The Alpha Setter effect sets the alpha bits on a video image.</span></span>

<span data-ttu-id="b1eab-107">ID classe (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}</span><span class="sxs-lookup"><span data-stu-id="b1eab-107">Class ID (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}</span></span>

<span data-ttu-id="b1eab-108">Nome variabile CLSID: CLSID \_ DxtAlphaSetter</span><span class="sxs-lookup"><span data-stu-id="b1eab-108">CLSID Variable Name: CLSID\_DxtAlphaSetter</span></span>

<span data-ttu-id="b1eab-109">Nome descrittivo: "DxtAlphaSetter"</span><span class="sxs-lookup"><span data-stu-id="b1eab-109">Friendly Name: "DxtAlphaSetter"</span></span>

### <a name="properties"></a><span data-ttu-id="b1eab-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1eab-110">Properties</span></span>



| <span data-ttu-id="b1eab-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b1eab-111">Property</span></span>  | <span data-ttu-id="b1eab-112">Type</span><span class="sxs-lookup"><span data-stu-id="b1eab-112">Type</span></span>   | <span data-ttu-id="b1eab-113">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b1eab-113">Default</span></span> | <span data-ttu-id="b1eab-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1eab-114">Description</span></span>                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| <span data-ttu-id="b1eab-115">Alfa</span><span class="sxs-lookup"><span data-stu-id="b1eab-115">Alpha</span></span>     | <span data-ttu-id="b1eab-116">BYTE</span><span class="sxs-lookup"><span data-stu-id="b1eab-116">BYTE</span></span>   | <span data-ttu-id="b1eab-117">-1</span><span class="sxs-lookup"><span data-stu-id="b1eab-117">-1</span></span>      | <span data-ttu-id="b1eab-118">Imposta l'alfa per l'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="b1eab-118">Sets the alpha for the entire image.</span></span>                        |
| <span data-ttu-id="b1eab-119">AlphaRamp</span><span class="sxs-lookup"><span data-stu-id="b1eab-119">AlphaRamp</span></span> | <span data-ttu-id="b1eab-120">double</span><span class="sxs-lookup"><span data-stu-id="b1eab-120">double</span></span> | <span data-ttu-id="b1eab-121">-1.0</span><span class="sxs-lookup"><span data-stu-id="b1eab-121">-1.0</span></span>    | <span data-ttu-id="b1eab-122">Imposta l'alfa come percentuale del valore alfa originale.</span><span class="sxs-lookup"><span data-stu-id="b1eab-122">Sets the alpha as a percentage of the original alpha value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b1eab-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1eab-123">Remarks</span></span>

<span data-ttu-id="b1eab-124">Una proprietà con un valore negativo viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="b1eab-124">A property with a negative value is ignored.</span></span> <span data-ttu-id="b1eab-125">Una sola proprietà può avere un valore non negativo.</span><span class="sxs-lookup"><span data-stu-id="b1eab-125">Only one property can have a non-negative value.</span></span> <span data-ttu-id="b1eab-126">La proprietà Alpha specifica un valore alfa costante per ogni pixel nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b1eab-126">The Alpha property specifies a constant alpha value for every pixel in the image.</span></span> <span data-ttu-id="b1eab-127">Questa proprietà sovrascrive i valori alfa dall'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="b1eab-127">This property overwrites the alpha values from the original image.</span></span> <span data-ttu-id="b1eab-128">La proprietà AlphaRamp specifica il valore alfa di ogni pixel come percentuale del valore originale del pixel, da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="b1eab-128">The AlphaRamp property specifies each pixel's alpha value as a percentage of the pixel's original value, from 0.0 to 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1eab-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1eab-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1eab-130">Fusione alfa</span><span class="sxs-lookup"><span data-stu-id="b1eab-130">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



