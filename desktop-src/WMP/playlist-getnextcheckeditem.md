---
title: PLAYLIST. getNextCheckedItem
description: Il metodo getNextCheckedItem recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- PLAYLIST. getNextCheckedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324733"
---
# <a name="playlistgetnextcheckeditem"></a><span data-ttu-id="a1f48-104">PLAYLIST. getNextCheckedItem</span><span class="sxs-lookup"><span data-stu-id="a1f48-104">PLAYLIST.getNextCheckedItem</span></span>

<span data-ttu-id="a1f48-105">Il metodo **getNextCheckedItem** recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="a1f48-105">The **getNextCheckedItem** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="a1f48-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1f48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1f48-107"><span id="item"></span><span id="ITEM"></span>*elemento*</span><span class="sxs-lookup"><span data-stu-id="a1f48-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="a1f48-108">**Numero** (**Long**) che indica l'indice dell'elemento in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="a1f48-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1f48-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1f48-109">Return Value</span></span>

<span data-ttu-id="a1f48-110">Questo metodo restituisce un **numero** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="a1f48-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1f48-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1f48-111">Remarks</span></span>

<span data-ttu-id="a1f48-112">Quando non sono presenti altri elementi controllati, questo metodo restituisce 1.</span><span class="sxs-lookup"><span data-stu-id="a1f48-112">When there are no further checked items, this method returns  1.</span></span>

<span data-ttu-id="a1f48-113">Questo metodo è stato sostituito da **getNextCheckedItem2**, che supporta le playlist nidificate.</span><span class="sxs-lookup"><span data-stu-id="a1f48-113">This method has been replaced by **getNextCheckedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1f48-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1f48-114">Requirements</span></span>



| <span data-ttu-id="a1f48-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1f48-115">Requirement</span></span> | <span data-ttu-id="a1f48-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a1f48-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a1f48-117">Versione</span><span class="sxs-lookup"><span data-stu-id="a1f48-117">Version</span></span><br/> | <span data-ttu-id="a1f48-118">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="a1f48-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1f48-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1f48-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f48-120">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="a1f48-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="a1f48-121">**PLAYLIST. getNextCheckedItem2**</span><span class="sxs-lookup"><span data-stu-id="a1f48-121">**PLAYLIST.getNextCheckedItem2**</span></span>](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





