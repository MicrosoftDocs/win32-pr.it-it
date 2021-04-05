---
description: La funzione ExitWindows disconnette l'utente corrente. È anche possibile chiamare la funzione ExitWindowsEx con il \_ flag di disconnessione EXW.
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: Disconnessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0571c0522c494acd763d57dcae8d200125cd53d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885844"
---
# <a name="logging-off"></a><span data-ttu-id="7c6ae-104">Disconnessione</span><span class="sxs-lookup"><span data-stu-id="7c6ae-104">Logging Off</span></span>

<span data-ttu-id="7c6ae-105">La funzione [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) disconnette l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="7c6ae-105">The [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function logs off the current user.</span></span> <span data-ttu-id="7c6ae-106">È anche possibile chiamare la funzione [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) con il \_ flag di disconnessione EXW.</span><span class="sxs-lookup"><span data-stu-id="7c6ae-106">You can also call the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function with the EXW\_LOGOFF flag.</span></span>

<span data-ttu-id="7c6ae-107">Per impostazione predefinita, quando un'applicazione utilizza [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) o [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) per disconnettersi, il sistema invia il messaggio [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) a ogni finestra.</span><span class="sxs-lookup"><span data-stu-id="7c6ae-107">By default, when an application uses [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) or [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) to log off, the system sends the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message to each window.</span></span> <span data-ttu-id="7c6ae-108">Le applicazioni accettano di terminare restituendo **true** quando ricevono questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="7c6ae-108">Applications agree to terminate by returning **TRUE** when they receive this message.</span></span> <span data-ttu-id="7c6ae-109">Se un'applicazione restituisce **false** durante l'elaborazione del messaggio, l'operazione di disconnessione viene annullata.</span><span class="sxs-lookup"><span data-stu-id="7c6ae-109">If any application returns **FALSE** when processing this message, the log-off operation is canceled.</span></span> <span data-ttu-id="7c6ae-110">Se l'applicazione gestisce il messaggio **WM \_ QUERYENDSESSION** , è possibile consentire all'utente di annullare l'operazione di disconnessione, anche se un'altra applicazione o il sistema ha originato la richiesta di sessione finale.</span><span class="sxs-lookup"><span data-stu-id="7c6ae-110">If your application handles the **WM\_QUERYENDSESSION** message, you can allow the user to cancel the log-off operation, even if another application or the system originated the end-session request.</span></span> <span data-ttu-id="7c6ae-111">Per un esempio, vedere [come disconnettere l'utente corrente](how-to-log-off-the-current-user.md).</span><span class="sxs-lookup"><span data-stu-id="7c6ae-111">For an example, see [How to Log Off the Current User](how-to-log-off-the-current-user.md).</span></span>

<span data-ttu-id="7c6ae-112">Quando un'applicazione restituisce **true** per [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), riceve il messaggio [**WM \_ ENDSESSION**](wm-endsession.md) ed è terminato, indipendentemente dal modo in cui le altre applicazioni rispondono al messaggio **WM \_ QUERYENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="7c6ae-112">When an application returns **TRUE** for [**WM\_QUERYENDSESSION**](wm-queryendsession.md), it receives the [**WM\_ENDSESSION**](wm-endsession.md) message and it is terminated, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="7c6ae-113">Per forzare l'interruzione di tutte le applicazioni, usare [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)e specificare il \_ flag di forza EXW.</span><span class="sxs-lookup"><span data-stu-id="7c6ae-113">To force all applications to terminate, use [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex), and specify the EXW\_FORCE flag.</span></span> <span data-ttu-id="7c6ae-114">Ciò impedisce al sistema di inviare messaggi [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) .</span><span class="sxs-lookup"><span data-stu-id="7c6ae-114">This prevents the system from sending [**WM\_QUERYENDSESSION**](wm-queryendsession.md) messages.</span></span>

<span data-ttu-id="7c6ae-115">Il sistema invia anche il \_ \_ segnale di controllo degli eventi di disconnessione CTRL a ogni processo durante un'operazione di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="7c6ae-115">The system also sends the CTRL\_LOGOFF\_EVENT control signal to every process during a log-off operation.</span></span> <span data-ttu-id="7c6ae-116">Un'applicazione console può registrare un [**HandlerRoutine**](/windows/console/handlerroutine) per elaborare questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="7c6ae-116">A console application can register a [**HandlerRoutine**](/windows/console/handlerroutine) to process these messages.</span></span>

<span data-ttu-id="7c6ae-117">Se il processo che ha chiamato [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) è in esecuzione nella sessione di accesso dell'utente interattivo, tutti i processi nella sessione di accesso vengono interrotti.</span><span class="sxs-lookup"><span data-stu-id="7c6ae-117">If the process that called [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) is running in the logon session of the interactive user, all processes in the logon session are terminated.</span></span> <span data-ttu-id="7c6ae-118">Se il processo che chiama **ExitWindowsEx** è in un'altra sessione di accesso, verranno effettuate solo le notifiche. nessun processo viene terminato.</span><span class="sxs-lookup"><span data-stu-id="7c6ae-118">If the process calling **ExitWindowsEx** is in some other logon session, only the notifications are made; no processes are terminated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c6ae-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c6ae-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c6ae-120">Come disconnettere l'utente corrente</span><span class="sxs-lookup"><span data-stu-id="7c6ae-120">How to Log Off the Current User</span></span>](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
