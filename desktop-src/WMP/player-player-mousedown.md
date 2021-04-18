---
title: Evento Player. MouseDown
description: L'evento MouseDown si verifica quando l'utente preme un pulsante del mouse. | Evento Player. MouseDown
ms.assetid: cc2fd2ca-c974-4683-98ca-2202c4d5b240
keywords:
- Finestre eventi MouseDown Media Player
- Evento MouseDown Windows Media Player, classe Player
- Classe Player Windows Media Player, evento MouseDown
topic_type:
- apiref
api_name:
- Player.MouseDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29eb0c8aa5f6731f94d0e4c3b4ff967cb7819f42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328199"
---
# <a name="playermousedown-event"></a><span data-ttu-id="2ac76-107">Evento Player. MouseDown</span><span class="sxs-lookup"><span data-stu-id="2ac76-107">Player.MouseDown event</span></span>

<span data-ttu-id="2ac76-108">L'evento **MouseDown** si verifica quando l'utente preme un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="2ac76-108">The **MouseDown** event occurs when the user presses a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ac76-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ac76-109">Syntax</span></span>


```JScript
Player.MouseDown(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="2ac76-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ac76-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ac76-111">*Npulsante*</span><span class="sxs-lookup"><span data-stu-id="2ac76-111">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="2ac76-112">**Number** (**int**) che specifica un bit con bit corrispondenti al pulsante sinistro (bit 0), al pulsante destro (bit 1) e al pulsante centrale (bit 2).</span><span class="sxs-lookup"><span data-stu-id="2ac76-112">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="2ac76-113">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="2ac76-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="2ac76-114">Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.</span><span class="sxs-lookup"><span data-stu-id="2ac76-114">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="2ac76-115">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="2ac76-115">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="2ac76-116">**Number** (**int**) che specifica un bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), il tasto Ctrl (bit 1) e il tasto Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="2ac76-116">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="2ac76-117">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="2ac76-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="2ac76-118">L'argomento Shift indica lo stato di queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="2ac76-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="2ac76-119">È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.</span><span class="sxs-lookup"><span data-stu-id="2ac76-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="2ac76-120">*fX*</span><span class="sxs-lookup"><span data-stu-id="2ac76-120">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="2ac76-121">**Numero** (**Long**) che specifica la coordinata x del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.</span><span class="sxs-lookup"><span data-stu-id="2ac76-121">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="2ac76-122">*fY*</span><span class="sxs-lookup"><span data-stu-id="2ac76-122">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="2ac76-123">**Numero** (**Long**) che specifica la coordinata y del puntatore del mouse rispetto all'angolo superiore sinistro del controllo.</span><span class="sxs-lookup"><span data-stu-id="2ac76-123">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ac76-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ac76-124">Return value</span></span>

<span data-ttu-id="2ac76-125">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2ac76-125">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ac76-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ac76-126">Remarks</span></span>

<span data-ttu-id="2ac76-127">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="2ac76-127">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="2ac76-128">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="2ac76-128">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="2ac76-129">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2ac76-129">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ac76-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ac76-130">Requirements</span></span>



| <span data-ttu-id="2ac76-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ac76-131">Requirement</span></span> | <span data-ttu-id="2ac76-132">Valore</span><span class="sxs-lookup"><span data-stu-id="2ac76-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac76-133">Versione</span><span class="sxs-lookup"><span data-stu-id="2ac76-133">Version</span></span><br/> | <span data-ttu-id="2ac76-134">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="2ac76-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="2ac76-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2ac76-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="2ac76-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ac76-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ac76-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ac76-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ac76-138">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="2ac76-138">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





