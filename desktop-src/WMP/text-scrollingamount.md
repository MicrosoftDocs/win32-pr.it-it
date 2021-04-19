---
title: TESTO. scrollingAmount
description: L'attributo scrollingAmount specifica o Recupera il numero di pixel spostati dal testo durante ogni spostamento dello scorrimento.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- Media Player di Windows TEXT. scrollingAmount
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328587"
---
# <a name="textscrollingamount"></a><span data-ttu-id="f3548-104">TESTO. scrollingAmount</span><span class="sxs-lookup"><span data-stu-id="f3548-104">TEXT.scrollingAmount</span></span>

<span data-ttu-id="f3548-105">L'attributo **scrollingAmount** specifica o Recupera il numero di pixel spostati dal testo durante ogni spostamento dello scorrimento.</span><span class="sxs-lookup"><span data-stu-id="f3548-105">The **scrollingAmount** attribute specifies or retrieves the number of pixels that the text moves during each scrolling movement.</span></span>

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a><span data-ttu-id="f3548-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="f3548-106">Possible Values</span></span>

<span data-ttu-id="f3548-107">Questo attributo è un **numero** di lettura/scrittura positivo (**int**) con un valore predefinito di 6.</span><span class="sxs-lookup"><span data-stu-id="f3548-107">This attribute is a positive read/write **Number** (**int**) with a default value of 6.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3548-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3548-108">Remarks</span></span>

<span data-ttu-id="f3548-109">Per lo scorrimento uniforme, **scrollingAmount** deve essere di dimensioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="f3548-109">For smooth scrolling, **scrollingAmount** should be small.</span></span> <span data-ttu-id="f3548-110">Per il disegno veloce con grandi Gap, il **scrollingAmount** deve essere più grande.</span><span class="sxs-lookup"><span data-stu-id="f3548-110">For fast drawing with big gaps, the **scrollingAmount** should be larger.</span></span> <span data-ttu-id="f3548-111">Se lo **scorrimento** è "false", **scrollingAmount** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f3548-111">If **scrolling** ="false", **scrollingAmount** is ignored.</span></span>

<span data-ttu-id="f3548-112">Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .</span><span class="sxs-lookup"><span data-stu-id="f3548-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3548-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3548-113">Requirements</span></span>



| <span data-ttu-id="f3548-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3548-114">Requirement</span></span> | <span data-ttu-id="f3548-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f3548-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f3548-116">Versione</span><span class="sxs-lookup"><span data-stu-id="f3548-116">Version</span></span><br/> | <span data-ttu-id="f3548-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="f3548-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3548-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3548-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3548-119">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="f3548-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="f3548-120">**TESTO. scorrimento**</span><span class="sxs-lookup"><span data-stu-id="f3548-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





