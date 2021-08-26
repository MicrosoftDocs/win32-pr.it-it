---
title: Desktop remoto sessioni
description: Poiché ogni accesso a un client di Connessione Desktop remoto (RDC) riceve un ID sessione separato, l'esperienza utente è simile all'accesso a più computer contemporaneamente; ad esempio un computer dell'ufficio e un computer domestico.
ms.assetid: 09a990cd-7590-4d73-b1f5-8736f0b4f17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5093e9da70301fc4258ce2df88527c87940e455050a0673ac36d2fb04a8cd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987161"
---
# <a name="remote-desktop-sessions"></a>Desktop remoto sessioni

Quando un utente accede a un computer Servizi Desktop remoto abilitato, viene avviata una sessione per l'utente. Ogni sessione è identificata da un ID sessione univoco. Poiché ogni accesso a un client di Connessione Desktop remoto (RDC) riceve un ID sessione separato, l'esperienza utente è simile all'accesso a più computer contemporaneamente; ad esempio un computer dell'ufficio e un computer domestico.

Ogni sessione desktop remoto è associata a una stazione finestra interattiva. L'unico nome di stazione finestra supportato per una stazione finestra interattiva è "WinSta0"; pertanto ogni sessione è associata alla propria stazione finestra "WinSta0". Sono disponibili tre desktop standard per ogni stazione di finestre: il desktop Winlogon, il desktop screen saver e il desktop interattivo.

L'utente associato alla stazione finestra interattiva per una sessione è noto come *utente interattivo.* In un client Connessione Desktop remoto (RDC) possono essere presenti più utenti interattivi oltre all'utente interattivo nella console Servizi Desktop remoto. Per recuperare l'identificatore della sessione attualmente collegata alla console, usare la [**funzione WTSGetActiveConsoleSessionId.**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)

Quando un utente si disconnette da un client Connessione Desktop remoto (RDC), la sessione del client sul server Host sessione Desktop remoto (in precedenza noto come server terminal) viene eliminata e le stazioni finestra e i desktop associati a tale sessione vengono rimossi. Tuttavia, poiché la Servizi Desktop remoto della console non viene mai eliminata, le stazioni finestra associate alla sessione della console non vengono eliminate. Ciò influisce sul comportamento delle applicazioni in un ambiente Servizi Desktop remoto quando sono configurate per l'esecuzione nel contesto di sicurezza dell'utente interattivo, noto anche come modalità di attivazione dell'oggetto "RunAs Interactive User".

Per altre informazioni sull'avvio di un processo del server locale in una sessione specificata, vedere Attivazione da sessione a sessione con un [moniker](session-to-session-activation-with-a-session-moniker.md) di sessione e Uso di [un moniker di sessione.](using-a-session-moniker.md) Per altre informazioni sui contesti di sicurezza, vedere [Contesto di sicurezza del client.](/windows/desktop/SecAuthZ/the-client-security-context)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessioni figlio](child-sessions.md)
</dt> </dl>

 

 