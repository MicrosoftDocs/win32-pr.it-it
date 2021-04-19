---
description: Winlogon invia messaggi a GINA mentre vengono visualizzate le finestre di dialogo. Questi messaggi sono tutti incapsulati nel messaggio di firma di accesso condiviso di WLX \_ WM \_ come indicato di seguito.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Invio di messaggi a GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2f7b5b0d8fbecafad0bcc36c84cf395813f767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311602"
---
# <a name="sending-messages-to-the-gina"></a><span data-ttu-id="d91ce-104">Invio di messaggi a GINA</span><span class="sxs-lookup"><span data-stu-id="d91ce-104">Sending Messages to the GINA</span></span>

<span data-ttu-id="d91ce-105">[*Winlogon*](../secgloss/w-gly.md) invia messaggi a [*Gina*](../secgloss/g-gly.md) mentre vengono visualizzate le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="d91ce-105">[*Winlogon*](../secgloss/w-gly.md) sends messages to the [*GINA*](../secgloss/g-gly.md) while dialog boxes are displayed.</span></span> <span data-ttu-id="d91ce-106">Questi messaggi sono tutti incapsulati nel messaggio di firma di accesso condiviso di WLX \_ WM \_ come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d91ce-106">These messages are all encapsulated in the WLX\_WM\_SAS message as follows.</span></span>



| <span data-ttu-id="d91ce-107">Tipo di sequenza di attenzione sicura nel parametro wParam</span><span class="sxs-lookup"><span data-stu-id="d91ce-107">Secure attention sequence type in wParam parameter</span></span> | <span data-ttu-id="d91ce-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d91ce-108">Description</span></span>                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d91ce-109">tipo di firma di accesso condiviso di WLX \_ \_ \_ CTRL \_ ALT \_ Canc</span><span class="sxs-lookup"><span data-stu-id="d91ce-109">WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL</span></span>                     | <span data-ttu-id="d91ce-110">Indica che è stata ricevuta una sequenza di tasti CTRL + ALT + CANC.</span><span class="sxs-lookup"><span data-stu-id="d91ce-110">Indicates that a CTRL+ALT+DEL key sequence was received.</span></span>                                                                                      |
| <span data-ttu-id="d91ce-111">tipo di firma di accesso condiviso di WLX \_ SAS \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="d91ce-111">WLX\_SAS\_TYPE\_SC\_INSERT</span></span>                         | <span data-ttu-id="d91ce-112">Indica che una [*Smart Card*](../secgloss/s-gly.md) è stata inserita in un dispositivo compatibile.</span><span class="sxs-lookup"><span data-stu-id="d91ce-112">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span> |
| <span data-ttu-id="d91ce-113">tipo di firma di accesso condiviso di WLX \_ \_ \_ SC \_ Remove</span><span class="sxs-lookup"><span data-stu-id="d91ce-113">WLX\_SAS\_TYPE\_SC\_REMOVE</span></span>                         | <span data-ttu-id="d91ce-114">Indica che una smart card è stata rimossa da un dispositivo compatibile.</span><span class="sxs-lookup"><span data-stu-id="d91ce-114">Indicates that a smart card has been removed from a compatible device.</span></span>                                                                        |
| <span data-ttu-id="d91ce-115">\_disconnessione \_ utente tipo di SAS \_ wlx \_</span><span class="sxs-lookup"><span data-stu-id="d91ce-115">WLX\_SAS\_TYPE\_USER\_LOGOFF</span></span>                       | <span data-ttu-id="d91ce-116">Indica che un utente ha richiesto la disconnessione.</span><span class="sxs-lookup"><span data-stu-id="d91ce-116">Indicates that a user requested logoff.</span></span>                                                                                                       |
| <span data-ttu-id="d91ce-117">\_ \_ \_ timeout SCRNSVR tipo SAS \_ di wlx</span><span class="sxs-lookup"><span data-stu-id="d91ce-117">WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT</span></span>                   | <span data-ttu-id="d91ce-118">Indica che la screen saver deve essere eseguita a causa della mancanza di input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d91ce-118">Indicates that the screen saver should be run due to lack of user input.</span></span>                                                                      |
| <span data-ttu-id="d91ce-119">\_ \_ timeout tipo di SAS di WLX \_</span><span class="sxs-lookup"><span data-stu-id="d91ce-119">WLX\_SAS\_TYPE\_TIMEOUT</span></span>                            | <span data-ttu-id="d91ce-120">Indica che non è stato ricevuto alcun input da parte dell'utente entro il periodo di timeout specificato.</span><span class="sxs-lookup"><span data-stu-id="d91ce-120">Indicates that no user input was received within the specified time-out period.</span></span>                                                               |



 

<span data-ttu-id="d91ce-121">Per i timeout e le disconnessioni, Winlogon chiude la finestra di dialogo dopo che il messaggio è stato inviato.</span><span class="sxs-lookup"><span data-stu-id="d91ce-121">For time-outs and logoffs, Winlogon will close the dialog box after the message has been sent.</span></span> <span data-ttu-id="d91ce-122">Questo messaggio viene inviato in modo che l'operazione della finestra di dialogo possa rispondere in modo utile, ad esempio chiudendosi se si è verificata una disconnessione.</span><span class="sxs-lookup"><span data-stu-id="d91ce-122">This message is sent so the dialog box operation can respond in a useful manner (for example, by closing itself down if a logoff has occurred).</span></span>

<span data-ttu-id="d91ce-123">Per i timeout di input, la finestra di dialogo viene chiusa con il timeout di input del codice WLX \_ DLG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d91ce-123">For input time-outs, the dialog box is closed with the code WLX\_DLG\_INPUT\_TIMEOUT.</span></span>

<span data-ttu-id="d91ce-124">Per screen saver i timeout, la finestra di dialogo viene chiusa con il timeout del codice WLX \_ DLG \_ Screen \_ saver \_ .</span><span class="sxs-lookup"><span data-stu-id="d91ce-124">For screen saver time-outs, the dialog box is closed with the code WLX\_DLG\_SCREEN\_SAVER\_TIMEOUT.</span></span>

<span data-ttu-id="d91ce-125">Per le disconnessioni, l'operazione della finestra di dialogo viene chiusa con \_ la \_ disconnessione utente del codice wlx DLG \_ .</span><span class="sxs-lookup"><span data-stu-id="d91ce-125">For logoffs, the dialog box operation is closed with the code WLX\_DLG\_USER\_LOGOFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d91ce-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d91ce-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d91ce-127">Inizializzazione di Winlogon</span><span class="sxs-lookup"><span data-stu-id="d91ce-127">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="d91ce-128">Stati di Winlogon</span><span class="sxs-lookup"><span data-stu-id="d91ce-128">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="d91ce-129">Operazioni di Tempo di servizio della finestra di dialogo supportate</span><span class="sxs-lookup"><span data-stu-id="d91ce-129">Supported Dialog Box Service Time-out Operations</span></span>](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[<span data-ttu-id="d91ce-130">Funzioni di supporto di Winlogon</span><span class="sxs-lookup"><span data-stu-id="d91ce-130">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
