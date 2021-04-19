---
title: Evento Player. MediaCollectionMediaRemoved
description: L'evento MediaCollectionMediaRemoved si verifica quando un elemento multimediale viene rimosso dalla libreria locale. | Evento Player. MediaCollectionMediaRemoved
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- Media Player di Windows Event MediaCollectionMediaRemoved
- Windows Event MediaCollectionMediaRemoved Media Player, classe Player
- Classe Player Windows Media Player, evento MediaCollectionMediaRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72af5fe4c5e90effeb34745ea71e3edb457da357
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333243"
---
# <a name="playermediacollectionmediaremoved-event"></a><span data-ttu-id="248d3-107">Evento Player. MediaCollectionMediaRemoved</span><span class="sxs-lookup"><span data-stu-id="248d3-107">Player.MediaCollectionMediaRemoved event</span></span>

<span data-ttu-id="248d3-108">L'evento MediaCollectionMediaRemoved si verifica quando un elemento multimediale viene rimosso dalla libreria locale.</span><span class="sxs-lookup"><span data-stu-id="248d3-108">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="248d3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="248d3-109">Syntax</span></span>


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a><span data-ttu-id="248d3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="248d3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="248d3-111">*pdispMedia*</span><span class="sxs-lookup"><span data-stu-id="248d3-111">*pdispMedia*</span></span> 
</dt> <dd>

<span data-ttu-id="248d3-112">Oggetto **multimediale** che è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="248d3-112">**Media** object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="248d3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="248d3-113">Return value</span></span>

<span data-ttu-id="248d3-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="248d3-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="248d3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="248d3-115">Remarks</span></span>

<span data-ttu-id="248d3-116">Questo evento si verifica solo per la libreria locale.</span><span class="sxs-lookup"><span data-stu-id="248d3-116">This event only occurs for the local library.</span></span>

<span data-ttu-id="248d3-117">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="248d3-117">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="248d3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="248d3-118">Requirements</span></span>



| <span data-ttu-id="248d3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="248d3-119">Requirement</span></span> | <span data-ttu-id="248d3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="248d3-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="248d3-121">Versione</span><span class="sxs-lookup"><span data-stu-id="248d3-121">Version</span></span><br/> | <span data-ttu-id="248d3-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="248d3-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="248d3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="248d3-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="248d3-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="248d3-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="248d3-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="248d3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="248d3-126">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="248d3-126">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="248d3-127">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="248d3-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="248d3-128">**Player. mediacollection**</span><span class="sxs-lookup"><span data-stu-id="248d3-128">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





