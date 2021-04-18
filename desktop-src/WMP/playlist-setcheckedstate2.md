---
title: PLAYLIST. setCheckedState2
description: Il metodo setCheckedState2 imposta lo stato di selezione dell'elemento con l'indice specificato nell'elemento PLAYLIST.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- PLAYLIST. setCheckedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324528"
---
# <a name="playlistsetcheckedstate2"></a><span data-ttu-id="e62af-104">PLAYLIST. setCheckedState2</span><span class="sxs-lookup"><span data-stu-id="e62af-104">PLAYLIST.setCheckedState2</span></span>

<span data-ttu-id="e62af-105">Il metodo **setCheckedState2** imposta lo stato di selezione dell'elemento con l'indice specificato nell'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="e62af-105">The **setCheckedState2** method sets the checked state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a><span data-ttu-id="e62af-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e62af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e62af-107"><span id="item"></span><span id="ITEM"></span>*elemento*</span><span class="sxs-lookup"><span data-stu-id="e62af-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="e62af-108">**Numero** (**Long**) che indica l'indice dell'elemento della playlist da controllare o deselezionare.</span><span class="sxs-lookup"><span data-stu-id="e62af-108">**Number** (**long**) indicating the index of the playlist item to be checked or unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="e62af-109"><span id="checked"></span><span id="CHECKED"></span>*selezionata*</span><span class="sxs-lookup"><span data-stu-id="e62af-109"><span id="checked"></span><span id="CHECKED"></span>*checked*</span></span>
</dt> <dd>

<span data-ttu-id="e62af-110">**Valore booleano** che indica se l'elemento specificato deve essere selezionato (true) o deselezionato (false).</span><span class="sxs-lookup"><span data-stu-id="e62af-110">**Boolean** indicating whether the specified item is to be checked (true) or unchecked (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e62af-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e62af-111">Return Value</span></span>

<span data-ttu-id="e62af-112">Questo metodo restituisce un **valore booleano**.</span><span class="sxs-lookup"><span data-stu-id="e62af-112">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e62af-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e62af-113">Remarks</span></span>

<span data-ttu-id="e62af-114">Questo metodo può funzionare con playlist annidate e sostituisce il metodo **setCheckedState** , che non può.</span><span class="sxs-lookup"><span data-stu-id="e62af-114">This method can work with nested playlists and replaces the **setCheckedState** method, which cannot.</span></span> <span data-ttu-id="e62af-115">È possibile impostare tutti gli elementi sullo stato richiesto specificando 1 nel parametro *Item* .</span><span class="sxs-lookup"><span data-stu-id="e62af-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e62af-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e62af-116">Requirements</span></span>



| <span data-ttu-id="e62af-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e62af-117">Requirement</span></span> | <span data-ttu-id="e62af-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e62af-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e62af-119">Versione</span><span class="sxs-lookup"><span data-stu-id="e62af-119">Version</span></span><br/> | <span data-ttu-id="e62af-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e62af-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e62af-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e62af-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e62af-122">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="e62af-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="e62af-123">**PLAYLIST. setCheckedState**</span><span class="sxs-lookup"><span data-stu-id="e62af-123">**PLAYLIST.setCheckedState**</span></span>](playlist-setcheckedstate.md)
</dt> </dl>

 

 





