---
title: Evento ActivateInput
description: Evento ActivateInput
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0b4fdf83256d58dd247dee85b639f5499f013e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045233"
---
# <a name="activateinput-event"></a><span data-ttu-id="53965-103">Evento ActivateInput</span><span class="sxs-lookup"><span data-stu-id="53965-103">ActivateInput Event</span></span>

<span data-ttu-id="53965-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53965-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="53965-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="53965-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="53965-106">Si verifica quando un client diventa attivo come input.</span><span class="sxs-lookup"><span data-stu-id="53965-106">Occurs when a client becomes input-active.</span></span>

</dd> <dt>

<span data-ttu-id="53965-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="53965-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="53965-108">**Sub** *Agent* \_ ActivateInput **(ByVal** *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="53965-108">**Sub** *agent*\_ActivateInput **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="53965-109">Parte</span><span class="sxs-lookup"><span data-stu-id="53965-109">Part</span></span>          | <span data-ttu-id="53965-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53965-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="53965-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="53965-111">*CharacterID*</span></span> | <span data-ttu-id="53965-112">Restituisce l'ID del carattere tramite il quale il client diventa attivo come input.</span><span class="sxs-lookup"><span data-stu-id="53965-112">Returns the ID of the character through which the client becomes input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="53965-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="53965-113">Remarks</span></span>

<span data-ttu-id="53965-114">Il client attivo per l'input riceve gli eventi di input del mouse e vocale forniti dal server.</span><span class="sxs-lookup"><span data-stu-id="53965-114">The input-active client receives mouse and speech input events supplied by the server.</span></span> <span data-ttu-id="53965-115">Il server invia questo evento solo al client che diventa attivo come input.</span><span class="sxs-lookup"><span data-stu-id="53965-115">The server sends this event only to the client that becomes input-active.</span></span>

<span data-ttu-id="53965-116">Questo evento può verificarsi quando l'utente passa all'oggetto [Command](the-command-object.md) , ad esempio scegliendo la voce oggetto comando nella finestra comandi o nel menu a comparsa per un carattere.</span><span class="sxs-lookup"><span data-stu-id="53965-116">This event can occur when the user switches to your [Command](the-command-object.md) object, for example, by choosing your Command object entry in the Commands Window or in the pop-up menu for a character.</span></span> <span data-ttu-id="53965-117">Può inoltre verificarsi quando l'utente seleziona un carattere, facendo clic o pronunciando il relativo nome, quando un carattere diventa visibile e quando il carattere di un'altra applicazione client diventa nascosto.</span><span class="sxs-lookup"><span data-stu-id="53965-117">It can also occur when the user selects a character (by clicking or speaking its name), when a character becomes visible, and when the character of another client application becomes hidden.</span></span> <span data-ttu-id="53965-118">È anche possibile chiamare il [metodo Activate](activate-method.md) (con **stato** impostato su 2) per rendere esplicitamente il carattere in primo piano, il che comporta che l'applicazione client diventi input-Active e attiva questo evento.</span><span class="sxs-lookup"><span data-stu-id="53965-118">You can also call the [Activate Method](activate-method.md) (with **State** set to 2) to explicitly make the character topmost, which results in your client application becoming input-active and triggers this event.</span></span> <span data-ttu-id="53965-119">Tuttavia, questo evento non si verifica se si usa il metodo Activate solo per specificare se il client è il client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="53965-119">However, this event does not occur if you use the Activate Method method only to specify whether your client is the active client of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="53965-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="53965-120">See Also</span></span>

<span data-ttu-id="53965-121">[Evento **DeactivateInput**](deactivateinput-event.md), [metodo **Activate**](activate-method.md)</span><span class="sxs-lookup"><span data-stu-id="53965-121">[**DeactivateInput** event](deactivateinput-event.md), [**Activate** method](activate-method.md)</span></span>


 

 




