---
title: Evento Player. KeyUp
description: L'evento KeyUp si verifica quando viene rilasciato un tasto. | Evento Player. KeyUp
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- Media Player di eventi KeyUp di Windows
- Evento KeyUp Windows Media Player, classe Player
- Classe Player Windows Media Player, evento KeyUp
topic_type:
- apiref
api_name:
- Player.KeyUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06e9b77871e9f62d46bdfa223bfa40b87feaf06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326310"
---
# <a name="playerkeyup-event"></a><span data-ttu-id="56069-107">Evento Player. KeyUp</span><span class="sxs-lookup"><span data-stu-id="56069-107">Player.KeyUp event</span></span>

<span data-ttu-id="56069-108">L'evento **KeyUp** si verifica quando viene rilasciato un tasto.</span><span class="sxs-lookup"><span data-stu-id="56069-108">The **KeyUp** event occurs when a key is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="56069-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56069-109">Syntax</span></span>


```JScript
Player.KeyUp(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="56069-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="56069-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56069-111">*nKeyCode*</span><span class="sxs-lookup"><span data-stu-id="56069-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="56069-112">**Numero** (**int**) che specifica quale tasto fisico è premuto.</span><span class="sxs-lookup"><span data-stu-id="56069-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="56069-113">Per i valori possibili, vedere [evento Player. KeyDown](player-player-keydown.md).</span><span class="sxs-lookup"><span data-stu-id="56069-113">For possible values, see [Player.KeyDown Event](player-player-keydown.md).</span></span>

</dd> <dt>

<span data-ttu-id="56069-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="56069-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="56069-115">**Number** (**int**) che specifica un bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), il tasto Ctrl (bit 1) e il tasto Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="56069-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="56069-116">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="56069-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="56069-117">L'argomento Shift indica lo stato di queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="56069-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="56069-118">È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.</span><span class="sxs-lookup"><span data-stu-id="56069-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56069-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56069-119">Return value</span></span>

<span data-ttu-id="56069-120">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="56069-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56069-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="56069-121">Remarks</span></span>

<span data-ttu-id="56069-122">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="56069-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="56069-123">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="56069-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="56069-124">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="56069-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="56069-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56069-125">Requirements</span></span>



| <span data-ttu-id="56069-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="56069-126">Requirement</span></span> | <span data-ttu-id="56069-127">Valore</span><span class="sxs-lookup"><span data-stu-id="56069-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="56069-128">Versione</span><span class="sxs-lookup"><span data-stu-id="56069-128">Version</span></span><br/> | <span data-ttu-id="56069-129">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="56069-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="56069-130">DLL</span><span class="sxs-lookup"><span data-stu-id="56069-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="56069-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56069-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56069-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56069-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56069-133">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="56069-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





