---
title: CUSTOMSLIDER. Value
description: L'attributo value specifica o recupera la posizione corrente del dispositivo di scorrimento. | CUSTOMSLIDER. Value
ms.assetid: 29e17f48-1848-458d-9da4-316013b21980
keywords:
- Media Player di Windows CUSTOMSLIDER. Value
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89be4edd43fc79c8a8938a3861c982068760bcf3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331747"
---
# <a name="customslidervalue"></a><span data-ttu-id="2090d-105">CUSTOMSLIDER. Value</span><span class="sxs-lookup"><span data-stu-id="2090d-105">CUSTOMSLIDER.value</span></span>

<span data-ttu-id="2090d-106">L'attributo **value** specifica o recupera la posizione corrente del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="2090d-106">The **value** attribute specifies or retrieves the current position of the slider.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="2090d-107">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="2090d-107">Possible Values</span></span>

<span data-ttu-id="2090d-108">Questo attributo è un **numero** di lettura/scrittura (**float**) con un valore predefinito uguale all'attributo **min** .</span><span class="sxs-lookup"><span data-stu-id="2090d-108">This attribute is a read/write **Number** (**float**) with a default value equal to the **min** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="2090d-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="2090d-109">Remarks</span></span>

<span data-ttu-id="2090d-110">Il **valore** deve essere maggiore o uguale a **min** e minore o uguale a **Max**. Se il valore non rientra nell'intervallo, viene generato un avviso e il valore non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="2090d-110">The **value** must be greater than or equal to **min** and less than or equal to **max**. If the value falls outside the range, a warning is issued, and the value does not change.</span></span>

## <a name="examples"></a><span data-ttu-id="2090d-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="2090d-111">Examples</span></span>

<span data-ttu-id="2090d-112">Vedere l'attributo [dimensione positionImage](customslider-positionimage.md) per un esempio che illustra come vengono usati gli attributi dell'elemento **CUSTOMSLIDER** .</span><span class="sxs-lookup"><span data-stu-id="2090d-112">See the [positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **CUSTOMSLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2090d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2090d-113">Requirements</span></span>



| <span data-ttu-id="2090d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2090d-114">Requirement</span></span> | <span data-ttu-id="2090d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2090d-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2090d-116">Versione</span><span class="sxs-lookup"><span data-stu-id="2090d-116">Version</span></span><br/> | <span data-ttu-id="2090d-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="2090d-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2090d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2090d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2090d-119">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="2090d-119">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> </dl>

 

 





