---
title: PLAYLIST. getNextCheckedItem2
description: Il metodo getNextCheckedItem2 recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- PLAYLIST. getNextCheckedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324732"
---
# <a name="playlistgetnextcheckeditem2"></a><span data-ttu-id="33414-104">PLAYLIST. getNextCheckedItem2</span><span class="sxs-lookup"><span data-stu-id="33414-104">PLAYLIST.getNextCheckedItem2</span></span>

<span data-ttu-id="33414-105">Il metodo **getNextCheckedItem2** recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="33414-105">The **getNextCheckedItem2** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="33414-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="33414-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33414-107"><span id="item"></span><span id="ITEM"></span>*elemento*</span><span class="sxs-lookup"><span data-stu-id="33414-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="33414-108">**Numero** (**Long**) che indica l'indice dell'elemento in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="33414-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33414-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33414-109">Return Value</span></span>

<span data-ttu-id="33414-110">Questo metodo restituisce un **numero** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="33414-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="33414-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="33414-111">Remarks</span></span>

<span data-ttu-id="33414-112">Questo metodo può funzionare con playlist annidate e sostituisce il metodo **getNextCheckedItem** , che non può.</span><span class="sxs-lookup"><span data-stu-id="33414-112">This method can work with nested playlists and replaces the **getNextCheckedItem** method, which cannot.</span></span> <span data-ttu-id="33414-113">Passare 1 nel parametro *Item* per trovare il primo elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="33414-113">Pass  1 in the *item* parameter to find the first checked item.</span></span> <span data-ttu-id="33414-114">Quando non sono presenti altri elementi controllati, questo metodo restituisce 1.</span><span class="sxs-lookup"><span data-stu-id="33414-114">When there are no further checked items, this method returns  1.</span></span>

## <a name="requirements"></a><span data-ttu-id="33414-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33414-115">Requirements</span></span>



| <span data-ttu-id="33414-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="33414-116">Requirement</span></span> | <span data-ttu-id="33414-117">Valore</span><span class="sxs-lookup"><span data-stu-id="33414-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="33414-118">Versione</span><span class="sxs-lookup"><span data-stu-id="33414-118">Version</span></span><br/> | <span data-ttu-id="33414-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="33414-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="33414-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33414-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33414-121">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="33414-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="33414-122">**PLAYLIST. getNextCheckedItem**</span><span class="sxs-lookup"><span data-stu-id="33414-122">**PLAYLIST.getNextCheckedItem**</span></span>](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





