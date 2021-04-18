---
title: TESTO. scorrimento
description: L'attributo di scorrimento specifica o recupera un valore che indica se lo scorrimento del testo viene eseguito.
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- TESTO. scorrimento di Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328589"
---
# <a name="textscrolling"></a><span data-ttu-id="34d42-104">TESTO. scorrimento</span><span class="sxs-lookup"><span data-stu-id="34d42-104">TEXT.scrolling</span></span>

<span data-ttu-id="34d42-105">L'attributo di **scorrimento** specifica o recupera un valore che indica se lo scorrimento del testo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34d42-105">The **scrolling** attribute specifies or retrieves a value indicating whether the text scrolls.</span></span>

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a><span data-ttu-id="34d42-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="34d42-106">Possible Values</span></span>

<span data-ttu-id="34d42-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="34d42-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="34d42-108">Valore</span><span class="sxs-lookup"><span data-stu-id="34d42-108">Value</span></span> | <span data-ttu-id="34d42-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34d42-109">Description</span></span>                     |
|-------|---------------------------------|
| <span data-ttu-id="34d42-110">true</span><span class="sxs-lookup"><span data-stu-id="34d42-110">true</span></span>  | <span data-ttu-id="34d42-111">Lo scorrimento è abilitato.</span><span class="sxs-lookup"><span data-stu-id="34d42-111">Scrolling is enabled.</span></span>           |
| <span data-ttu-id="34d42-112">false</span><span class="sxs-lookup"><span data-stu-id="34d42-112">false</span></span> | <span data-ttu-id="34d42-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="34d42-113">Default.</span></span> <span data-ttu-id="34d42-114">Lo scorrimento è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="34d42-114">Scrolling is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="34d42-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="34d42-115">Remarks</span></span>

<span data-ttu-id="34d42-116">La funzionalità di scorrimento fornisce un buffer di due spazi tra la fine del testo e l'inizio della riga ripetuta.</span><span class="sxs-lookup"><span data-stu-id="34d42-116">The scrolling feature provides a two-space buffer between the end of the text and the beginning of the repeated line.</span></span>

<span data-ttu-id="34d42-117">L'attributo **giustificazione** specifica il punto in cui il testo viene visualizzato prima dell'inizio dello scorrimento.</span><span class="sxs-lookup"><span data-stu-id="34d42-117">The **justification** attribute specifies where the text first appears before the scrolling begins.</span></span>

<span data-ttu-id="34d42-118">Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .</span><span class="sxs-lookup"><span data-stu-id="34d42-118">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="34d42-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34d42-119">Requirements</span></span>



| <span data-ttu-id="34d42-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="34d42-120">Requirement</span></span> | <span data-ttu-id="34d42-121">Valore</span><span class="sxs-lookup"><span data-stu-id="34d42-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="34d42-122">Versione</span><span class="sxs-lookup"><span data-stu-id="34d42-122">Version</span></span><br/> | <span data-ttu-id="34d42-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="34d42-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34d42-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34d42-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34d42-125">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="34d42-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="34d42-126">**TESTO. giustificazione**</span><span class="sxs-lookup"><span data-stu-id="34d42-126">**TEXT.justification**</span></span>](text-justification.md)
</dt> <dt>

[<span data-ttu-id="34d42-127">**TESTO. scrollingAmount**</span><span class="sxs-lookup"><span data-stu-id="34d42-127">**TEXT.scrollingAmount**</span></span>](text-scrollingamount.md)
</dt> <dt>

[<span data-ttu-id="34d42-128">**TESTO. scrollingDelay**</span><span class="sxs-lookup"><span data-stu-id="34d42-128">**TEXT.scrollingDelay**</span></span>](text-scrollingdelay.md)
</dt> <dt>

[<span data-ttu-id="34d42-129">**TESTO. scrollingDirection**</span><span class="sxs-lookup"><span data-stu-id="34d42-129">**TEXT.scrollingDirection**</span></span>](text-scrollingdirection.md)
</dt> </dl>

 

 





