---
title: Evento ActiveClientChange
description: Evento ActiveClientChange
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221425"
---
# <a name="activeclientchange-event"></a><span data-ttu-id="acf1f-103">Evento ActiveClientChange</span><span class="sxs-lookup"><span data-stu-id="acf1f-103">ActiveClientChange Event</span></span>

<span data-ttu-id="acf1f-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="acf1f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="acf1f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="acf1f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="acf1f-106">Si verifica quando viene modificato il client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="acf1f-106">Occurs when the active client of the character changes.</span></span>

</dd> <dt>

<span data-ttu-id="acf1f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="acf1f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="acf1f-108">Agente **secondario** *.* ActiveClientChange (ByVal *CharacterID*, ByVal *Active* **)**</span><span class="sxs-lookup"><span data-stu-id="acf1f-108">**Sub** *agent.* ActiveClientChange (ByVal *CharacterID*, ByVal *Active* **)**</span></span>



| <span data-ttu-id="acf1f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="acf1f-109">Part</span></span>          | <span data-ttu-id="acf1f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acf1f-110">Description</span></span>                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acf1f-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="acf1f-111">*CharacterID*</span></span> | <span data-ttu-id="acf1f-112">Restituisce l'ID del carattere per il quale si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="acf1f-112">Returns the ID of the character for which the event occurred.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="acf1f-113">*Attivo*</span><span class="sxs-lookup"><span data-stu-id="acf1f-113">*Active*</span></span>      | <span data-ttu-id="acf1f-114">Valore booleano che indica se il client diventa attivo o meno.</span><span class="sxs-lookup"><span data-stu-id="acf1f-114">A Boolean value that indicates whether the client became active or not active.</span></span> <span data-ttu-id="acf1f-115">Valore **true** L'applicazione client è diventata il client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="acf1f-115">**True** The client application became the active client of the character.</span></span> <br/> <span data-ttu-id="acf1f-116">**False** L'applicazione client non è più il client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="acf1f-116">**False** The client application is no longer the active client of the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="acf1f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="acf1f-117">Remarks</span></span>

<span data-ttu-id="acf1f-118">Quando più applicazioni client condividono lo stesso carattere, il client attivo del carattere riceve l'input del mouse (ad esempio, gli eventi di clic o di trascinamento del controllo agente Microsoft).</span><span class="sxs-lookup"><span data-stu-id="acf1f-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="acf1f-119">Analogamente, quando vengono visualizzati più caratteri, il client attivo del carattere superiore (noto anche come client attivo di input) riceve gli eventi di [comando](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="acf1f-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [Command](command-event.md) events.</span></span>

<span data-ttu-id="acf1f-120">Quando viene modificato il client attivo di un carattere, questo evento restituisce l'ID di tale carattere e **true** se l'applicazione è diventata il client attivo del carattere o **false** se non è più il client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="acf1f-120">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="acf1f-121">Un'applicazione client può ricevere questo evento quando l'utente seleziona la voce di un'applicazione client nel menu popup del carattere o tramite il comando vocale, quando l'applicazione client modifica il proprio stato attivo o quando un'altra applicazione client chiude la connessione a Agent.</span><span class="sxs-lookup"><span data-stu-id="acf1f-121">A client application may receive this event when the user selects a client application's entry in character's pop-up menu or by voice command, when the client application changes its active status, or when another client application quits its connection to Agent.</span></span> <span data-ttu-id="acf1f-122">Agent invia questo evento solo alle applicazioni client direttamente interessate; che diventeranno il client attivo o smetteranno di essere il client attivo.</span><span class="sxs-lookup"><span data-stu-id="acf1f-122">Agent sends this event only to the client applications that are directly affected; that either become the active client or stop being the active client.</span></span>

### <a name="see-also"></a><span data-ttu-id="acf1f-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="acf1f-123">See Also</span></span>

<span data-ttu-id="acf1f-124">[\* \* \* \* ActivateInput \* \* evento \* \*](activateinput-event.md), [\* \* \* \* attivo \* \* proprietà \* \*](active-property.md), [\* \* \* \* DeactivateInput \* \* evento \* \*](deactivateinput-event.md), [\* \* \* \* Attiva \* \* metodo \* \*](activate-method.md)</span><span class="sxs-lookup"><span data-stu-id="acf1f-124">[\*\*\*\*ActivateInput\*\* event\*\*](activateinput-event.md), [\*\*\*\*Active\*\* property\*\*](active-property.md), [\*\*\*\*DeactivateInput\*\* event\*\*](deactivateinput-event.md), [\*\*\*\*Activate\*\* method\*\*](activate-method.md)</span></span>


 

 





