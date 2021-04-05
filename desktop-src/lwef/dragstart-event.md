---
title: Evento DragStart
description: Evento DragStart
ms.assetid: fef0ae05-1958-45c6-8260-107c47b5fa92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e382e77c87848226568755c06d2541ebb4db14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044691"
---
# <a name="dragstart-event"></a><span data-ttu-id="38a99-103">Evento DragStart</span><span class="sxs-lookup"><span data-stu-id="38a99-103">DragStart Event</span></span>

<span data-ttu-id="38a99-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="38a99-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="38a99-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="38a99-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="38a99-106">Si verifica quando l'utente inizia a trascinare un carattere.</span><span class="sxs-lookup"><span data-stu-id="38a99-106">Occurs when the user begins dragging a character.</span></span>

</dd> <dt>

<span data-ttu-id="38a99-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="38a99-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="38a99-108"> *Agente secondario\ *\ *\ * \_ DragStart*\ *  **(ByVal** *CharacterID*, **(** *pulsante* ByVal, **(ByVal** *Shift*, **(** ByVal *X*, **(ByVal** *Y\ *\ * *)**</span><span class="sxs-lookup"><span data-stu-id="38a99-108">**Sub** *agent\*\*\*\_DragStart*\* **(ByVal** *CharacterID*, **(ByVal** *Button*, **(ByVal** *Shift*, **(ByVal** *X*, **(ByVal** *Y\*\*\*)*\*</span></span>



| <span data-ttu-id="38a99-109">Parte</span><span class="sxs-lookup"><span data-stu-id="38a99-109">Part</span></span>          | <span data-ttu-id="38a99-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38a99-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38a99-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="38a99-111">*CharacterID*</span></span> | <span data-ttu-id="38a99-112">Restituisce l'ID del carattere selezionato sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="38a99-112">Returns the ID of the clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="38a99-113">*Button*</span><span class="sxs-lookup"><span data-stu-id="38a99-113">*Button*</span></span>      | <span data-ttu-id="38a99-114">Restituisce un intero che identifica il pulsante che è stato premuto e rilasciato per generare l'evento.</span><span class="sxs-lookup"><span data-stu-id="38a99-114">Returns an integer that identifies the button that was pressed and released to cause the event.</span></span> <span data-ttu-id="38a99-115">L'argomento del pulsante è un bit con bit corrispondente al pulsante sinistro (bit 0), pulsante destro (bit 1) e pulsante centrale (bit 2).</span><span class="sxs-lookup"><span data-stu-id="38a99-115">The button argument is a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="38a99-116">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="38a99-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="38a99-117">Viene impostato solo uno dei bit, che indica il pulsante che ha causato l'evento.</span><span class="sxs-lookup"><span data-stu-id="38a99-117">Only one of the bits is set, indicating the button that caused the event.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="38a99-118">*MAIUSC*</span><span class="sxs-lookup"><span data-stu-id="38a99-118">*Shift*</span></span>       | <span data-ttu-id="38a99-119">Restituisce un intero che corrisponde allo stato dei tasti MAIUSC, CTRL e ALT quando il pulsante specificato nell'argomento del pulsante viene premuto o rilasciato.</span><span class="sxs-lookup"><span data-stu-id="38a99-119">Returns an integer that corresponds to the state of the SHIFT, CTRL, and ALT keys when the button specified in the button argument is pressed or released.</span></span> <span data-ttu-id="38a99-120">Se la chiave è inattiva, viene impostato un bit.</span><span class="sxs-lookup"><span data-stu-id="38a99-120">A bit is set if the key is down.</span></span> <span data-ttu-id="38a99-121">L'argomento Shift è un bit con i bit meno significativi che corrispondono al tasto MAIUSC (bit 0), il tasto CTRL (bit 1) e il tasto ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="38a99-121">The shift argument is a bitfield with the least-significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="38a99-122">Questi bit corrispondono rispettivamente ai valori 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="38a99-122">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="38a99-123">L'argomento Shift indica lo stato di queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="38a99-123">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="38a99-124">È possibile impostare some, all o nessuno dei bit, a indicare che vengono premuti alcuni, tutti o nessuno dei tasti.</span><span class="sxs-lookup"><span data-stu-id="38a99-124">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span> <span data-ttu-id="38a99-125">Se, ad esempio, sono stati premuti sia CTRL che ALT, il valore di Shift sarà 6.</span><span class="sxs-lookup"><span data-stu-id="38a99-125">For example, if both CTRL and ALT were pressed, the value of shift would be 6.</span></span> |
| <span data-ttu-id="38a99-126">*X, Y*</span><span class="sxs-lookup"><span data-stu-id="38a99-126">*X,Y*</span></span>         | <span data-ttu-id="38a99-127">Restituisce un Integer che specifica la posizione corrente del puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="38a99-127">Returns an integer that specifies the current location of the mouse pointer.</span></span> <span data-ttu-id="38a99-128">I valori X e Y sono sempre espressi in pixel, in relazione all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="38a99-128">The X and Y values are always expressed in pixels, relative to the upper left corner of the screen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="38a99-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="38a99-129">Remarks</span></span>

<span data-ttu-id="38a99-130">Questo evento viene inviato solo al client attivo di input di un carattere.</span><span class="sxs-lookup"><span data-stu-id="38a99-130">This event is sent only to the input-active client of a character.</span></span> <span data-ttu-id="38a99-131">Quando l'utente trascina un carattere senza client attivo di input, il server imposta l'ultimo client attivo di input come il client attivo di input corrente, inviando l'evento [**ActivateInput**](activateinput-event.md) al client e quindi inviando l'evento **DragStart** .</span><span class="sxs-lookup"><span data-stu-id="38a99-131">When the user drags a character with no input-active client, the server sets its last input-active client as the current input-active client, sending the [**ActivateInput**](activateinput-event.md) event to that client, and then sending the **DragStart** event.</span></span>

### <a name="see-also"></a><span data-ttu-id="38a99-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="38a99-132">See Also</span></span>

[<span data-ttu-id="38a99-133">**Evento DragComplete**</span><span class="sxs-lookup"><span data-stu-id="38a99-133">**DragComplete event**</span></span>](dragcomplete-event.md)


 

 




