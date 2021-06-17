---
title: Attributi con più valori (Windows Media Player SDK)
description: Informazioni sugli attributi con più valori in Windows Media Player SDK. Alcuni attributi dell'elemento multimediale possono avere più valori.
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Windows Media Player,attributi per elementi multimediali
- Windows Media Player a oggetti, attributi per elementi multimediali
- modello a oggetti,attributi per elementi multimediali
- Windows Media Player Mobile, attributi per elementi multimediali
- Windows Media Player controllo ActiveX, attributi per elementi multimediali
- Windows Media Player controllo ActiveX mobile, attributi per elementi multimediali
- Controllo ActiveX,attributi per elementi multimediali
- Windows Media Player,attributi per elementi multimediali
- libreria,attributi per elementi multimediali
- attributi,più valori
- più valori di attributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16baf4bab47dc972ec7b043980dccb0f2aadd57
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262603"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a><span data-ttu-id="51762-115">Attributi con più valori (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="51762-115">Attributes with Multiple Values (Windows Media Player SDK)</span></span>

<span data-ttu-id="51762-116">Alcuni attributi dell'elemento multimediale possono avere più valori.</span><span class="sxs-lookup"><span data-stu-id="51762-116">Some media item attributes can have multiple values.</span></span> <span data-ttu-id="51762-117">Ad esempio, gli **attributi Author**, **WM/Composer** e **WM/Genre** possono avere più di un valore.</span><span class="sxs-lookup"><span data-stu-id="51762-117">For example, the **Author**, **WM/Composer**, and **WM/Genre** attributes can each have more than one value.</span></span> <span data-ttu-id="51762-118">Il tipo di dati di tali attributi è **stringa multivalore**.</span><span class="sxs-lookup"><span data-stu-id="51762-118">The data type of such attributes is **multi-valued string**.</span></span>

<span data-ttu-id="51762-119">In Windows Media Player la libreria visualizza più valori in un singolo campo, separandoli con punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="51762-119">In Windows Media Player, the library displays multiple values in a single field, separating the values with semicolons.</span></span> <span data-ttu-id="51762-120">Tuttavia, ogni valore è in realtà un attributo separato nell'elemento di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="51762-120">However, each value is actually a separate attribute in the Windows Media item.</span></span>

<span data-ttu-id="51762-121">È possibile scrivere codice che determinerà se un determinato attributo ha più valori e quindi recupera tutti questi valori.</span><span class="sxs-lookup"><span data-stu-id="51762-121">You can write code that will determine whether a given attribute has multiple values and then retrieve all of those values.</span></span> <span data-ttu-id="51762-122">È necessario usare *Media*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="51762-122">You must use *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="51762-123">Se si usa l'oggetto *Media*. **metodo getItemInfo** per recuperare un attributo multivalore, si recupererà solo il primo valore.</span><span class="sxs-lookup"><span data-stu-id="51762-123">If you use the *Media*.**getItemInfo** method to retrieve a multi-valued attribute, you will only retrieve the first value.</span></span>

<span data-ttu-id="51762-124">L'esempio finale [nell'argomento Reading Attribute Values](reading-attribute-values.md) (Lettura dei valori degli attributi) illustra l'uso di *Media*. **getAttributeCountByType** e *Media*. **Metodi getItemInfoByType** per recuperare più valori per un determinato attributo.</span><span class="sxs-lookup"><span data-stu-id="51762-124">The final example in the [Reading Attribute Values](reading-attribute-values.md) topic demonstrates the use of the *Media*.**getAttributeCountByType** and *Media*.**getItemInfoByType** methods to retrieve multiple values for a given attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51762-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="51762-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51762-126">**Attributi dell'elemento multimediale**</span><span class="sxs-lookup"><span data-stu-id="51762-126">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="51762-127">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="51762-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="51762-128">**Lettura dei valori degli attributi da un CD o dvd**</span><span class="sxs-lookup"><span data-stu-id="51762-128">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




