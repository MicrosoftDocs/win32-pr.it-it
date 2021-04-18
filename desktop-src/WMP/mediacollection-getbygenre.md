---
title: Mediacollection. getByGenre, metodo
description: Il metodo getByGenre recupera una playlist degli elementi multimediali con il genere specificato.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- Metodo getByGenre Windows Media Player
- Metodo getByGenre Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getByGenre
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73cd7fe9bb3efa9115e2ba5d01b6d12c89898d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327168"
---
# <a name="mediacollectiongetbygenre-method"></a><span data-ttu-id="3c489-106">Mediacollection. getByGenre, metodo</span><span class="sxs-lookup"><span data-stu-id="3c489-106">MediaCollection.getByGenre method</span></span>

<span data-ttu-id="3c489-107">Il metodo **getByGenre** recupera una playlist degli elementi multimediali con il genere specificato.</span><span class="sxs-lookup"><span data-stu-id="3c489-107">The **getByGenre** method retrieves a playlist of the media items with the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c489-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c489-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a><span data-ttu-id="3c489-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c489-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c489-110">*genere* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c489-110">*genre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c489-111">**Stringa** che contiene il nome del genere.</span><span class="sxs-lookup"><span data-stu-id="3c489-111">**String** containing the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c489-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c489-112">Return value</span></span>

<span data-ttu-id="3c489-113">Questo metodo restituisce un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="3c489-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c489-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c489-114">Remarks</span></span>

<span data-ttu-id="3c489-115">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="3c489-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3c489-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3c489-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3c489-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="3c489-117">Examples</span></span>

<span data-ttu-id="3c489-118">Nell'esempio JScript seguente viene utilizzato *mediacollection*. **getByGenre** per recuperare una playlist di elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="3c489-118">The following JScript example uses *MediaCollection*.**getByGenre** to retrieve a playlist of media items.</span></span> <span data-ttu-id="3c489-119">La playlist contiene elementi con il genere specificato dall'utente in un elemento input di testo HTML denominato getgenre.</span><span class="sxs-lookup"><span data-stu-id="3c489-119">The playlist contains items with the genre specified by the user in an HTML TEXT input element named GetGenre.</span></span> <span data-ttu-id="3c489-120">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="3c489-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="3c489-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c489-121">Requirements</span></span>



| <span data-ttu-id="3c489-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c489-122">Requirement</span></span> | <span data-ttu-id="3c489-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3c489-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c489-124">Versione</span><span class="sxs-lookup"><span data-stu-id="3c489-124">Version</span></span><br/> | <span data-ttu-id="3c489-125">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="3c489-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3c489-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3c489-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="3c489-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c489-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c489-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c489-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c489-129">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="3c489-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="3c489-130">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="3c489-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="3c489-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3c489-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3c489-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3c489-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





