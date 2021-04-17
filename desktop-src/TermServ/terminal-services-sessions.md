---
title: Sessioni di Desktop remoto
description: Poiché ogni accesso a un client di Connessione Desktop remoto (RDC) riceve un ID sessione separato, l'esperienza utente è simile a quella di essere connessi contemporaneamente a più computer; ad esempio, un computer Office e un computer di casa.
ms.assetid: 09a990cd-7590-4d73-b1f5-8736f0b4f17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb99f9745e382bdff1099eabae9a8e8ef0b8333
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299958"
---
# <a name="remote-desktop-sessions"></a>Sessioni di Desktop remoto

Quando un utente accede a un computer abilitato per la Servizi Desktop remoto, viene avviata una sessione per l'utente. Ogni sessione è identificata da un ID di sessione univoco. Poiché ogni accesso a un client di Connessione Desktop remoto (RDC) riceve un ID sessione separato, l'esperienza utente è simile a quella di essere connessi contemporaneamente a più computer; ad esempio, un computer Office e un computer di casa.

Ogni sessione Desktop remoto è associata a una stazione finestra interattiva. L'unico nome della stazione di finestra supportato per una finestra interattiva è "WinSta0". Pertanto, ogni sessione è associata alla propria finestra "WinSta0". Sono disponibili tre desktop standard per ogni finestra di Windows: il desktop Winlogon, il desktop screen saver e il desktop interattivo.

L'utente associato alla stazione interattiva della finestra per una sessione è noto come *utente interattivo*. In un client Connessione Desktop remoto (RDC) possono essere presenti più utenti interattivi oltre all'utente interattivo nella console di Servizi Desktop remoto. Per recuperare l'identificatore della sessione attualmente collegata alla console, usare la funzione [**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid) .

Quando un utente si disconnette da un client Connessione Desktop remoto (RDC), la sessione che il client ha sul server di host sessione Desktop remoto (host sessione Desktop remoto) (in precedenza noto come Terminal Server) viene eliminata e le stazioni e i desktop della finestra associati alla sessione vengono rimossi. Tuttavia, poiché la sessione della console di Servizi Desktop remoto non viene mai eliminata, le stazioni della finestra associate alla sessione della console non vengono eliminate. Ciò influiscono sul comportamento delle applicazioni in un ambiente di Servizi Desktop remoto quando sono configurate per l'esecuzione nel contesto di sicurezza dell'utente interattivo, nota anche come modalità di attivazione degli oggetti "RunAs Interactive".

Per ulteriori informazioni sull'avvio di un processo del server locale in una sessione specificata, vedere [attivazione da sessione a sessione con un moniker di sessione](session-to-session-activation-with-a-session-moniker.md) e [utilizzo di un moniker di sessione](using-a-session-moniker.md). Per ulteriori informazioni sui contesti di sicurezza, vedere [il contesto di sicurezza del client](/windows/desktop/SecAuthZ/the-client-security-context).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessioni figlio](child-sessions.md)
</dt> </dl>

 

 