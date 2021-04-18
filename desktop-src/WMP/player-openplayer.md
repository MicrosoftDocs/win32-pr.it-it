---
title: Player. openPlayer, metodo
description: Il metodo openPlayer apre Windows Media Player usando l'URL specificato. | Player. openPlayer, metodo
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- Metodo openPlayer Windows Media Player
- Metodo openPlayer Windows Media Player, classe Player
- Classe Player Windows Media Player, metodo openPlayer
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327067"
---
# <a name="playeropenplayer-method"></a><span data-ttu-id="b6935-107">Player. openPlayer, metodo</span><span class="sxs-lookup"><span data-stu-id="b6935-107">Player.openPlayer method</span></span>

<span data-ttu-id="b6935-108">Il metodo **openPlayer** apre Windows Media Player usando l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="b6935-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6935-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6935-109">Syntax</span></span>


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="b6935-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6935-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6935-111">*URL* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b6935-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6935-112">**Stringa** che rappresenta l'URL dell'elemento multimediale da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="b6935-112">**String** representing the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6935-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6935-113">Return value</span></span>

<span data-ttu-id="b6935-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b6935-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6935-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6935-115">Remarks</span></span>

<span data-ttu-id="b6935-116">Questo metodo avvia Media Player Windows con l'URL specificato impostato come elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="b6935-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="b6935-117">Se il lettore è stato chiuso in precedenza in modalità Skin, verrà aperto utilizzando l'ultima interfaccia selezionata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b6935-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="b6935-118">In caso contrario, il lettore verrà aperto in modalità completa.</span><span class="sxs-lookup"><span data-stu-id="b6935-118">Otherwise, the Player opens in full mode.</span></span>

<span data-ttu-id="b6935-119">Se questo metodo viene chiamato da un controllo Windows Media PlayerActiveX incorporato in modalità remota, il comportamento è identico a quello di *PlayerApplication*. metodo **switchToPlayerApplication** .</span><span class="sxs-lookup"><span data-stu-id="b6935-119">If this method is called from a Windows Media PlayerActiveX control embedded in remote mode, its behavior is identical to the *PlayerApplication*.**switchToPlayerApplication** method.</span></span>

<span data-ttu-id="b6935-120">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b6935-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6935-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6935-121">Requirements</span></span>



| <span data-ttu-id="b6935-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6935-122">Requirement</span></span> | <span data-ttu-id="b6935-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b6935-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6935-124">Versione</span><span class="sxs-lookup"><span data-stu-id="b6935-124">Version</span></span><br/> | <span data-ttu-id="b6935-125">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="b6935-125">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="b6935-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b6935-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="b6935-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6935-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6935-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6935-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6935-129">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="b6935-129">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="b6935-130">**PlayerApplication.switchToPlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="b6935-130">**PlayerApplication.switchToPlayerApplication**</span></span>](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





