---
title: PlaylistCollection. nuova playlist, metodo
description: Il metodo nuova playlist crea una nuova playlist nella libreria.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- Metodo nuova playlist Windows Media Player
- Metodo nuova playlist Windows Media Player, Classe PlaylistCollection
- Classe PlaylistCollection Windows Media Player, metodo nuova playlist
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331370"
---
# <a name="playlistcollectionnewplaylist-method"></a><span data-ttu-id="0f0a8-106">PlaylistCollection. nuova playlist, metodo</span><span class="sxs-lookup"><span data-stu-id="0f0a8-106">PlaylistCollection.newPlaylist method</span></span>

<span data-ttu-id="0f0a8-107">Il metodo **nuova playlist** crea una nuova playlist nella libreria.</span><span class="sxs-lookup"><span data-stu-id="0f0a8-107">The **newPlaylist** method creates a new playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0a8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f0a8-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="0f0a8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f0a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f0a8-110">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f0a8-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f0a8-111">**Stringa** contenente il nome della playlist da creare.</span><span class="sxs-lookup"><span data-stu-id="0f0a8-111">**String** containing the name of the playlist to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f0a8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f0a8-112">Return value</span></span>

<span data-ttu-id="0f0a8-113">Questo metodo restituisce un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="0f0a8-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f0a8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f0a8-114">Remarks</span></span>

<span data-ttu-id="0f0a8-115">Questo metodo crea una playlist vuota nella libreria.</span><span class="sxs-lookup"><span data-stu-id="0f0a8-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="0f0a8-116">Per riempire la playlist con elementi multimediali, usare *playlist*. **appendItem** o *playlist*. **InsertItem**.</span><span class="sxs-lookup"><span data-stu-id="0f0a8-116">To fill the playlist with media items, use *Playlist*.**appendItem** or *Playlist*.**insertItem**.</span></span>

<span data-ttu-id="0f0a8-117">Nella libreria sono consentite più playlist con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="0f0a8-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="0f0a8-118">Per evitare di creare un nome di playlist duplicato con questo metodo, usare **GetByName** e *PlaylistArray*. **conteggio** per determinare se una playlist con un determinato nome esiste già.</span><span class="sxs-lookup"><span data-stu-id="0f0a8-118">To avoid creating a duplicate playlist name with this method, use **getByName** and *PlaylistArray*.**count** to determine whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="0f0a8-119">Gli spazi iniziali e finali non sono consentiti nei nomi delle playlist e vengono rimossi automaticamente dal valore specificato per il parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="0f0a8-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *name* parameter.</span></span>

<span data-ttu-id="0f0a8-120">Per usare questo metodo, è necessario l'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="0f0a8-120">To use this method, full access to the library is required.</span></span> <span data-ttu-id="0f0a8-121">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0f0a8-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0f0a8-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="0f0a8-122">Examples</span></span>

<span data-ttu-id="0f0a8-123">Nell'esempio JScript seguente viene creata una nuova playlist vuota denominata "Three".</span><span class="sxs-lookup"><span data-stu-id="0f0a8-123">The following JScript example creates a new empty playlist called "ThreeList".</span></span> <span data-ttu-id="0f0a8-124">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="0f0a8-124">The **Player** object was created with ID="Player".</span></span>


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a><span data-ttu-id="0f0a8-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f0a8-125">Requirements</span></span>



| <span data-ttu-id="0f0a8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f0a8-126">Requirement</span></span> | <span data-ttu-id="0f0a8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0f0a8-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f0a8-128">Versione</span><span class="sxs-lookup"><span data-stu-id="0f0a8-128">Version</span></span><br/> | <span data-ttu-id="0f0a8-129">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="0f0a8-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0f0a8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0f0a8-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="0f0a8-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f0a8-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f0a8-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f0a8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f0a8-133">**Mediacollection. Add**</span><span class="sxs-lookup"><span data-stu-id="0f0a8-133">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="0f0a8-134">**Playlist. appendItem**</span><span class="sxs-lookup"><span data-stu-id="0f0a8-134">**Playlist.appendItem**</span></span>](playlist-appenditem.md)
</dt> <dt>

[<span data-ttu-id="0f0a8-135">**Playlist. insertItem**</span><span class="sxs-lookup"><span data-stu-id="0f0a8-135">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="0f0a8-136">**PlaylistArray. Count**</span><span class="sxs-lookup"><span data-stu-id="0f0a8-136">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="0f0a8-137">**PlaylistCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="0f0a8-137">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="0f0a8-138">**PlaylistCollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="0f0a8-138">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="0f0a8-139">**PlaylistCollection. importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="0f0a8-139">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="0f0a8-140">**PlaylistCollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="0f0a8-140">**PlaylistCollection.remove**</span></span>](playlistcollection-remove.md)
</dt> <dt>

[<span data-ttu-id="0f0a8-141">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0f0a8-141">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0f0a8-142">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="0f0a8-142">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





