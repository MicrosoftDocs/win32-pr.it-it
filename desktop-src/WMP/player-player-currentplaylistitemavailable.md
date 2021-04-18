---
title: Evento Player. CurrentPlaylistItemAvailable
description: L'evento CurrentPlaylistItemAvailable si verifica quando la playlist corrente diventa disponibile. | Evento Player. CurrentPlaylistItemAvailable
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Media Player di Windows Event CurrentPlaylistItemAvailable
- Windows Event CurrentPlaylistItemAvailable Media Player, classe Player
- Classe Player Windows Media Player, evento CurrentPlaylistItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328874"
---
# <a name="playercurrentplaylistitemavailable-event"></a><span data-ttu-id="49433-107">Evento Player. CurrentPlaylistItemAvailable</span><span class="sxs-lookup"><span data-stu-id="49433-107">Player.CurrentPlaylistItemAvailable event</span></span>

<span data-ttu-id="49433-108">L'evento **CurrentPlaylistItemAvailable** si verifica quando la playlist corrente diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="49433-108">The **CurrentPlaylistItemAvailable** event occurs when the current playlist becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="49433-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49433-109">Syntax</span></span>


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="49433-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="49433-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49433-111">*bstrItemName*</span><span class="sxs-lookup"><span data-stu-id="49433-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="49433-112">**Stringa** che contiene il nome dell'elemento della playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="49433-112">**String** containing the name of the current playlist item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49433-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49433-113">Return value</span></span>

<span data-ttu-id="49433-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="49433-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49433-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="49433-115">Remarks</span></span>

<span data-ttu-id="49433-116">Il nome della playlist corrente può essere usato per recuperare l'oggetto **playlist** corrispondente usando *PlaylistCollection*. metodo **GetByName** .</span><span class="sxs-lookup"><span data-stu-id="49433-116">The name of the current playlist can be used to retrieve the corresponding **Playlist** object using the *PlaylistCollection*.**getByName** method.</span></span>

<span data-ttu-id="49433-117">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="49433-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="49433-118">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="49433-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="49433-119">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="49433-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="49433-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49433-120">Requirements</span></span>



| <span data-ttu-id="49433-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="49433-121">Requirement</span></span> | <span data-ttu-id="49433-122">Valore</span><span class="sxs-lookup"><span data-stu-id="49433-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="49433-123">Versione</span><span class="sxs-lookup"><span data-stu-id="49433-123">Version</span></span><br/> | <span data-ttu-id="49433-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="49433-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="49433-125">DLL</span><span class="sxs-lookup"><span data-stu-id="49433-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="49433-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49433-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49433-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49433-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49433-128">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="49433-128">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="49433-129">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="49433-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="49433-130">**PlaylistCollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="49433-130">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





