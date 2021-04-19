---
title: Evento Player. PlaylistCollectionPlaylistRemoved
description: L'evento PlaylistCollectionPlaylistRemoved si verifica quando una playlist viene rimossa dalla raccolta di playlist. | Evento Player. PlaylistCollectionPlaylistRemoved
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Media Player di Windows Event PlaylistCollectionPlaylistRemoved
- Windows Event PlaylistCollectionPlaylistRemoved Media Player, classe Player
- Classe Player Windows Media Player, evento PlaylistCollectionPlaylistRemoved
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a449a7b00516f4fee613722d1cc126eb74227948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332672"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a><span data-ttu-id="676bb-107">Evento Player. PlaylistCollectionPlaylistRemoved</span><span class="sxs-lookup"><span data-stu-id="676bb-107">Player.PlaylistCollectionPlaylistRemoved event</span></span>

<span data-ttu-id="676bb-108">L'evento **PlaylistCollectionPlaylistRemoved** si verifica quando una playlist viene rimossa dalla raccolta di playlist.</span><span class="sxs-lookup"><span data-stu-id="676bb-108">The **PlaylistCollectionPlaylistRemoved** event occurs when a playlist is removed from the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="676bb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="676bb-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="676bb-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="676bb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="676bb-111">*bstrPlaylistName*</span><span class="sxs-lookup"><span data-stu-id="676bb-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="676bb-112">**Stringa** che specifica il nome della playlist che è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="676bb-112">**String** specifying the name of the playlist that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="676bb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="676bb-113">Return value</span></span>

<span data-ttu-id="676bb-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="676bb-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="676bb-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="676bb-115">Remarks</span></span>

<span data-ttu-id="676bb-116">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="676bb-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="676bb-117">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="676bb-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="676bb-118">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="676bb-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="676bb-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="676bb-119">Requirements</span></span>



| <span data-ttu-id="676bb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="676bb-120">Requirement</span></span> | <span data-ttu-id="676bb-121">Valore</span><span class="sxs-lookup"><span data-stu-id="676bb-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="676bb-122">Versione</span><span class="sxs-lookup"><span data-stu-id="676bb-122">Version</span></span><br/> | <span data-ttu-id="676bb-123">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="676bb-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="676bb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="676bb-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="676bb-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="676bb-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="676bb-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="676bb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="676bb-127">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="676bb-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="676bb-128">**PlaylistCollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="676bb-128">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





