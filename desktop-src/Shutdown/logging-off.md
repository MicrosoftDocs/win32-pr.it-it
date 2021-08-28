---
description: La funzione ExitWindows disconnette l'utente corrente. È anche possibile chiamare la funzione ExitWindowsEx con il flag EXW \_ LOGOFF.
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: Disconnessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2ab8525630673b897704cea675c5c2a1e6dc6b1df4dd875e8872a79f915204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664401"
---
# <a name="logging-off"></a>Disconnessione

La [**funzione ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) disconnette l'utente corrente. È anche possibile chiamare la [**funzione ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) con il flag EXW \_ LOGOFF.

Per impostazione predefinita, quando un'applicazione usa [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) o [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) per disconnettersi, il sistema invia il messaggio [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) a ogni finestra. Le applicazioni accettano di terminare restituisce **TRUE** quando ricevono questo messaggio. Se un'applicazione restituisce **FALSE** durante l'elaborazione di questo messaggio, l'operazione di disconnessione viene annullata. Se l'applicazione gestisce il messaggio **WM \_ QUERYENDSESSION,** è possibile consentire all'utente di annullare l'operazione di disconnessione, anche se un'altra applicazione o il sistema ha originato la richiesta di fine sessione. Per un esempio, vedere [Come disconnettere l'utente corrente.](how-to-log-off-the-current-user.md)

Quando un'applicazione restituisce **TRUE** per [**WM \_ QUERYENDSESSION,**](wm-queryendsession.md)riceve il messaggio [**\_ ENDSESSION WM**](wm-endsession.md) e viene terminata, indipendentemente dal modo in cui le altre applicazioni rispondono al messaggio **WM \_ QUERYENDSESSION.**

Per forzare la terminazione di tutte le applicazioni, [**usare ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)e specificare il flag EXW \_ FORCE. In questo modo si impedisce al sistema di [**inviare messaggi WM \_ QUERYENDSESSION.**](wm-queryendsession.md)

Il sistema invia anche il segnale di controllo CTRL \_ LOGOFF \_ EVENT a ogni processo durante un'operazione di disconnessione. Un'applicazione console può registrare [**un handlerRoutine**](/windows/console/handlerroutine) per elaborare questi messaggi.

Se il processo che ha chiamato [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) è in esecuzione nella sessione di accesso dell'utente interattivo, tutti i processi nella sessione di accesso vengono terminati. Se il processo che chiama **ExitWindowsEx** si trova in un'altra sessione di accesso, vengono effettuate solo le notifiche. nessun processo viene terminato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come disconnettere l'utente corrente](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
