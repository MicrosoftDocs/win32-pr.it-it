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
# <a name="supported-dialog-box-service-time-out-operations"></a>Operazioni di Tempo di servizio della finestra di dialogo supportate

[*Winlogon*](../secgloss/w-gly.md) implementa due operazioni di timeout, una per le finestre di dialogo sicure e l'altra per l'attivazione e la terminazione screen saver.

Quando si visualizza una finestra di dialogo protetta, ad esempio l'accesso o lo sblocco di una workstation, Winlogon può eseguire il timeout delle finestre di dialogo e restituire un codice risultato appropriato alla routine della finestra di dialogo. Winlogon fornisce un set di funzioni di supporto della finestra di dialogo per [*Gina*](../secgloss/g-gly.md). GINA deve usare queste funzioni anziché le controparti di Windows per garantire che GINA e Winlogon mantengano il controllo appropriato per le finestre di dialogo. L'impossibilità di usare le versioni di Winlogon di queste funzioni potrebbe consentire a utenti non autorizzati di accedere al sistema.

I servizi della finestra di dialogo Winlogon sono forniti dalle funzioni di supporto seguenti.



| Funzione di supporto                                               | Descrizione                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**WlxMessageBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | Simile alla funzione [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) di Windows.                         |
| [**WlxDialogBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | Simile alla funzione [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) di Windows.                           |
| [**WlxDialogBoxIndirect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | Simile alla funzione [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) di Windows.           |
| [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | Simile alla funzione [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) di Windows.                 |
| [**WlxDialogBoxIndirectParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | Simile alla funzione [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) di Windows. |



 

Le DLL GINA possono anche ricevere \_ messaggi di firma di accesso condiviso di WLX WM \_ da Winlogon. Questi messaggi vengono inviati alle finestre di dialogo attive se viene ricevuta una [*sequenza di attenzione sicura*](../secgloss/s-gly.md) . Questa operazione è utile se GINA sta richiedendo il PIN corrispondente per una [*Smart Card*](../secgloss/s-gly.md)e la scheda viene rimossa dal [*lettore*](../secgloss/r-gly.md)di smart card. Winlogon usa la firma di accesso condiviso \_ di WLX DLG \_ come codice risultato EndDialog quando si verifica un evento SAS durante un'operazione della finestra di dialogo.

Anche i timeout vengono recapitati in questo modo. Un messaggio di firma di accesso condiviso \_ di WLX WM \_ viene inviato con il timeout di tipo di firma di accesso condiviso del tipo \_ \_ \_ SCRNSVR \_ timeout o wlx \_ \_ \_ La finestra di dialogo terminerà con un codice di uscita appropriato per consentire agli sviluppatori GINA di associare le notifiche di timeout.

Le finestre di dialogo GINA possono essere terminate da Winlogon usando la \_ disconnessione utente del codice wlx DLG \_ \_ . Indica che l'utente si è disconnesso durante l'esecuzione della finestra di dialogo, ad esempio chiamando la funzione [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) da un altro thread.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Inizializzazione di Winlogon](initializing-winlogon.md)
</dt> <dt>

[Stati di Winlogon](winlogon-states.md)
</dt> <dt>

[Invio di messaggi a GINA](sending-messages-to-the-gina.md)
</dt> <dt>

[Funzioni di supporto di Winlogon](authentication-functions.md)
</dt> </dl>

 

 
