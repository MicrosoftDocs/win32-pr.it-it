---
title: Playlist. removeItem, metodo
description: Il metodo removeItem rimuove l'elemento specificato dalla playlist.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- Metodo removeItem Windows Media Player
- Metodo removeItem Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo removeItem
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de03333e2373744f9e9197be8ed8582997c557d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327609"
---
# <a name="playlistremoveitem-method"></a><span data-ttu-id="b3ee4-106">Playlist. removeItem, metodo</span><span class="sxs-lookup"><span data-stu-id="b3ee4-106">Playlist.removeItem method</span></span>

<span data-ttu-id="b3ee4-107">Il metodo **RemoveItem** rimuove l'elemento specificato dalla playlist.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-107">The **removeItem** method removes the specified item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ee4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3ee4-108">Syntax</span></span>


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="b3ee4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3ee4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3ee4-110">*elemento* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b3ee4-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ee4-111">Oggetto **multimediale** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-111">**Media** object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3ee4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3ee4-112">Return value</span></span>

<span data-ttu-id="b3ee4-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3ee4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3ee4-114">Remarks</span></span>

<span data-ttu-id="b3ee4-115">Se l'elemento rimosso è la traccia attualmente in gioco (*Player*.**currentMedia**), la riproduzione viene arrestata e l'elemento successivo nella playlist diventa quello corrente.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-115">If the item removed is the currently playing track (*Player*.**currentMedia**), playback stops and the next item in the playlist becomes the current one.</span></span> <span data-ttu-id="b3ee4-116">Se non è presente alcun elemento successivo, viene usato l'elemento precedente o se non sono presenti altri elementi, quindi *Player*. **currentMedia** è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-116">If there is no next item, the previous item is used, or if there are no other items, then *Player*.**currentMedia** is set to **NULL**.</span></span>

<span data-ttu-id="b3ee4-117">Per usare questo metodo, è necessario l'accesso completo alla libreria.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-117">To use this method, full access to the library is required.</span></span> <span data-ttu-id="b3ee4-118">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b3ee4-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3ee4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3ee4-119">Requirements</span></span>



| <span data-ttu-id="b3ee4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3ee4-120">Requirement</span></span> | <span data-ttu-id="b3ee4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b3ee4-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ee4-122">Versione</span><span class="sxs-lookup"><span data-stu-id="b3ee4-122">Version</span></span><br/> | <span data-ttu-id="b3ee4-123">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b3ee4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b3ee4-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="b3ee4-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3ee4-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3ee4-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3ee4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ee4-127">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="b3ee4-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="b3ee4-128">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="b3ee4-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="b3ee4-129">**Playlist. insertItem**</span><span class="sxs-lookup"><span data-stu-id="b3ee4-129">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="b3ee4-130">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="b3ee4-130">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="b3ee4-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b3ee4-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b3ee4-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b3ee4-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





