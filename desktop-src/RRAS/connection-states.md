---
title: Stati di connessione
description: Durante il processo di connessione a un server remoto, il Gestione connessioni di accesso remoto e il server RAS nel computer remoto eseguono diversi passaggi per stabilire la connessione.
ms.assetid: 7a8b0086-308b-47d2-888e-69ff473c6015
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9e52e1e4ea4a071f6606681aa2dc2fc15e88df659f8fd16746abf2d84727d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074221"
---
# <a name="connection-states"></a>Stati di connessione

Durante il processo di connessione a un server remoto, il Gestione connessioni di accesso remoto e il server RAS nel computer remoto eseguono diversi passaggi per stabilire la connessione. Ognuno di questi passaggi è identificato da uno stato di connessione. [**L'enumerazione RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) è un set di valori che corrispondono a questi stati di connessione. Gli stati di connessione possono essere suddivisi nei tre gruppi seguenti:

<dl> <dt>

<span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Stati di esecuzione
</dt> <dd>

Gli stati in esecuzione sono le parti dell'operazione di connessione che RAS gestisce automaticamente, ad esempio la connessione ai dispositivi necessari, l'autenticazione dell'utente e l'attesa di un callback dal server remoto. A meno che non si verifichi un errore, il client RAS non deve eseguire alcuna azione oltre a passare la notifica all'utente.

</dd> <dt>

<span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Stati sospesi
</dt> <dd>

Gli [stati sospesi si](paused-states.md) verificano quando il server remoto sospende l'operazione di connessione per ottenere input aggiuntivo dall'utente. Durante uno stato di sospensione, l'utente può digitare un numero di [callback,](callback-connections.md) un nome utente e una password diversi se l'autenticazione utente non riesce o una nuova password se quella precedente è scaduta.

</dd> <dt>

<span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Stati del terminale
</dt> <dd>

Gli stati del terminale si verificano quando la connessione è stata stabilita correttamente, l'operazione di connessione non è riuscita o la connessione è stata interrotta da [**una chiamata RasHangUp.**](/windows/desktop/api/Ras/nf-ras-rashangupa)

</dd> </dl>

Un client RAS può usare diversi meccanismi per determinare lo stato corrente di un'operazione di connessione. Quando un client RAS esegue la funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) in modo asincrono, il Gestione connessioni [](notification-handlers.md) di accesso remoto invia notifiche di stato al gestore delle notifiche del client ogni volta che cambia lo stato della connessione. Inoltre, il client può usare la [**funzione RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per ottenere lo stato corrente di qualsiasi operazione di connessione RAS.

 

 