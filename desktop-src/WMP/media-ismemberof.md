---
title: Media. isMemberOf, metodo
description: Il metodo isMemberOf restituisce un valore che indica se l'elemento multimediale è un membro della playlist specificata.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- Metodo isMemberOf Windows Media Player
- Metodo isMemberOf Windows Media Player, classe media
- Media class Media Player Windows, metodo isMemberOf
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325835"
---
# <a name="mediaismemberof-method"></a><span data-ttu-id="fd9ae-106">Media. isMemberOf, metodo</span><span class="sxs-lookup"><span data-stu-id="fd9ae-106">Media.isMemberOf method</span></span>

<span data-ttu-id="fd9ae-107">Il metodo **isMemberOf** restituisce un valore che indica se l'elemento multimediale è un membro della playlist specificata.</span><span class="sxs-lookup"><span data-stu-id="fd9ae-107">The **isMemberOf** method returns a value indicating whether the media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9ae-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd9ae-108">Syntax</span></span>


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="fd9ae-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd9ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd9ae-110">*playlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd9ae-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd9ae-111">Oggetto **playlist** che potrebbe contenere l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="fd9ae-111">**Playlist** object that might contain the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd9ae-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd9ae-112">Return value</span></span>

<span data-ttu-id="fd9ae-113">Questo metodo restituisce un **valore booleano**.</span><span class="sxs-lookup"><span data-stu-id="fd9ae-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd9ae-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd9ae-114">Remarks</span></span>

<span data-ttu-id="fd9ae-115">Questo metodo non consente di controllare le playlist recuperate tramite l'oggetto **mediacollection** .</span><span class="sxs-lookup"><span data-stu-id="fd9ae-115">This method is cannot check playlists retrieved through the **MediaCollection** object.</span></span> <span data-ttu-id="fd9ae-116">Per verificare se un elemento multimediale è un membro di una determinata playlist denominata, recuperare la playlist con *Player*. *PlaylistCollection*. **GetByName**(*Name*). **elemento**(0).</span><span class="sxs-lookup"><span data-stu-id="fd9ae-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist with *player*.*playlistCollection*.**getByName**(*name*).**item**(0).</span></span> <span data-ttu-id="fd9ae-117">Questo metodo può essere usato anche con playlist CD e playlist di metafile.</span><span class="sxs-lookup"><span data-stu-id="fd9ae-117">This method can also be used with CD playlists and metafile playlists.</span></span>

<span data-ttu-id="fd9ae-118">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="fd9ae-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="fd9ae-119">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fd9ae-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fd9ae-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="fd9ae-120">Examples</span></span>

<span data-ttu-id="fd9ae-121">Nell'esempio JScript seguente viene usato il *supporto*. **isMemberOf** per verificare se l'elemento multimediale corrente è un membro della playlist denominata playlist di esempio.</span><span class="sxs-lookup"><span data-stu-id="fd9ae-121">The following JScript example uses *Media*.**isMemberOf** to test whether the current media item is a member of the playlist named Sample Playlist.</span></span> <span data-ttu-id="fd9ae-122">In caso contrario, l'elemento multimediale corrente viene aggiunto alla playlist di esempio.</span><span class="sxs-lookup"><span data-stu-id="fd9ae-122">If it is not, the current media item is appended to the sample playlist.</span></span> <span data-ttu-id="fd9ae-123">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="fd9ae-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

```



## <a name="requirements"></a><span data-ttu-id="fd9ae-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd9ae-124">Requirements</span></span>



| <span data-ttu-id="fd9ae-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd9ae-125">Requirement</span></span> | <span data-ttu-id="fd9ae-126">Valore</span><span class="sxs-lookup"><span data-stu-id="fd9ae-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9ae-127">Versione</span><span class="sxs-lookup"><span data-stu-id="fd9ae-127">Version</span></span><br/> | <span data-ttu-id="fd9ae-128">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="fd9ae-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fd9ae-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fd9ae-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd9ae-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd9ae-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd9ae-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd9ae-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd9ae-132">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="fd9ae-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="fd9ae-133">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="fd9ae-133">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="fd9ae-134">**PlaylistCollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="fd9ae-134">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="fd9ae-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fd9ae-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="fd9ae-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fd9ae-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





