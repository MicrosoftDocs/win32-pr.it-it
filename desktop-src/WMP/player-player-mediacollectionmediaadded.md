---
title: Evento Player. MediaCollectionMediaAdded
description: L'evento MediaCollectionMediaAdded si verifica quando un elemento multimediale viene aggiunto alla libreria locale. | Evento Player. MediaCollectionMediaAdded
ms.assetid: 01696d28-e83b-4fd2-8e88-2871831b61e7
keywords:
- Media Player di Windows Event MediaCollectionMediaAdded
- Windows Event MediaCollectionMediaAdded Media Player, classe Player
- Classe Player Windows Media Player, evento MediaCollectionMediaAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18dd0536f508090c46f9fc5a9059c809f50091d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331850"
---
# <a name="playermediacollectionmediaadded-event"></a><span data-ttu-id="81d04-107">Evento Player. MediaCollectionMediaAdded</span><span class="sxs-lookup"><span data-stu-id="81d04-107">Player.MediaCollectionMediaAdded event</span></span>

<span data-ttu-id="81d04-108">L'evento MediaCollectionMediaAdded si verifica quando un elemento multimediale viene aggiunto alla libreria locale.</span><span class="sxs-lookup"><span data-stu-id="81d04-108">The MediaCollectionMediaAdded event occurs when a media item is added to the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="81d04-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81d04-109">Syntax</span></span>


```JScript
Player.MediaCollectionMediaAdded(
  pdispMedia
)
```



## <a name="parameters"></a><span data-ttu-id="81d04-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="81d04-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81d04-111">*pdispMedia*</span><span class="sxs-lookup"><span data-stu-id="81d04-111">*pdispMedia*</span></span> 
</dt> <dd>

<span data-ttu-id="81d04-112">Oggetto **multimediale** aggiunto.</span><span class="sxs-lookup"><span data-stu-id="81d04-112">**Media** object that was added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81d04-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81d04-113">Return value</span></span>

<span data-ttu-id="81d04-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="81d04-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81d04-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="81d04-115">Remarks</span></span>

<span data-ttu-id="81d04-116">Questo evento si verifica solo per la libreria locale.</span><span class="sxs-lookup"><span data-stu-id="81d04-116">This event only occurs for the local library.</span></span>

<span data-ttu-id="81d04-117">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="81d04-117">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="81d04-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81d04-118">Requirements</span></span>



| <span data-ttu-id="81d04-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="81d04-119">Requirement</span></span> | <span data-ttu-id="81d04-120">Valore</span><span class="sxs-lookup"><span data-stu-id="81d04-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81d04-121">Versione</span><span class="sxs-lookup"><span data-stu-id="81d04-121">Version</span></span><br/> | <span data-ttu-id="81d04-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="81d04-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="81d04-123">DLL</span><span class="sxs-lookup"><span data-stu-id="81d04-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="81d04-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81d04-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81d04-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81d04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d04-126">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="81d04-126">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="81d04-127">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="81d04-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="81d04-128">**Player. mediacollection**</span><span class="sxs-lookup"><span data-stu-id="81d04-128">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





