---
title: Attributi con più valori (Windows Media Player SDK)
description: Attributi con più valori
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Media Player di Windows, attributi per elementi multimediali
- Modello a oggetti di Windows Media Player, attributi per elementi multimediali
- modello a oggetti, attributi per elementi multimediali
- Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX di Windows Media Player, attributi per elementi multimediali
- Controllo ActiveX Windows Media Player Mobile, attributi per elementi multimediali
- Controllo ActiveX, attributi per elementi multimediali
- Windows Media Player Library, attributi per elementi multimediali
- libreria, attributi per elementi multimediali
- attributi, più valori
- più valori di attributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad93c4025d09a234b1834a32e4ca3789bcaa4a35
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400154"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a><span data-ttu-id="cfc06-114">Attributi con più valori (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="cfc06-114">Attributes with Multiple Values (Windows Media Player SDK)</span></span>

<span data-ttu-id="cfc06-115">Alcuni attributi dell'elemento multimediale possono avere più valori.</span><span class="sxs-lookup"><span data-stu-id="cfc06-115">Some media item attributes can have multiple values.</span></span> <span data-ttu-id="cfc06-116">Ad esempio, gli attributi **Author**, **WM/Composer** e **WM/genre** possono avere più di un valore.</span><span class="sxs-lookup"><span data-stu-id="cfc06-116">For example, the **Author**, **WM/Composer**, and **WM/Genre** attributes can each have more than one value.</span></span> <span data-ttu-id="cfc06-117">Il tipo di dati di tali attributi è costituito da una **stringa multivalore**.</span><span class="sxs-lookup"><span data-stu-id="cfc06-117">The data type of such attributes is **multi-valued string**.</span></span>

<span data-ttu-id="cfc06-118">In Windows Media Player la libreria Visualizza più valori in un singolo campo, separando i valori con un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="cfc06-118">In Windows Media Player, the library displays multiple values in a single field, separating the values with semicolons.</span></span> <span data-ttu-id="cfc06-119">Tuttavia, ogni valore è effettivamente un attributo separato nell'elemento multimediale di Windows.</span><span class="sxs-lookup"><span data-stu-id="cfc06-119">However, each value is actually a separate attribute in the Windows Media item.</span></span>

<span data-ttu-id="cfc06-120">È possibile scrivere codice per determinare se un attributo specificato dispone di più valori e quindi recuperare tutti questi valori.</span><span class="sxs-lookup"><span data-stu-id="cfc06-120">You can write code that will determine whether a given attribute has multiple values and then retrieve all of those values.</span></span> <span data-ttu-id="cfc06-121">È necessario utilizzare *supporti*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="cfc06-121">You must use *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="cfc06-122">Se si usa il *supporto*. metodo **GetItemInfo** per recuperare un attributo multivalore, si recupererà solo il primo valore.</span><span class="sxs-lookup"><span data-stu-id="cfc06-122">If you use the *Media*.**getItemInfo** method to retrieve a multi-valued attribute, you will only retrieve the first value.</span></span>

<span data-ttu-id="cfc06-123">Nell'esempio finale nell'argomento [Reading attribute values](reading-attribute-values.md) viene illustrato l'utilizzo del *supporto*. **getAttributeCountByType** e *supporti*. metodi **getItemInfoByType** per recuperare più valori per un attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="cfc06-123">The final example in the [Reading Attribute Values](reading-attribute-values.md) topic demonstrates the use of the *Media*.**getAttributeCountByType** and *Media*.**getItemInfoByType** methods to retrieve multiple values for a given attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfc06-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cfc06-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfc06-125">**Attributi elemento multimediale**</span><span class="sxs-lookup"><span data-stu-id="cfc06-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="cfc06-126">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="cfc06-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="cfc06-127">**Lettura di valori di attributo da un CD o DVD**</span><span class="sxs-lookup"><span data-stu-id="cfc06-127">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




