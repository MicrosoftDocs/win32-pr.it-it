---
title: Evento HelpComplete
description: Evento HelpComplete
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299705"
---
# <a name="helpcomplete-event"></a><span data-ttu-id="51a0c-103">Evento HelpComplete</span><span class="sxs-lookup"><span data-stu-id="51a0c-103">HelpComplete Event</span></span>

<span data-ttu-id="51a0c-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51a0c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="51a0c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="51a0c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="51a0c-106">Indica che la modalità della Guida sensibile al contesto è stata chiusa.</span><span class="sxs-lookup"><span data-stu-id="51a0c-106">Indicates that context-sensitive Help mode has been exited.</span></span>

</dd> <dt>

<span data-ttu-id="51a0c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="51a0c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="51a0c-108">Agente **secondario** *. \* \* \* (ByVal* \*  \*CharacterID \* \* *, ByVal* \*  \*Name \* \* *, ByVal* \*  *causare \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="51a0c-108">**Sub** *agent.\*\*\*(ByVal*\* *CharacterID\*\*\*, ByVal*\* *Name\*\*\*, ByVal*\* *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="51a0c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="51a0c-109">Part</span></span>          | <span data-ttu-id="51a0c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51a0c-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51a0c-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="51a0c-111">*CharacterID*</span></span> | <span data-ttu-id="51a0c-112">Restituisce l'ID del carattere selezionato sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="51a0c-112">Returns the ID of the clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="51a0c-113">*Nome*</span><span class="sxs-lookup"><span data-stu-id="51a0c-113">*Name*</span></span>        | <span data-ttu-id="51a0c-114">Restituisce un valore stringa che identifica il nome (ID) del comando.</span><span class="sxs-lookup"><span data-stu-id="51a0c-114">Returns a string value identifying the name (ID) of the command.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="51a0c-115">*Causa*</span><span class="sxs-lookup"><span data-stu-id="51a0c-115">*Cause*</span></span>       | <span data-ttu-id="51a0c-116">Restituisce un valore che indica la causa del completamento della modalità della guida.</span><span class="sxs-lookup"><span data-stu-id="51a0c-116">Returns a value that indicates what caused the Help mode to complete.</span></span> <span data-ttu-id="51a0c-117">1 l'utente ha selezionato un comando fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="51a0c-117">1 The user selected a command supplied by your application.</span></span><br/> <span data-ttu-id="51a0c-118">2 l'utente ha selezionato l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) di un altro client.</span><span class="sxs-lookup"><span data-stu-id="51a0c-118">2 The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span><br/> <span data-ttu-id="51a0c-119">3 l'utente ha selezionato il comando Open Voice Commands.</span><span class="sxs-lookup"><span data-stu-id="51a0c-119">3 The user selected the Open Voice Commands command.</span></span><br/> <span data-ttu-id="51a0c-120">4 l'utente ha selezionato il comando Chiudi voce comandi.</span><span class="sxs-lookup"><span data-stu-id="51a0c-120">4 The user selected the Close Voice Commands command.</span></span><br/> <span data-ttu-id="51a0c-121">5 l'utente ha selezionato il comando Mostra *caratteriname* .</span><span class="sxs-lookup"><span data-stu-id="51a0c-121">5 The user selected the Show *CharacterName* command.</span></span><br/> <span data-ttu-id="51a0c-122">6 l'utente ha selezionato il comando Nascondi *caratterename* .</span><span class="sxs-lookup"><span data-stu-id="51a0c-122">6 The user selected the Hide *CharacterName* command.</span></span><br/> <span data-ttu-id="51a0c-123">7 l'utente ha selezionato (selezionato) il carattere.</span><span class="sxs-lookup"><span data-stu-id="51a0c-123">7 The user selected (clicked) the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="51a0c-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="51a0c-124">Remarks</span></span>

<span data-ttu-id="51a0c-125">In genere, la modalità della guida viene completata quando l'utente fa clic o trascina il carattere o seleziona un comando dal menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="51a0c-125">Typically, Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="51a0c-126">Se si fa clic su un altro carattere o altrove sullo schermo, la modalità della guida non viene annullata.</span><span class="sxs-lookup"><span data-stu-id="51a0c-126">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="51a0c-127">Il client che imposta la modalità della Guida per il carattere può annullare la modalità della Guida impostando [**HelpModeOn**](helpmodeon-property.md) su **false**.</span><span class="sxs-lookup"><span data-stu-id="51a0c-127">The client that set Help mode for the character can cancel Help mode by setting [**HelpModeOn**](helpmodeon-property.md) to **False**.</span></span> <span data-ttu-id="51a0c-128">(L'evento **HelpComplete** non viene attivato).</span><span class="sxs-lookup"><span data-stu-id="51a0c-128">(This does not trigger the **HelpComplete** event.)</span></span>

<span data-ttu-id="51a0c-129">Quando l'utente seleziona un comando dal menu popup del carattere in modalità guida, il server rimuove il menu, chiama la guida con il [**HelpContextID**](helpcontextid-property.md)specificato del comando e invia questo evento.</span><span class="sxs-lookup"><span data-stu-id="51a0c-129">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="51a0c-130">L'oggetto sensibile al contesto (noto anche come?) La finestra della guida viene visualizzata nella posizione del puntatore.</span><span class="sxs-lookup"><span data-stu-id="51a0c-130">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="51a0c-131">Se l'utente seleziona il comando in base all'input vocale, la finestra della guida viene visualizzata sopra il carattere.</span><span class="sxs-lookup"><span data-stu-id="51a0c-131">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="51a0c-132">Se il carattere è esterno allo schermo, la finestra viene visualizzata sullo schermo più vicino alla posizione corrente del carattere.</span><span class="sxs-lookup"><span data-stu-id="51a0c-132">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="51a0c-133">Se il server restituisce un nome come stringa vuota (""), indica che l'utente ha selezionato un comando fornito dal server.</span><span class="sxs-lookup"><span data-stu-id="51a0c-133">If the server returns Name as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="51a0c-134">Questo evento viene inviato solo all'applicazione client che inserisce il carattere in modalità guida.</span><span class="sxs-lookup"><span data-stu-id="51a0c-134">This event is sent only to the client application that places the character in Help mode.</span></span>

### <a name="see-also"></a><span data-ttu-id="51a0c-135">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="51a0c-135">See Also</span></span>

<span data-ttu-id="51a0c-136">[**Proprietà HelpModeOn**](helpmodeon-property.md), [ **proprietà HelpContextID**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="51a0c-136">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

