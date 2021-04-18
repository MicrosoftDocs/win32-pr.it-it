---
title: Player. nuova playlist, metodo
description: Il metodo nuova playlist crea un nuovo oggetto playlist.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- Metodo nuova playlist Windows Media Player
- Metodo nuova playlist Windows Media Player, classe Player
- Classe Player Windows Media Player, metodo nuova playlist
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa65ae4b453fe919116a33c5ee86b14ba353f681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324977"
---
# <a name="playernewplaylist-method"></a><span data-ttu-id="7cbe6-106">Player. nuova playlist, metodo</span><span class="sxs-lookup"><span data-stu-id="7cbe6-106">Player.newPlaylist method</span></span>

<span data-ttu-id="7cbe6-107">Il metodo **nuova playlist** crea un nuovo oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="7cbe6-107">The **newPlaylist** method creates a new **Playlist** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbe6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cbe6-108">Syntax</span></span>


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="7cbe6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7cbe6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cbe6-110">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cbe6-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-111">**Stringa** contenente il nome della nuova playlist.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-111">**String** containing the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="7cbe6-112">*URL* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="7cbe6-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cbe6-113">**Stringa** contenente l'URL della playlist Windows Media Metafile con la quale creare l'oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="7cbe6-113">**String** containing the URL of the Windows Media metafile playlist to create the **Playlist** object with.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cbe6-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7cbe6-114">Return value</span></span>

<span data-ttu-id="7cbe6-115">Questo metodo restituisce un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="7cbe6-115">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cbe6-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7cbe6-116">Remarks</span></span>

<span data-ttu-id="7cbe6-117">Se il parametro *URL* è impostato su null o su "" (stringa vuota), verrà creato un oggetto **playlist** vuoto.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-117">If the *URL* parameter is set to null or "" (empty string), an empty **Playlist** object will be created.</span></span> <span data-ttu-id="7cbe6-118">Se il parametro *Name* è impostato su "", viene usato il nome del metafile.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-118">If the *name* parameter is set to "", the name in the metafile is used.</span></span>

<span data-ttu-id="7cbe6-119">La nuova playlist creata con questo metodo non viene aggiunta alla libreria.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="7cbe6-120">Per aggiungere una nuova playlist alla libreria, usare *PlaylistCollection*. **importPlaylist** o *PlaylistCollection*. **nuova playlist**.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-120">To add a new playlist to the library, use *PlaylistCollection*.**importPlaylist** or *PlaylistCollection*.**newPlaylist**.</span></span> <span data-ttu-id="7cbe6-121">Eventuali spazi iniziali o finali nel nome della playlist vengono rimossi automaticamente quando vengono aggiunti alla libreria.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="7cbe6-122">Poiché la libreria consente più playlist con lo stesso nome, è consigliabile verificare la presenza di una playlist con un nome specificato prima di aggiungerne una nuova.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cbe6-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cbe6-123">Requirements</span></span>



| <span data-ttu-id="7cbe6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cbe6-124">Requirement</span></span> | <span data-ttu-id="7cbe6-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7cbe6-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7cbe6-126">Versione</span><span class="sxs-lookup"><span data-stu-id="7cbe6-126">Version</span></span><br/> | <span data-ttu-id="7cbe6-127">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="7cbe6-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="7cbe6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7cbe6-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="7cbe6-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cbe6-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cbe6-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7cbe6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cbe6-131">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-131">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="7cbe6-132">**PlaylistCollection. importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-132">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="7cbe6-133">**PlaylistCollection. nuova playlist**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-133">**PlaylistCollection.newPlaylist**</span></span>](playlistcollection-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="7cbe6-134">**Metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7cbe6-134">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 





