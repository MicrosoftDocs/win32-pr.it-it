---
title: PLAYLIST. getNextSelectedItem
description: Il metodo getNextSelectedItem recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- PLAYLIST. getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324730"
---
# <a name="playlistgetnextselecteditem"></a><span data-ttu-id="e399d-104">PLAYLIST. getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="e399d-104">PLAYLIST.getNextSelectedItem</span></span>

<span data-ttu-id="e399d-105">Il metodo **getNextSelectedItem** recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="e399d-105">The **getNextSelectedItem** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="e399d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e399d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e399d-107"><span id="item"></span><span id="ITEM"></span>*elemento*</span><span class="sxs-lookup"><span data-stu-id="e399d-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="e399d-108">**Numero** (**Long**) che indica l'indice dell'elemento in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="e399d-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e399d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e399d-109">Return Value</span></span>

<span data-ttu-id="e399d-110">Questo metodo restituisce un **numero** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="e399d-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="e399d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e399d-111">Remarks</span></span>

<span data-ttu-id="e399d-112">Quando non sono presenti altri elementi selezionati, questo metodo restituisce 1.</span><span class="sxs-lookup"><span data-stu-id="e399d-112">When there are no further selected items, this method returns  1.</span></span>

<span data-ttu-id="e399d-113">Questo metodo è stato sostituito da **getNextSelectedItem2**, che supporta le playlist nidificate.</span><span class="sxs-lookup"><span data-stu-id="e399d-113">This method has been replaced by **getNextSelectedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="e399d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e399d-114">Requirements</span></span>



| <span data-ttu-id="e399d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e399d-115">Requirement</span></span> | <span data-ttu-id="e399d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e399d-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e399d-117">Versione</span><span class="sxs-lookup"><span data-stu-id="e399d-117">Version</span></span><br/> | <span data-ttu-id="e399d-118">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="e399d-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e399d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e399d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e399d-120">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="e399d-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="e399d-121">**PLAYLIST. getNextSelectedItem2**</span><span class="sxs-lookup"><span data-stu-id="e399d-121">**PLAYLIST.getNextSelectedItem2**</span></span>](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





