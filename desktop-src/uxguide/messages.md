---
title: Messaggi (nozioni di base sulla progettazione)
description: I messaggi sono di qualsiasi tipo necessario per gli utenti di messaggi o desiderano vedere quando usano l'app. Informazioni su come presentare gli errori, gli avvisi, le conferme e le notifiche nell'app.
ms.assetid: 700F1F1F-B41D-4C0A-B2EC-91C84E46E526
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dba3296c9824b2153184c45b6a021ea823b4d151
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320353"
---
# <a name="messages-design-basics"></a><span data-ttu-id="316ca-104">Messaggi (nozioni di base sulla progettazione)</span><span class="sxs-lookup"><span data-stu-id="316ca-104">Messages (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="316ca-105">Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="316ca-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="316ca-106">Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="316ca-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="316ca-107">I messaggi sono di qualsiasi tipo necessario per gli utenti di messaggi o desiderano vedere quando usano l'app.</span><span class="sxs-lookup"><span data-stu-id="316ca-107">Messages are any kind of message users need or want to see as they use your app.</span></span> <span data-ttu-id="316ca-108">Informazioni su come presentare gli errori, gli avvisi, le conferme e le notifiche nell'app.</span><span class="sxs-lookup"><span data-stu-id="316ca-108">Learn how to present errors, warning, confirmations, and notifications in your app.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="316ca-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="316ca-109">In this section</span></span>



| <span data-ttu-id="316ca-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="316ca-110">Topic</span></span>                                        | <span data-ttu-id="316ca-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="316ca-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="316ca-112">Messaggi di errore</span><span class="sxs-lookup"><span data-stu-id="316ca-112">Error Messages</span></span>](mess-error.md)<br/>  | <span data-ttu-id="316ca-113">Un messaggio di errore avvisa gli utenti di un problema che si è già verificato.</span><span class="sxs-lookup"><span data-stu-id="316ca-113">An error message alerts users of a problem that has already occurred.</span></span> <span data-ttu-id="316ca-114">Al contrario, un messaggio di avviso avvisa gli utenti di una condizione che potrebbe causare un problema in futuro.</span><span class="sxs-lookup"><span data-stu-id="316ca-114">By contrast, a warning message alerts users of a condition that might cause a problem in the future.</span></span> <span data-ttu-id="316ca-115">I messaggi di errore possono essere presentati usando le finestre di dialogo modali, i messaggi sul posto, le notifiche o le mongolfiere.</span><span class="sxs-lookup"><span data-stu-id="316ca-115">Error messages can be presented using modal dialog boxes, in-place messages, notifications, or balloons.</span></span><br/>                                                  |
| [<span data-ttu-id="316ca-116">Messaggi di avviso</span><span class="sxs-lookup"><span data-stu-id="316ca-116">Warning Messages</span></span>](mess-warn.md)<br/> | <span data-ttu-id="316ca-117">Un messaggio di avviso è una finestra di dialogo modale, un messaggio sul posto, una notifica o un fumetto che avvisa l'utente di una condizione che potrebbe causare un problema in futuro.</span><span class="sxs-lookup"><span data-stu-id="316ca-117">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="316ca-118">Conferme</span><span class="sxs-lookup"><span data-stu-id="316ca-118">Confirmations</span></span>](mess-confirm.md)<br/> | <span data-ttu-id="316ca-119">Una conferma è una finestra di dialogo modale che chiede se l'utente desidera procedere con un'azione.</span><span class="sxs-lookup"><span data-stu-id="316ca-119">A confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span><br/>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="316ca-120">Notifications</span><span class="sxs-lookup"><span data-stu-id="316ca-120">Notifications</span></span>](mess-notif.md)<br/>   | <span data-ttu-id="316ca-121">Una notifica informa gli utenti degli eventi che non sono correlati all'attività dell'utente corrente, visualizzando brevemente un fumetto da un'icona nell'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="316ca-121">A notification informs users of events that are unrelated to the current user activity, by briefly displaying a balloon from an icon in the notification area.</span></span> <span data-ttu-id="316ca-122">La notifica potrebbe essere dovuta a un'azione dell'utente o a un evento di sistema significativo oppure potrebbe offrire informazioni potenzialmente utili da Microsoft Windows o da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="316ca-122">The notification could result from a user action or significant system event, or could offer potentially useful information from Microsoft Windows or an application.</span></span><br/> |



 

 

