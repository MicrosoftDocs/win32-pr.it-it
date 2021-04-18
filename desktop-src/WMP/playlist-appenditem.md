---
title: Playlist. appendItem, metodo
description: Il metodo appendItem aggiunge un elemento multimediale alla fine della playlist.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- Metodo appendItem Windows Media Player
- Metodo appendItem Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo appendItem
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 828799d5b6e71e7ff0e7be4c1e55714f6343be51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327145"
---
# <a name="playlistappenditem-method"></a><span data-ttu-id="3d80d-106">Playlist. appendItem, metodo</span><span class="sxs-lookup"><span data-stu-id="3d80d-106">Playlist.appendItem method</span></span>

<span data-ttu-id="3d80d-107">Il metodo **appendItem** aggiunge un elemento multimediale alla fine della playlist.</span><span class="sxs-lookup"><span data-stu-id="3d80d-107">The **appendItem** method adds a media item to the end of the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d80d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d80d-108">Syntax</span></span>


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="3d80d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d80d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d80d-110">*elemento* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3d80d-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d80d-111">Oggetto **multimediale** da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="3d80d-111">**Media** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d80d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d80d-112">Return value</span></span>

<span data-ttu-id="3d80d-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3d80d-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d80d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d80d-114">Remarks</span></span>

<span data-ttu-id="3d80d-115">Per usare questo metodo, è necessario l'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="3d80d-115">To use this method, full access to the library is required.</span></span> <span data-ttu-id="3d80d-116">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3d80d-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3d80d-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="3d80d-117">Examples</span></span>

<span data-ttu-id="3d80d-118">Nell'esempio JScript seguente viene utilizzata la *playlist*. **appendItem** aggiungere l'elemento multimediale corrente alla playlist denominata "Three".</span><span class="sxs-lookup"><span data-stu-id="3d80d-118">The following JScript example uses *Playlist*.**appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="3d80d-119">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="3d80d-119">The **Player** object was created with ID="Player".</span></span>


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a><span data-ttu-id="3d80d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d80d-120">Requirements</span></span>



| <span data-ttu-id="3d80d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d80d-121">Requirement</span></span> | <span data-ttu-id="3d80d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3d80d-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d80d-123">Versione</span><span class="sxs-lookup"><span data-stu-id="3d80d-123">Version</span></span><br/> | <span data-ttu-id="3d80d-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="3d80d-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3d80d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3d80d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3d80d-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d80d-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d80d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d80d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d80d-128">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="3d80d-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="3d80d-129">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3d80d-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3d80d-130">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3d80d-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





