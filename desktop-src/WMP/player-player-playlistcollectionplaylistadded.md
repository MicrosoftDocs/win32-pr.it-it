---
title: Evento Player. PlaylistCollectionPlaylistAdded
description: L'evento PlaylistCollectionPlaylistAdded si verifica quando viene aggiunta una playlist alla raccolta playlist. | Evento Player. PlaylistCollectionPlaylistAdded
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Media Player di Windows Event PlaylistCollectionPlaylistAdded
- Windows Event PlaylistCollectionPlaylistAdded Media Player, classe Player
- Classe Player Windows Media Player, evento PlaylistCollectionPlaylistAdded
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329070"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a><span data-ttu-id="c31da-107">Evento Player. PlaylistCollectionPlaylistAdded</span><span class="sxs-lookup"><span data-stu-id="c31da-107">Player.PlaylistCollectionPlaylistAdded event</span></span>

<span data-ttu-id="c31da-108">L'evento **PlaylistCollectionPlaylistAdded** si verifica quando viene aggiunta una playlist alla raccolta playlist.</span><span class="sxs-lookup"><span data-stu-id="c31da-108">The **PlaylistCollectionPlaylistAdded** event occurs when a playlist is added to the playlist collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c31da-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c31da-109">Syntax</span></span>


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a><span data-ttu-id="c31da-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c31da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c31da-111">*bstrPlaylistName*</span><span class="sxs-lookup"><span data-stu-id="c31da-111">*bstrPlaylistName*</span></span> 
</dt> <dd>

<span data-ttu-id="c31da-112">**Stringa** che specifica il nome della playlist aggiunta.</span><span class="sxs-lookup"><span data-stu-id="c31da-112">**String** specifying the name of the playlist that was added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c31da-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c31da-113">Return value</span></span>

<span data-ttu-id="c31da-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c31da-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c31da-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c31da-115">Remarks</span></span>

<span data-ttu-id="c31da-116">Il nome della playlist aggiunta può essere usato per recuperare l'oggetto **playlist** corrispondente usando *PlaylistCollection*. metodo **GetByName** .</span><span class="sxs-lookup"><span data-stu-id="c31da-116">The name of the playlist that was added can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="c31da-117">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="c31da-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="c31da-118">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="c31da-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="c31da-119">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c31da-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="c31da-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c31da-120">Requirements</span></span>



| <span data-ttu-id="c31da-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c31da-121">Requirement</span></span> | <span data-ttu-id="c31da-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c31da-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c31da-123">Versione</span><span class="sxs-lookup"><span data-stu-id="c31da-123">Version</span></span><br/> | <span data-ttu-id="c31da-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="c31da-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c31da-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c31da-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="c31da-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c31da-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c31da-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c31da-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c31da-128">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="c31da-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="c31da-129">**PlaylistCollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="c31da-129">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





