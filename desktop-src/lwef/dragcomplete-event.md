---
title: Evento DragComplete
description: Evento DragComplete
ms.assetid: b48e7097-9d9d-4eab-9dfc-68dbc9793382
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7a02fe98e4cf3cdefc1b7734305067550e4923
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298361"
---
# <a name="dragcomplete-event"></a><span data-ttu-id="487d7-103">Evento DragComplete</span><span class="sxs-lookup"><span data-stu-id="487d7-103">DragComplete Event</span></span>

<span data-ttu-id="487d7-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="487d7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="487d7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="487d7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="487d7-106">Si verifica al completamento del trascinamento di un carattere da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="487d7-106">Occurs when the user completes dragging a character.</span></span>

</dd> <dt>

<span data-ttu-id="487d7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="487d7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="487d7-108">Agente **secondario** \*\* \* \* \_ DragComplete\* \*  **(ByVal** *CharacterID*,  *pulsante* ByVal, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="487d7-108">**Sub** *agent\*\*\*\_DragComplete*\* **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y\*\*\*)*\*</span></span>



| <span data-ttu-id="487d7-109">Parte</span><span class="sxs-lookup"><span data-stu-id="487d7-109">Part</span></span>          | <span data-ttu-id="487d7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="487d7-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="487d7-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="487d7-111">*CharacterID*</span></span> | <span data-ttu-id="487d7-112">Restituisce l'ID del carattere trascinato sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="487d7-112">Returns the ID of the dragged character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="487d7-113">*Button*</span><span class="sxs-lookup"><span data-stu-id="487d7-113">*Button*</span></span>      | <span data-ttu-id="487d7-114">Restituisce un intero che identifica il pulsante che è stato premuto e rilasciato per generare l'evento.</span><span class="sxs-lookup"><span data-stu-id="487d7-114">Returns an integer that identifies the button that was pressed and released to cause the event.</span></span> <span data-ttu-id="487d7-115">L'argomento del pulsante è un bit con bit corrispondente al pulsante sinistro (bit 0), pulsante destro (bit 1) e pulsante centrale (bit 2).</span><span class="sxs-lookup"><span data-stu-id="487d7-115">The button argument is a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="487d7-116">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="487d7-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="487d7-117">Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.</span><span class="sxs-lookup"><span data-stu-id="487d7-117">Only one of the bits is set, indicating the button that caused the event.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="487d7-118">*MAIUSC*</span><span class="sxs-lookup"><span data-stu-id="487d7-118">*Shift*</span></span>       | <span data-ttu-id="487d7-119">Restituisce un intero che corrisponde allo stato dei tasti MAIUSC, CTRL e ALT quando il pulsante specificato nell'argomento del pulsante viene premuto o rilasciato.</span><span class="sxs-lookup"><span data-stu-id="487d7-119">Returns an integer that corresponds to the state of the SHIFT, CTRL, and ALT keys when the button specified in the button argument is pressed or released.</span></span> <span data-ttu-id="487d7-120">Se la chiave è inattiva, viene impostato un bit.</span><span class="sxs-lookup"><span data-stu-id="487d7-120">A bit is set if the key is down.</span></span> <span data-ttu-id="487d7-121">L'argomento Shift è un bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), il tasto CTRL (bit 1) e il tasto ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="487d7-121">The shift argument is a bitfield with the least-significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="487d7-122">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="487d7-122">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="487d7-123">L'argomento Shift indica lo stato di queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="487d7-123">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="487d7-124">È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.</span><span class="sxs-lookup"><span data-stu-id="487d7-124">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span> <span data-ttu-id="487d7-125">Se, ad esempio, sono stati premuti sia CTRL che ALT, il valore di Shift sarà 6.</span><span class="sxs-lookup"><span data-stu-id="487d7-125">For example, if both CTRL and ALT were pressed, the value of shift would be 6.</span></span> |
| <span data-ttu-id="487d7-126">*X, Y*</span><span class="sxs-lookup"><span data-stu-id="487d7-126">*X,Y*</span></span>         | <span data-ttu-id="487d7-127">Restituisce un Integer che specifica la posizione corrente del puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="487d7-127">Returns an integer that specifies the current location of the mouse pointer.</span></span> <span data-ttu-id="487d7-128">I valori X e Y sono sempre espressi in pixel, in relazione all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="487d7-128">The X and Y values are always expressed in pixels, relative to the upper left corner of the screen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="487d7-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="487d7-129">Remarks</span></span>

<span data-ttu-id="487d7-130">Questo evento viene inviato solo al client attivo di input di un carattere.</span><span class="sxs-lookup"><span data-stu-id="487d7-130">This event is sent only to the input-active client of a character.</span></span> <span data-ttu-id="487d7-131">Quando l'utente trascina un carattere senza client attivo per l'input, il server imposta l'ultimo client attivo di input come input corrente-client attivo, inviando l'evento [**ActivateInput**](activateinput-event.md) al client e quindi inviando gli eventi [**DragStart**](dragstart-event.md) e **DragComplete** .</span><span class="sxs-lookup"><span data-stu-id="487d7-131">When the user drags a character with no input-active client, the server sets its last input-active client as the current input-active client, sending the [**ActivateInput**](activateinput-event.md) event to that client, and then sending the [**DragStart**](dragstart-event.md) and **DragComplete** events.</span></span>

### <a name="see-also"></a><span data-ttu-id="487d7-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="487d7-132">See Also</span></span>

[<span data-ttu-id="487d7-133">**Evento DragStart**</span><span class="sxs-lookup"><span data-stu-id="487d7-133">**DragStart event**</span></span>](dragstart-event.md)


 

 




