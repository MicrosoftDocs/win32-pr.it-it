---
title: PLAYLIST. itemPlaylist
description: L'attributo itemPlaylist recupera la playlist per l'elemento multimediale visualizzato in corrispondenza dell'indice specificato nell'elemento PLAYLIST.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- PLAYLIST. itemPlaylist Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332530"
---
# <a name="playlistitemplaylist"></a><span data-ttu-id="75413-104">PLAYLIST. itemPlaylist</span><span class="sxs-lookup"><span data-stu-id="75413-104">PLAYLIST.itemPlaylist</span></span>

<span data-ttu-id="75413-105">L'attributo **itemPlaylist** recupera la playlist per l'elemento multimediale visualizzato in corrispondenza dell'indice specificato nell'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="75413-105">The **itemPlaylist** attribute retrieves the playlist for the media item that is displayed at the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a><span data-ttu-id="75413-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="75413-106">Possible Values</span></span>

<span data-ttu-id="75413-107">Questo attributo è un oggetto **playlist** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="75413-107">This attribute is a read-only **Playlist** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="75413-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="75413-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75413-109"><span id="index"></span><span id="INDEX"></span>*Indice*</span><span class="sxs-lookup"><span data-stu-id="75413-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="75413-110">**Numero**(**Long**) che contiene l'indice di un elemento della playlist.</span><span class="sxs-lookup"><span data-stu-id="75413-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75413-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="75413-111">Remarks</span></span>

<span data-ttu-id="75413-112">La proprietà **itemPlaylist** restituirà l'oggetto playlist espanso nell'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="75413-112">The **itemPlaylist** property will return the playlist object that is expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="75413-113">Se ad esempio sono presenti due Playlist nidificate che non sono espanse nell'elemento **playlist** e che contengono tre clip multimediali ciascuna, **itemPlaylist**(1) restituirà la playlist padre che contiene le due Playlist nidificate.</span><span class="sxs-lookup"><span data-stu-id="75413-113">For example, if there are two nested playlists that are not expanded in the **PLAYLIST** element, and that contain three media clips each, **itemPlaylist**(1) will return the parent playlist that contains the two nested playlists.</span></span> <span data-ttu-id="75413-114">Se la seconda playlist è espansa, **itemPlaylist**(1) restituirà la seconda playlist.</span><span class="sxs-lookup"><span data-stu-id="75413-114">If the second playlist is expanded, **itemPlaylist**(1) will return the second playlist.</span></span> <span data-ttu-id="75413-115">Se entrambe le playlist sono espanse, **itemPlaylist**(1) restituirà la prima playlist.</span><span class="sxs-lookup"><span data-stu-id="75413-115">If both playlists are expanded, **itemPlaylist**(1) will return the first playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="75413-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75413-116">Requirements</span></span>



| <span data-ttu-id="75413-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="75413-117">Requirement</span></span> | <span data-ttu-id="75413-118">Valore</span><span class="sxs-lookup"><span data-stu-id="75413-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="75413-119">Versione</span><span class="sxs-lookup"><span data-stu-id="75413-119">Version</span></span><br/> | <span data-ttu-id="75413-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="75413-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75413-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75413-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75413-122">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="75413-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="75413-123">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="75413-123">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





