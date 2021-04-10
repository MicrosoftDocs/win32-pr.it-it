---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3b7dbbdf272844242943d49ed86b303d220185
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046616"
---
# <a name="iagentnotifysinkexhelpcomplete"></a><span data-ttu-id="8ca5c-103">IAgentNotifySinkEx::HelpComplete</span><span class="sxs-lookup"><span data-stu-id="8ca5c-103">IAgentNotifySinkEx::HelpComplete</span></span>

<span data-ttu-id="8ca5c-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8ca5c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

<span data-ttu-id="8ca5c-105">Notifica a un'applicazione client quando l'utente seleziona un comando o un carattere per completare la modalità della guida.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-105">Notifies a client application when the user selects a command or character to complete Help mode.</span></span>

-   <span data-ttu-id="8ca5c-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="8ca5c-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="8ca5c-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="8ca5c-108">Identificatore del carattere per il quale è stata completata la modalità della guida.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-108">Identifier of the character for which Help mode completed.</span></span>

</dd> <dt>

<span data-ttu-id="8ca5c-109"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span><span class="sxs-lookup"><span data-stu-id="8ca5c-109"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="8ca5c-110">Identificatore del comando selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-110">Identifier of the command the user selected.</span></span>

</dd> <dt>

<span data-ttu-id="8ca5c-111"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="8ca5c-111"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="8ca5c-112">La motivo dell'evento, che può corrispondere ai valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ca5c-112">The cause for the event, which may be the following values:</span></span>



| <span data-ttu-id="8ca5c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="8ca5c-113">Value</span></span>                                                                         | <span data-ttu-id="8ca5c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ca5c-114">Description</span></span>                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca5c-115">comando CSHELPCAUSE **short senza segno const** **\_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="8ca5c-115">**const unsigned short** **CSHELPCAUSE\_COMMAND = 1;**</span></span><br/>             | <span data-ttu-id="8ca5c-116">L'utente ha selezionato un comando fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-116">The user selected a command supplied by your application.</span></span>                            |
| <span data-ttu-id="8ca5c-117">**const unsigned short** **CSHELPCAUSE \_ OTHERPROGRAM = 2;**</span><span class="sxs-lookup"><span data-stu-id="8ca5c-117">**const unsigned short** **CSHELPCAUSE\_OTHERPROGRAM = 2;**</span></span><br/>        | <span data-ttu-id="8ca5c-118">L'utente ha selezionato l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) di un altro client.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-118">The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span> |
| <span data-ttu-id="8ca5c-119">**const unsigned short** **CSHELPCAUSE \_ OPENCOMMANDSWINDOW = 3;**</span><span class="sxs-lookup"><span data-stu-id="8ca5c-119">**const unsigned short** **CSHELPCAUSE\_OPENCOMMANDSWINDOW = 3;**</span></span><br/>  | <span data-ttu-id="8ca5c-120">L'utente ha selezionato il comando Open Voice Commands.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-120">The user selected the Open Voice Commands command.</span></span>                                   |
| <span data-ttu-id="8ca5c-121">**const unsigned short** **CSHELPCAUSE \_ CLOSECOMMANDSWINDOW = 4;**</span><span class="sxs-lookup"><span data-stu-id="8ca5c-121">**const unsigned short** **CSHELPCAUSE\_CLOSECOMMANDSWINDOW = 4;**</span></span><br/> | <span data-ttu-id="8ca5c-122">L'utente ha selezionato il comando Chiudi voce comandi.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-122">The user selected the Close Voice Commands command.</span></span>                                  |
| <span data-ttu-id="8ca5c-123">**const unsigned short** **CSHELPCAUSE \_ SHOWCHARACTER = 5;**</span><span class="sxs-lookup"><span data-stu-id="8ca5c-123">**const unsigned short** **CSHELPCAUSE\_SHOWCHARACTER = 5;**</span></span><br/>       | <span data-ttu-id="8ca5c-124">L'utente ha selezionato il comando Mostra *caratteriname* .</span><span class="sxs-lookup"><span data-stu-id="8ca5c-124">The user selected the Show *CharacterName* command.</span></span>                                  |
| <span data-ttu-id="8ca5c-125">**const unsigned short** **CSHELPCAUSE \_ HIDECHARACTER = 6;**</span><span class="sxs-lookup"><span data-stu-id="8ca5c-125">**const unsigned short** **CSHELPCAUSE\_HIDECHARACTER = 6;**</span></span><br/>       | <span data-ttu-id="8ca5c-126">L'utente ha selezionato il comando Nascondi *caratterename* .</span><span class="sxs-lookup"><span data-stu-id="8ca5c-126">The user selected the Hide *CharacterName* command.</span></span>                                  |
| <span data-ttu-id="8ca5c-127">carattere CSHELPCAUSE **short const senza segno** **\_ = 7;**</span><span class="sxs-lookup"><span data-stu-id="8ca5c-127">**const unsigned short** **CSHELPCAUSE\_CHARACTER = 7;**</span></span><br/>           | <span data-ttu-id="8ca5c-128">L'utente ha selezionato (selezionato) il carattere.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-128">The user selected (clicked) the character.</span></span>                                           |



 

</dd> </dl>

<span data-ttu-id="8ca5c-129">In genere, la modalità Guida viene completata quando l'utente fa clic o trascina il carattere o seleziona un comando dal menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-129">Typically Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="8ca5c-130">Se si fa clic su un altro carattere o altrove sullo schermo, la modalità della guida non viene annullata.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-130">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="8ca5c-131">Il client che imposta la modalità della Guida per il carattere può annullare la modalità della Guida impostando [**IAgentCharacter:: HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) su **false**.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-131">The client that set Help mode for the character can cancel Help mode by setting [**IAgentCharacter::HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) to **False**.</span></span> <span data-ttu-id="8ca5c-132">Questa operazione non attiva l'evento **IAgentNotifySinkEx:: HelpComplete** .</span><span class="sxs-lookup"><span data-stu-id="8ca5c-132">(This does not trigger the **IAgentNotifySinkEx::HelpComplete** event.)</span></span>

<span data-ttu-id="8ca5c-133">Quando l'utente seleziona un comando dal menu popup del carattere in modalità guida, il server rimuove il menu, chiama la guida con il [**HelpContextID**](helpcontextid-property.md)specificato del comando e invia questo evento.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-133">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="8ca5c-134">L'oggetto sensibile al contesto (noto anche come?) La finestra della guida viene visualizzata nella posizione del puntatore.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-134">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="8ca5c-135">Se l'utente seleziona il comando in base all'input vocale, la finestra della guida viene visualizzata sopra il carattere.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-135">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="8ca5c-136">Se il carattere è esterno allo schermo, la finestra viene visualizzata sullo schermo più vicino alla posizione corrente del carattere.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-136">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="8ca5c-137">Se il server restituisce *dwCommandID* come stringa vuota (""), significa che l'utente ha selezionato un comando fornito dal server.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-137">If the server returns *dwCommandID* as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="8ca5c-138">Questo evento viene inviato solo all'applicazione client che inserisce il carattere in modalità guida.</span><span class="sxs-lookup"><span data-stu-id="8ca5c-138">This event is sent only to the client application that places the character into Help mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ca5c-139">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8ca5c-139">See Also</span></span>

<span data-ttu-id="8ca5c-140">[**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx:: SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span><span class="sxs-lookup"><span data-stu-id="8ca5c-140">[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>


 

