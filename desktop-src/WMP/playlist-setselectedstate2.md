---
title: PLAYLIST. setSelectedState2
description: Il metodo setSelectedState2 imposta lo stato selezionato dell'elemento con l'indice specificato nell'elemento PLAYLIST.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- PLAYLIST. setSelectedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1a4e317543765fb24755516a0637b16958ad679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333834"
---
# <a name="playlistsetselectedstate2"></a><span data-ttu-id="ada8a-104">PLAYLIST. setSelectedState2</span><span class="sxs-lookup"><span data-stu-id="ada8a-104">PLAYLIST.setSelectedState2</span></span>

<span data-ttu-id="ada8a-105">Il metodo **setSelectedState2** imposta lo stato selezionato dell'elemento con l'indice specificato nell'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="ada8a-105">The **setSelectedState2** method sets the selected state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a><span data-ttu-id="ada8a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ada8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ada8a-107"><span id="item"></span><span id="ITEM"></span>*elemento*</span><span class="sxs-lookup"><span data-stu-id="ada8a-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="ada8a-108">**Numero** (**Long**) che indica l'indice di un elemento nella playlist.</span><span class="sxs-lookup"><span data-stu-id="ada8a-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="ada8a-109"><span id="selected"></span><span id="SELECTED"></span>*selezionato*</span><span class="sxs-lookup"><span data-stu-id="ada8a-109"><span id="selected"></span><span id="SELECTED"></span>*selected*</span></span>
</dt> <dd>

<span data-ttu-id="ada8a-110">**Valore booleano** che indica se l'elemento specificato deve essere selezionato (true) o deselezionato (false).</span><span class="sxs-lookup"><span data-stu-id="ada8a-110">**Boolean** indicating whether the specified item is to be selected (true) or unselected (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ada8a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ada8a-111">Return Value</span></span>

<span data-ttu-id="ada8a-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ada8a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ada8a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ada8a-113">Remarks</span></span>

<span data-ttu-id="ada8a-114">Questo metodo può funzionare con playlist annidate e sostituisce il metodo **setSelectedState** che non può.</span><span class="sxs-lookup"><span data-stu-id="ada8a-114">This method can work with nested playlists and replaces the **setSelectedState** method which cannot.</span></span> <span data-ttu-id="ada8a-115">È possibile impostare tutti gli elementi sullo stato richiesto specificando 1 nel parametro *Item* .</span><span class="sxs-lookup"><span data-stu-id="ada8a-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ada8a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ada8a-116">Requirements</span></span>



| <span data-ttu-id="ada8a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ada8a-117">Requirement</span></span> | <span data-ttu-id="ada8a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ada8a-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="ada8a-119">Versione</span><span class="sxs-lookup"><span data-stu-id="ada8a-119">Version</span></span><br/> | <span data-ttu-id="ada8a-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ada8a-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ada8a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ada8a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ada8a-122">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="ada8a-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="ada8a-123">**PLAYLIST. setSelectedState**</span><span class="sxs-lookup"><span data-stu-id="ada8a-123">**PLAYLIST.setSelectedState**</span></span>](playlist-setselectedstate.md)
</dt> </dl>

 

 





