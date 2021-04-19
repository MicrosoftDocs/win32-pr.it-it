---
title: Mediacollection. getByAlbum, metodo
description: Il metodo GetByAlbum recupera una playlist contenente gli elementi multimediali dall'album specificato.
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- Metodo getByAlbum Windows Media Player
- Metodo getByAlbum Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getByAlbum
topic_type:
- apiref
api_name:
- MediaCollection.getByAlbum
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d94cdfa880288893e9659b73b01bc754ac59bbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330348"
---
# <a name="mediacollectiongetbyalbum-method"></a><span data-ttu-id="a2393-106">Mediacollection. getByAlbum, metodo</span><span class="sxs-lookup"><span data-stu-id="a2393-106">MediaCollection.getByAlbum method</span></span>

<span data-ttu-id="a2393-107">Il metodo **GetByAlbum** recupera una playlist contenente gli elementi multimediali dall'album specificato.</span><span class="sxs-lookup"><span data-stu-id="a2393-107">The **GetByAlbum** method retrieves a playlist containing the media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2393-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2393-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a><span data-ttu-id="a2393-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2393-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2393-110">*album* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2393-110">*album* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2393-111">**Stringa** contenente il nome dell'album.</span><span class="sxs-lookup"><span data-stu-id="a2393-111">**String** containing the name of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2393-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2393-112">Return value</span></span>

<span data-ttu-id="a2393-113">Questo metodo restituisce un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="a2393-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2393-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2393-114">Remarks</span></span>

<span data-ttu-id="a2393-115">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="a2393-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="a2393-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a2393-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a2393-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="a2393-117">Examples</span></span>

<span data-ttu-id="a2393-118">Nell'esempio seguente viene utilizzato *mediacollection*. **getByAlbum** per recuperare una playlist di elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="a2393-118">The following example uses *MediaCollection*.**getByAlbum** to retrieve a playlist of media items.</span></span> <span data-ttu-id="a2393-119">La playlist contiene elementi con l'album specificato dall'utente in un elemento input di testo HTML denominato GetAlbum.</span><span class="sxs-lookup"><span data-stu-id="a2393-119">The playlist contains items with the album specified by the user in an HTML TEXT input element named GetAlbum.</span></span> <span data-ttu-id="a2393-120">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a2393-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and 
then play the digital media items. -->
<INPUT TYPE = "BUTTON"
       NAME = "PlayAlbum" 
       ID = "PlayAlbum"  
       VALUE = "Play Album"

onClick = "
    /* Retrieve the album title text from the user. */
    var album = GetAlbum.value;

    /* Create the playlist using getByAlbum. */
    var pl = Player.mediaCollection.getByAlbum(album);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="a2393-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2393-121">Requirements</span></span>



| <span data-ttu-id="a2393-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2393-122">Requirement</span></span> | <span data-ttu-id="a2393-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a2393-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2393-124">Versione</span><span class="sxs-lookup"><span data-stu-id="a2393-124">Version</span></span><br/> | <span data-ttu-id="a2393-125">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="a2393-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a2393-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a2393-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="a2393-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2393-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2393-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2393-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2393-129">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="a2393-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="a2393-130">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="a2393-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="a2393-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a2393-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a2393-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a2393-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





