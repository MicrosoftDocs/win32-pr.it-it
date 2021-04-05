---
description: Winlogon implementa due operazioni di timeout, una per le finestre di dialogo sicure e l'altra per l'attivazione e la terminazione screen saver.
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: Operazioni di Tempo di servizio della finestra di dialogo supportate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274950cadd45cd4e7e3be890da0e4350a4d0c5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751666"
---
# <a name="supported-dialog-box-service-time-out-operations"></a><span data-ttu-id="5e782-103">Operazioni di Tempo di servizio della finestra di dialogo supportate</span><span class="sxs-lookup"><span data-stu-id="5e782-103">Supported Dialog Box Service Time-out Operations</span></span>

<span data-ttu-id="5e782-104">[*Winlogon*](../secgloss/w-gly.md) implementa due operazioni di timeout, una per le finestre di dialogo sicure e l'altra per l'attivazione e la terminazione screen saver.</span><span class="sxs-lookup"><span data-stu-id="5e782-104">[*Winlogon*](../secgloss/w-gly.md) implements two time-out operations, one for secure dialog boxes and the other for screen saver activation and termination.</span></span>

<span data-ttu-id="5e782-105">Quando si visualizza una finestra di dialogo protetta, ad esempio l'accesso o lo sblocco di una workstation, Winlogon può eseguire il timeout delle finestre di dialogo e restituire un codice risultato appropriato alla routine della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5e782-105">While displaying a secure dialog box, such as logon or unlocking a workstation, Winlogon can time-out the dialog boxes and return an appropriate result code to the dialog box procedure.</span></span> <span data-ttu-id="5e782-106">Winlogon fornisce un set di funzioni di supporto della finestra di dialogo per [*Gina*](../secgloss/g-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5e782-106">Winlogon provides a set of dialog box support functions for the [*GINA*](../secgloss/g-gly.md).</span></span> <span data-ttu-id="5e782-107">GINA deve usare queste funzioni anziché le controparti di Windows per garantire che GINA e Winlogon mantengano il controllo appropriato per le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5e782-107">The GINA must use these functions instead of their Windows counterparts to ensure that the GINA and Winlogon maintain appropriate control over the dialog boxes.</span></span> <span data-ttu-id="5e782-108">L'impossibilità di usare le versioni di Winlogon di queste funzioni potrebbe consentire a utenti non autorizzati di accedere al sistema.</span><span class="sxs-lookup"><span data-stu-id="5e782-108">Failure to use the Winlogon versions of these functions could result in unauthorized users gaining access to the system.</span></span>

<span data-ttu-id="5e782-109">I servizi della finestra di dialogo Winlogon sono forniti dalle funzioni di supporto seguenti.</span><span class="sxs-lookup"><span data-stu-id="5e782-109">Winlogon dialog box services are provided by the following support functions.</span></span>



