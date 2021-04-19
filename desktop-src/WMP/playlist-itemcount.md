---
title: PLAYLIST. itemCount
description: L'attributo itemCount Recupera il numero di elementi attualmente visualizzati nell'elemento PLAYLIST.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- PLAYLIST. itemCount Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332539"
---
# <a name="playlistitemcount"></a><span data-ttu-id="afd26-104">PLAYLIST. itemCount</span><span class="sxs-lookup"><span data-stu-id="afd26-104">PLAYLIST.itemCount</span></span>

<span data-ttu-id="afd26-105">L'attributo **ItemCount** Recupera il numero di elementi attualmente visualizzati nell'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="afd26-105">The **itemCount** attribute retrieves the number of items currently displayed in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a><span data-ttu-id="afd26-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="afd26-106">Possible Values</span></span>

<span data-ttu-id="afd26-107">Questo attributo è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="afd26-107">This attribute is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="afd26-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="afd26-108">Remarks</span></span>

<span data-ttu-id="afd26-109">Il numero totale di elementi espansi viene conteggiato dalla proprietà **ItemCount** .</span><span class="sxs-lookup"><span data-stu-id="afd26-109">The **itemCount** property will count the total number of expanded items.</span></span> <span data-ttu-id="afd26-110">Se, ad esempio, sono presenti due playlist che contengono tre elementi multimediali, **ItemCount** restituirà 2 se le playlist non vengono espanse.</span><span class="sxs-lookup"><span data-stu-id="afd26-110">For example, if there are two playlists that contain three media items each, **itemCount** will return 2 if the playlists are not expanded.</span></span> <span data-ttu-id="afd26-111">Se viene espansa solo la prima playlist, **ItemCount** restituirà 4.</span><span class="sxs-lookup"><span data-stu-id="afd26-111">If only the first playlist is expanded, **itemCount** will return 4.</span></span> <span data-ttu-id="afd26-112">Se entrambe le playlist sono espanse, **ItemCount** restituirà 6.</span><span class="sxs-lookup"><span data-stu-id="afd26-112">If both playlists are expanded, **itemCount** will return 6.</span></span>

## <a name="requirements"></a><span data-ttu-id="afd26-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afd26-113">Requirements</span></span>



| <span data-ttu-id="afd26-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="afd26-114">Requirement</span></span> | <span data-ttu-id="afd26-115">Valore</span><span class="sxs-lookup"><span data-stu-id="afd26-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="afd26-116">Versione</span><span class="sxs-lookup"><span data-stu-id="afd26-116">Version</span></span><br/> | <span data-ttu-id="afd26-117">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="afd26-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="afd26-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afd26-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afd26-119">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="afd26-119">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





