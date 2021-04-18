---
title: Metodo query. beginNextGroup
description: Il metodo beginNextGroup avvia un nuovo gruppo di condizioni. | Metodo query. beginNextGroup
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- Metodo beginNextGroup Windows Media Player
- Metodo beginNextGroup Media Player Windows, classe query
- Classe di query Windows Media Player, metodo beginNextGroup
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c043b9a0ea506e054877b4d8122304ced75e28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331220"
---
# <a name="querybeginnextgroup-method"></a><span data-ttu-id="e1b0e-107">Metodo query. beginNextGroup</span><span class="sxs-lookup"><span data-stu-id="e1b0e-107">Query.beginNextGroup method</span></span>

<span data-ttu-id="e1b0e-108">Il metodo **beginNextGroup** avvia un nuovo gruppo di condizioni.</span><span class="sxs-lookup"><span data-stu-id="e1b0e-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b0e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1b0e-109">Syntax</span></span>


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a><span data-ttu-id="e1b0e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1b0e-110">Parameters</span></span>

<span data-ttu-id="e1b0e-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e1b0e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1b0e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1b0e-112">Return value</span></span>

<span data-ttu-id="e1b0e-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e1b0e-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b0e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1b0e-114">Remarks</span></span>

<span data-ttu-id="e1b0e-115">L'inizio di un nuovo gruppo di condizioni implica il completamento del gruppo di condizioni corrente.</span><span class="sxs-lookup"><span data-stu-id="e1b0e-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="e1b0e-116">Il nuovo gruppo di condizioni viene sempre concatenato al gruppo di condizioni precedente mediante la logica o.</span><span class="sxs-lookup"><span data-stu-id="e1b0e-116">The new condition group is always concatenated to the previous condition group using OR logic.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b0e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1b0e-117">Requirements</span></span>



| <span data-ttu-id="e1b0e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1b0e-118">Requirement</span></span> | <span data-ttu-id="e1b0e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e1b0e-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b0e-120">Versione</span><span class="sxs-lookup"><span data-stu-id="e1b0e-120">Version</span></span><br/> | <span data-ttu-id="e1b0e-121">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="e1b0e-121">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="e1b0e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e1b0e-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1b0e-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1b0e-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1b0e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1b0e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b0e-125">**Mediacollection. createQuery**</span><span class="sxs-lookup"><span data-stu-id="e1b0e-125">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="e1b0e-126">**Mediacollection. getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="e1b0e-126">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="e1b0e-127">**Mediacollection. getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="e1b0e-127">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="e1b0e-128">**Oggetto query**</span><span class="sxs-lookup"><span data-stu-id="e1b0e-128">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="e1b0e-129">**Query. addCondition**</span><span class="sxs-lookup"><span data-stu-id="e1b0e-129">**Query.addCondition**</span></span>](query-addcondition.md)
</dt> </dl>

 

 





