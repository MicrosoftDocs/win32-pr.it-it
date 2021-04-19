---
title: PlaylistCollection. importPlaylist, metodo
description: Il metodo importPlaylist aggiunge una playlist statica alla libreria. | PlaylistCollection. importPlaylist, metodo
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- Metodo importPlaylist Windows Media Player
- Metodo importPlaylist Windows Media Player, Classe PlaylistCollection
- Classe PlaylistCollection Windows Media Player, metodo importPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329433"
---
# <a name="playlistcollectionimportplaylist-method"></a><span data-ttu-id="b2425-107">PlaylistCollection. importPlaylist, metodo</span><span class="sxs-lookup"><span data-stu-id="b2425-107">PlaylistCollection.importPlaylist method</span></span>

<span data-ttu-id="b2425-108">Il metodo **importPlaylist** aggiunge una playlist statica alla libreria.</span><span class="sxs-lookup"><span data-stu-id="b2425-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2425-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2425-109">Syntax</span></span>


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="b2425-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2425-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2425-111">*playlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2425-111">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2425-112">Oggetto **playlist** da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="b2425-112">**Playlist** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2425-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2425-113">Return value</span></span>

<span data-ttu-id="b2425-114">Questo metodo restituisce l'oggetto **playlist** che è stato aggiunto.</span><span class="sxs-lookup"><span data-stu-id="b2425-114">This method returns the **Playlist** object that was added.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2425-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2425-115">Remarks</span></span>

<span data-ttu-id="b2425-116">Le playlist che non contengono elementi multimediali non possono essere aggiunte alla libreria utilizzando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="b2425-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="b2425-117">Per creare una playlist vuota nella libreria, usare il metodo **nuova playlist** .</span><span class="sxs-lookup"><span data-stu-id="b2425-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="b2425-118">È quindi possibile compilare la playlist risultante con elementi multimediali usando *playlist*. **appendItem** o *playlist*. **InsertItem**.</span><span class="sxs-lookup"><span data-stu-id="b2425-118">You can then fill the resulting playlist with media items by using *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="b2425-119">Se si passa questo metodo una playlist automatica, la query viene eseguita una volta e il risultato viene aggiunto alla libreria come playlist statica.</span><span class="sxs-lookup"><span data-stu-id="b2425-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="b2425-120">Per aggiungere una playlist automatica alla libreria e mantenerne il comportamento automatico, usare *mediacollection*. **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="b2425-120">To add an auto playlist to the library and preserve its automatic behavior, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="b2425-121">Per altre informazioni, vedere [playlist statiche e automatiche](static-and-auto-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="b2425-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="b2425-122">Per usare questo metodo, è necessario l'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="b2425-122">To use this method, full access to the library is required.</span></span> <span data-ttu-id="b2425-123">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b2425-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2425-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2425-124">Requirements</span></span>



| <span data-ttu-id="b2425-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2425-125">Requirement</span></span> | <span data-ttu-id="b2425-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b2425-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2425-127">Versione</span><span class="sxs-lookup"><span data-stu-id="b2425-127">Version</span></span><br/> | <span data-ttu-id="b2425-128">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="b2425-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b2425-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b2425-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="b2425-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2425-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2425-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2425-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2425-132">**Gestione delle playlist**</span><span class="sxs-lookup"><span data-stu-id="b2425-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="b2425-133">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="b2425-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="b2425-134">**Mediacollection. Add**</span><span class="sxs-lookup"><span data-stu-id="b2425-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="b2425-135">**Playlist. appendItem**</span><span class="sxs-lookup"><span data-stu-id="b2425-135">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="b2425-136">**Playlist. insertItem**</span><span class="sxs-lookup"><span data-stu-id="b2425-136">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="b2425-137">**PlaylistCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="b2425-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="b2425-138">**PlaylistCollection. nuova playlist**</span><span class="sxs-lookup"><span data-stu-id="b2425-138">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="b2425-139">**PlaylistCollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="b2425-139">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="b2425-140">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b2425-140">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b2425-141">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b2425-141">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





