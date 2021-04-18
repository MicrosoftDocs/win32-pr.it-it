---
title: Evento Player. PositionChange
description: L'evento PositionChange si verifica quando la posizione corrente dell'elemento multimediale è stata modificata.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Media Player di Windows Event PositionChange
- Windows Event PositionChange Media Player, classe Player
- Classe Player Windows Media Player, evento PositionChange
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327717"
---
# <a name="playerpositionchange-event"></a><span data-ttu-id="eefc3-106">Evento Player. PositionChange</span><span class="sxs-lookup"><span data-stu-id="eefc3-106">Player.PositionChange event</span></span>

<span data-ttu-id="eefc3-107">L'evento **PositionChange** si verifica quando la posizione corrente dell'elemento multimediale è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="eefc3-107">The **PositionChange** event occurs when the current position of the media item has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="eefc3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eefc3-108">Syntax</span></span>


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a><span data-ttu-id="eefc3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="eefc3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eefc3-110">*oldPosition*</span><span class="sxs-lookup"><span data-stu-id="eefc3-110">*oldPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="eefc3-111">Numero (**Double**) che specifica la posizione precedente.</span><span class="sxs-lookup"><span data-stu-id="eefc3-111">Number (**double**) specifying the old position.</span></span>

</dd> <dt>

<span data-ttu-id="eefc3-112">*newPosition*</span><span class="sxs-lookup"><span data-stu-id="eefc3-112">*newPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="eefc3-113">**Numero** (**Double**) che specifica la nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="eefc3-113">**Number** (**double**) specifying the new position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eefc3-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eefc3-114">Return value</span></span>

<span data-ttu-id="eefc3-115">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="eefc3-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eefc3-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="eefc3-116">Remarks</span></span>

<span data-ttu-id="eefc3-117">Questo evento non viene generato periodicamente durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="eefc3-117">This event is not raised routinely during playback.</span></span> <span data-ttu-id="eefc3-118">Si verifica solo quando un elemento modifica attivamente la posizione corrente dell'elemento multimediale in riproduzione, ad esempio l'utente che sposta il handle di ricerca o il codice specificando un valore per i *controlli*. **currentPosition**.</span><span class="sxs-lookup"><span data-stu-id="eefc3-118">It only occurs when something actively changes the current position of the playing media item, such as the user moving the seek handle or code specifying a value for *Controls*.**currentPosition**.</span></span>

<span data-ttu-id="eefc3-119">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="eefc3-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="eefc3-120">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="eefc3-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="eefc3-121">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="eefc3-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="eefc3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eefc3-122">Requirements</span></span>



| <span data-ttu-id="eefc3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="eefc3-123">Requirement</span></span> | <span data-ttu-id="eefc3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="eefc3-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eefc3-125">Versione</span><span class="sxs-lookup"><span data-stu-id="eefc3-125">Version</span></span><br/> | <span data-ttu-id="eefc3-126">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="eefc3-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="eefc3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="eefc3-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="eefc3-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eefc3-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eefc3-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eefc3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eefc3-130">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="eefc3-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





