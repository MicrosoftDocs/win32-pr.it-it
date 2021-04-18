---
title: Mediacollection. getByAuthor, metodo
description: Il metodo getByAuthor recupera una playlist degli elementi multimediali dall'autore specificato.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- Metodo getByAuthor Windows Media Player
- Metodo getByAuthor Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getByAuthor
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eae0928250e37e76bf3a39f38b43bef8a5691c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324534"
---
# <a name="mediacollectiongetbyauthor-method"></a><span data-ttu-id="56dff-106">Mediacollection. getByAuthor, metodo</span><span class="sxs-lookup"><span data-stu-id="56dff-106">MediaCollection.getByAuthor method</span></span>

<span data-ttu-id="56dff-107">Il metodo **getByAuthor** recupera una playlist degli elementi multimediali dall'autore specificato.</span><span class="sxs-lookup"><span data-stu-id="56dff-107">The **getByAuthor** method retrieves a playlist of the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="56dff-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56dff-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a><span data-ttu-id="56dff-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="56dff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56dff-110">*autore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56dff-110">*author* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56dff-111">**Stringa** contenente il nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="56dff-111">**String** containing the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56dff-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56dff-112">Return value</span></span>

<span data-ttu-id="56dff-113">Questo metodo restituisce un oggetto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="56dff-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="56dff-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="56dff-114">Remarks</span></span>

<span data-ttu-id="56dff-115">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="56dff-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="56dff-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="56dff-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="56dff-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="56dff-117">Examples</span></span>

<span data-ttu-id="56dff-118">Nell'esempio JScript seguente viene utilizzato *mediacollection*. **getByAuthor** per recuperare una playlist di elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="56dff-118">The following JScript example uses *MediaCollection*.**getByAuthor** to retrieve a playlist of media items.</span></span> <span data-ttu-id="56dff-119">La playlist contiene elementi che corrispondono all'autore specificato dall'utente in un elemento input di testo HTML denominato GetAuthor.</span><span class="sxs-lookup"><span data-stu-id="56dff-119">The playlist contains items matching the author specified by the user in an HTML TEXT input element named GetAuthor.</span></span> <span data-ttu-id="56dff-120">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="56dff-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
               Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="56dff-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56dff-121">Requirements</span></span>



| <span data-ttu-id="56dff-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="56dff-122">Requirement</span></span> | <span data-ttu-id="56dff-123">Valore</span><span class="sxs-lookup"><span data-stu-id="56dff-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="56dff-124">Versione</span><span class="sxs-lookup"><span data-stu-id="56dff-124">Version</span></span><br/> | <span data-ttu-id="56dff-125">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="56dff-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="56dff-126">DLL</span><span class="sxs-lookup"><span data-stu-id="56dff-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="56dff-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56dff-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56dff-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56dff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56dff-129">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="56dff-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="56dff-130">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="56dff-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="56dff-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="56dff-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="56dff-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="56dff-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