| <span data-ttu-id="5e782-110">Funzione di supporto</span><span class="sxs-lookup"><span data-stu-id="5e782-110">Support function</span></span>                                               | <span data-ttu-id="5e782-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e782-111">Description</span></span>                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e782-112">**WlxMessageBox**</span><span class="sxs-lookup"><span data-stu-id="5e782-112">**WlxMessageBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | <span data-ttu-id="5e782-113">Simile alla funzione [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) di Windows.</span><span class="sxs-lookup"><span data-stu-id="5e782-113">Similar to the Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) function.</span></span>                         |
| [<span data-ttu-id="5e782-114">**WlxDialogBox**</span><span class="sxs-lookup"><span data-stu-id="5e782-114">**WlxDialogBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | <span data-ttu-id="5e782-115">Simile alla funzione [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) di Windows.</span><span class="sxs-lookup"><span data-stu-id="5e782-115">Similar to the Windows [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function.</span></span>                           |
| [<span data-ttu-id="5e782-116">**WlxDialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="5e782-116">**WlxDialogBoxIndirect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | <span data-ttu-id="5e782-117">Simile alla funzione [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) di Windows.</span><span class="sxs-lookup"><span data-stu-id="5e782-117">Similar to the Windows [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) function.</span></span>           |
| [<span data-ttu-id="5e782-118">**WlxDialogBoxParam**</span><span class="sxs-lookup"><span data-stu-id="5e782-118">**WlxDialogBoxParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | <span data-ttu-id="5e782-119">Simile alla funzione [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) di Windows.</span><span class="sxs-lookup"><span data-stu-id="5e782-119">Similar to the Windows [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) function.</span></span>                 |
| [<span data-ttu-id="5e782-120">**WlxDialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="5e782-120">**WlxDialogBoxIndirectParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | <span data-ttu-id="5e782-121">Simile alla funzione [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) di Windows.</span><span class="sxs-lookup"><span data-stu-id="5e782-121">Similar to the Windows [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) function.</span></span> |



 

<span data-ttu-id="5e782-122">Le DLL GINA possono anche ricevere \_ messaggi di firma di accesso condiviso di WLX WM \_ da Winlogon.</span><span class="sxs-lookup"><span data-stu-id="5e782-122">GINA DLLs can also receive WLX\_WM\_SAS messages from Winlogon.</span></span> <span data-ttu-id="5e782-123">Questi messaggi vengono inviati alle finestre di dialogo attive se viene ricevuta una [*sequenza di attenzione sicura*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5e782-123">These messages are sent to active dialog boxes if an [*secure attention sequence*](../secgloss/s-gly.md) (SAS) is received.</span></span> <span data-ttu-id="5e782-124">Questa operazione è utile se GINA sta richiedendo il PIN corrispondente per una [*Smart Card*](../secgloss/s-gly.md)e la scheda viene rimossa dal [*lettore*](../secgloss/r-gly.md)di smart card.</span><span class="sxs-lookup"><span data-stu-id="5e782-124">This is useful if the GINA is in the process of prompting for the matching PIN for a [*smart card*](../secgloss/s-gly.md), and the card is removed from the smart card [*reader*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="5e782-125">Winlogon usa la firma di accesso condiviso \_ di WLX DLG \_ come codice risultato EndDialog quando si verifica un evento SAS durante un'operazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="5e782-125">Winlogon uses WLX\_DLG\_SAS as the EndDialog result code when an SAS event occurs during a dialog box operation.</span></span>

<span data-ttu-id="5e782-126">Anche i timeout vengono recapitati in questo modo.</span><span class="sxs-lookup"><span data-stu-id="5e782-126">Time-outs are also delivered in this manner.</span></span> <span data-ttu-id="5e782-127">Un messaggio di firma di accesso condiviso \_ di WLX WM \_ viene inviato con il timeout di tipo di firma di accesso condiviso del tipo \_ \_ \_ SCRNSVR \_ timeout o wlx \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="5e782-127">A WLX\_WM\_SAS message is sent with WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT or WLX\_SAS\_TYPE\_TIMEOUT.</span></span> <span data-ttu-id="5e782-128">La finestra di dialogo terminerà con un codice di uscita appropriato per consentire agli sviluppatori GINA di associare le notifiche di timeout.</span><span class="sxs-lookup"><span data-stu-id="5e782-128">The dialog box will end with an appropriate exit code to allow GINA developers to hook the time-out notifications.</span></span>

<span data-ttu-id="5e782-129">Le finestre di dialogo GINA possono essere terminate da Winlogon usando la \_ disconnessione utente del codice wlx DLG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5e782-129">GINA dialog boxes can be terminated by Winlogon by using the code WLX\_DLG\_USER\_LOGOFF.</span></span> <span data-ttu-id="5e782-130">Indica che l'utente si è disconnesso durante l'esecuzione della finestra di dialogo, ad esempio chiamando la funzione [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="5e782-130">This indicates that the user has logged off during the running of the dialog box (for example, by calling the [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) function from another thread).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e782-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5e782-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e782-132">Inizializzazione di Winlogon</span><span class="sxs-lookup"><span data-stu-id="5e782-132">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="5e782-133">Stati di Winlogon</span><span class="sxs-lookup"><span data-stu-id="5e782-133">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="5e782-134">Invio di messaggi a GINA</span><span class="sxs-lookup"><span data-stu-id="5e782-134">Sending Messages to the GINA</span></span>](sending-messages-to-the-gina.md)
</dt> <dt>

[<span data-ttu-id="5e782-135">Funzioni di supporto di Winlogon</span><span class="sxs-lookup"><span data-stu-id="5e782-135">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
