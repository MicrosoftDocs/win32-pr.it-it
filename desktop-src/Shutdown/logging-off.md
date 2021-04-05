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
# <a name="logging-off"></a>Disconnessione

La funzione [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) disconnette l'utente corrente. È anche possibile chiamare la funzione [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) con il \_ flag di disconnessione EXW.

Per impostazione predefinita, quando un'applicazione utilizza [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) o [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) per disconnettersi, il sistema invia il messaggio [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) a ogni finestra. Le applicazioni accettano di terminare restituendo **true** quando ricevono questo messaggio. Se un'applicazione restituisce **false** durante l'elaborazione del messaggio, l'operazione di disconnessione viene annullata. Se l'applicazione gestisce il messaggio **WM \_ QUERYENDSESSION** , è possibile consentire all'utente di annullare l'operazione di disconnessione, anche se un'altra applicazione o il sistema ha originato la richiesta di sessione finale. Per un esempio, vedere [come disconnettere l'utente corrente](how-to-log-off-the-current-user.md).

Quando un'applicazione restituisce **true** per [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), riceve il messaggio [**WM \_ ENDSESSION**](wm-endsession.md) ed è terminato, indipendentemente dal modo in cui le altre applicazioni rispondono al messaggio **WM \_ QUERYENDSESSION** .

Per forzare l'interruzione di tutte le applicazioni, usare [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)e specificare il \_ flag di forza EXW. Ciò impedisce al sistema di inviare messaggi [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) .

Il sistema invia anche il \_ \_ segnale di controllo degli eventi di disconnessione CTRL a ogni processo durante un'operazione di disconnessione. Un'applicazione console può registrare un [**HandlerRoutine**](/windows/console/handlerroutine) per elaborare questi messaggi.

Se il processo che ha chiamato [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) è in esecuzione nella sessione di accesso dell'utente interattivo, tutti i processi nella sessione di accesso vengono interrotti. Se il processo che chiama **ExitWindowsEx** è in un'altra sessione di accesso, verranno effettuate solo le notifiche. nessun processo viene terminato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come disconnettere l'utente corrente](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
