---
title: Evento Player. Click
description: L'evento click si verifica quando l'utente fa clic su un pulsante del mouse.
ms.assetid: c2d5fab9-9b53-4d0c-a001-8cbf4430e713
keywords:
- Fare clic su Windows Event Media Player
- Fare clic su evento Windows Media Player, classe lettore
- Classe Player Windows Media Player, fare clic su evento
topic_type:
- apiref
api_name:
- Player.Click
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8389460d59018b221749719d32edbaa89943808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328290"
---
# <a name="playerclick-event"></a><span data-ttu-id="65584-106">Evento Player. Click</span><span class="sxs-lookup"><span data-stu-id="65584-106">Player.Click event</span></span>

<span data-ttu-id="65584-107">L'evento **Click** si verifica quando l'utente fa clic su un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="65584-107">The **Click** event occurs when the user clicks a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="65584-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65584-108">Syntax</span></span>


```JScript
Player.Click(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="65584-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="65584-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65584-110">*Npulsante*</span><span class="sxs-lookup"><span data-stu-id="65584-110">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="65584-111">**Number** (**int**) che specifica un bit con bit corrispondenti al pulsante sinistro (bit 0), al pulsante destro (bit 1) e al pulsante centrale (bit 2).</span><span class="sxs-lookup"><span data-stu-id="65584-111">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="65584-112">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="65584-112">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="65584-113">Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.</span><span class="sxs-lookup"><span data-stu-id="65584-113">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="65584-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="65584-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="65584-115">**Number** (**int**) che specifica un bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), il tasto Ctrl (bit 1) e il tasto Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="65584-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="65584-116">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="65584-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="65584-117">L'argomento Shift indica lo stato di queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="65584-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="65584-118">È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.</span><span class="sxs-lookup"><span data-stu-id="65584-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="65584-119">*fX*</span><span class="sxs-lookup"><span data-stu-id="65584-119">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="65584-120">**Numero** (**Long**) che specifica la coordinata x del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.</span><span class="sxs-lookup"><span data-stu-id="65584-120">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="65584-121">*fY*</span><span class="sxs-lookup"><span data-stu-id="65584-121">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="65584-122">**Numero** (**Long**) che specifica la coordinata y del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.</span><span class="sxs-lookup"><span data-stu-id="65584-122">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65584-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65584-123">Return value</span></span>

<span data-ttu-id="65584-124">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="65584-124">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65584-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="65584-125">Remarks</span></span>

<span data-ttu-id="65584-126">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="65584-126">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="65584-127">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="65584-127">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="65584-128">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="65584-128">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="65584-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65584-129">Requirements</span></span>



| <span data-ttu-id="65584-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="65584-130">Requirement</span></span> | <span data-ttu-id="65584-131">Valore</span><span class="sxs-lookup"><span data-stu-id="65584-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65584-132">Versione</span><span class="sxs-lookup"><span data-stu-id="65584-132">Version</span></span><br/> | <span data-ttu-id="65584-133">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="65584-133">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="65584-134">DLL</span><span class="sxs-lookup"><span data-stu-id="65584-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="65584-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65584-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65584-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65584-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65584-137">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="65584-137">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





