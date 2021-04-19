---
title: Playlist. Item (metodo)
description: Il metodo Item recupera l'elemento multimediale in corrispondenza dell'indice specificato.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo Item
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c69386871aeec33dbc36a066ce3f75e80d7514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332541"
---
# <a name="playlistitem-method"></a><span data-ttu-id="3f303-106">Playlist. Item (metodo)</span><span class="sxs-lookup"><span data-stu-id="3f303-106">Playlist.item method</span></span>

<span data-ttu-id="3f303-107">Il metodo **Item** recupera l'elemento multimediale in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="3f303-107">The **item** method retrieves the media item at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f303-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f303-108">Syntax</span></span>


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="3f303-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f303-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f303-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3f303-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f303-111">**Numero** (**Long**) che contiene l'indice dell'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="3f303-111">**Number** (**long**) containing the index of the item to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f303-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f303-112">Return value</span></span>

<span data-ttu-id="3f303-113">Questo metodo restituisce un oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="3f303-113">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f303-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f303-114">Remarks</span></span>

<span data-ttu-id="3f303-115">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="3f303-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3f303-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3f303-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3f303-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="3f303-117">Examples</span></span>

<span data-ttu-id="3f303-118">Nell'esempio JScript seguente viene utilizzata la *playlist*. **elemento** per recuperare un elemento multimediale dalla playlist corrente in base a una selezione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3f303-118">The following JScript example uses *Playlist*.**item** to retrieve a media item from the current playlist based on a user selection.</span></span> <span data-ttu-id="3f303-119">È stato creato un elemento HTML SELECT denominato "Weblist", che è stato compilato con i titoli della playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="3f303-119">An HTML SELECT element was created with name "weblist", and filled with the titles from the current playlist.</span></span> <span data-ttu-id="3f303-120">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="3f303-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

```



## <a name="requirements"></a><span data-ttu-id="3f303-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f303-121">Requirements</span></span>



| <span data-ttu-id="3f303-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f303-122">Requirement</span></span> | <span data-ttu-id="3f303-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3f303-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3f303-124">Versione</span><span class="sxs-lookup"><span data-stu-id="3f303-124">Version</span></span><br/> | <span data-ttu-id="3f303-125">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="3f303-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3f303-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3f303-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="3f303-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f303-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f303-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f303-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f303-129">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="3f303-129">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="3f303-130">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="3f303-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="3f303-131">**Playlist. insertItem**</span><span class="sxs-lookup"><span data-stu-id="3f303-131">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="3f303-132">**Playlist. removeItem**</span><span class="sxs-lookup"><span data-stu-id="3f303-132">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="3f303-133">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3f303-133">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3f303-134">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3f303-134">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





