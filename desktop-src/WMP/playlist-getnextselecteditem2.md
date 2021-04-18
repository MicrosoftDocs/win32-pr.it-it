---
title: PLAYLIST. getNextSelectedItem2
description: Il metodo getNextSelectedItem2 recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- PLAYLIST. getNextSelectedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324726"
---
# <a name="playlistgetnextselecteditem2"></a><span data-ttu-id="35957-104">PLAYLIST. getNextSelectedItem2</span><span class="sxs-lookup"><span data-stu-id="35957-104">PLAYLIST.getNextSelectedItem2</span></span>

<span data-ttu-id="35957-105">Il metodo **getNextSelectedItem2** recupera l'indice del successivo elemento selezionato nella playlist che segue l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="35957-105">The **getNextSelectedItem2** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="35957-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35957-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35957-107"><span id="item"></span><span id="ITEM"></span>*elemento*</span><span class="sxs-lookup"><span data-stu-id="35957-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="35957-108">**Numero** (**Long**) che indica l'indice dell'elemento in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="35957-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35957-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35957-109">Return Value</span></span>

<span data-ttu-id="35957-110">Questo metodo restituisce un **numero** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="35957-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="35957-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="35957-111">Remarks</span></span>

<span data-ttu-id="35957-112">Questo metodo può funzionare con playlist annidate e sostituisce il metodo **getNextSelectedItem** , che non può.</span><span class="sxs-lookup"><span data-stu-id="35957-112">This method can work with nested playlists and replaces the **getNextSelectedItem** method, which cannot.</span></span> <span data-ttu-id="35957-113">Passare 1 nel parametro *Item* per trovare il primo elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="35957-113">Pass  1 in the *item* parameter to find the first selected item.</span></span> <span data-ttu-id="35957-114">Quando non sono presenti altri elementi selezionati, viene restituito-1.</span><span class="sxs-lookup"><span data-stu-id="35957-114">When there are no further selected items, -1 is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="35957-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35957-115">Requirements</span></span>



| <span data-ttu-id="35957-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="35957-116">Requirement</span></span> | <span data-ttu-id="35957-117">Valore</span><span class="sxs-lookup"><span data-stu-id="35957-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="35957-118">Versione</span><span class="sxs-lookup"><span data-stu-id="35957-118">Version</span></span><br/> | <span data-ttu-id="35957-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="35957-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35957-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35957-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35957-121">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="35957-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="35957-122">**PLAYLIST. getNextSelectedItem**</span><span class="sxs-lookup"><span data-stu-id="35957-122">**PLAYLIST.getNextSelectedItem**</span></span>](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





