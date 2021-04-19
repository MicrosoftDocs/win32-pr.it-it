---
title: TESTO. scrollingDelay
description: L'attributo scrollingDelay specifica o recupera l'intervallo di tempo tra i movimenti di scorrimento.
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- Media Player di Windows TEXT. scrollingDelay
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328585"
---
# <a name="textscrollingdelay"></a><span data-ttu-id="194b5-104">TESTO. scrollingDelay</span><span class="sxs-lookup"><span data-stu-id="194b5-104">TEXT.scrollingDelay</span></span>

<span data-ttu-id="194b5-105">L'attributo **scrollingDelay** specifica o recupera l'intervallo di tempo tra i movimenti di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="194b5-105">The **scrollingDelay** attribute specifies or retrieves the time delay between scrolling movements.</span></span>

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a><span data-ttu-id="194b5-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="194b5-106">Possible Values</span></span>

<span data-ttu-id="194b5-107">Questo attributo è un **numero** di lettura/scrittura (**int**) che specifica il ritardo in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="194b5-107">This attribute is a read/write **Number** (**int**) specifying the delay in milliseconds.</span></span> <span data-ttu-id="194b5-108">Il valore minimo è 30 e il valore predefinito è 85.</span><span class="sxs-lookup"><span data-stu-id="194b5-108">It has a minimum value of 30, and a default value of 85.</span></span> <span data-ttu-id="194b5-109">Se viene specificato un valore minore del valore minimo, viene usato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="194b5-109">If a value less than the minimum is specified, the default is used.</span></span>

## <a name="remarks"></a><span data-ttu-id="194b5-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="194b5-110">Remarks</span></span>

<span data-ttu-id="194b5-111">Se lo **scorrimento** è impostato su false, **scrollingDelay** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="194b5-111">If **scrolling** is set to false, **scrollingDelay** is ignored.</span></span>

<span data-ttu-id="194b5-112">Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .</span><span class="sxs-lookup"><span data-stu-id="194b5-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="194b5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="194b5-113">Requirements</span></span>



| <span data-ttu-id="194b5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="194b5-114">Requirement</span></span> | <span data-ttu-id="194b5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="194b5-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="194b5-116">Versione</span><span class="sxs-lookup"><span data-stu-id="194b5-116">Version</span></span><br/> | <span data-ttu-id="194b5-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="194b5-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="194b5-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="194b5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194b5-119">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="194b5-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="194b5-120">**TESTO. scorrimento**</span><span class="sxs-lookup"><span data-stu-id="194b5-120">**TEXT.scrolling**</span></span>](text-scrolling.md)
</dt> </dl>

 

 





