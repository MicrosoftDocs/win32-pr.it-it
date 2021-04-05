---
title: Stati di connessione
description: Durante il processo di connessione a un server remoto, la gestione connessione di accesso remoto e il server RAS sul computer remoto eseguono diversi passaggi per stabilire la connessione.
ms.assetid: 7a8b0086-308b-47d2-888e-69ff473c6015
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4488cc020a8a1b2a7da93384a4a5be1edb5182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872742"
---
# <a name="connection-states"></a>Stati di connessione

Durante il processo di connessione a un server remoto, la gestione connessione di accesso remoto e il server RAS sul computer remoto eseguono diversi passaggi per stabilire la connessione. Ognuno di questi passaggi è identificato da uno stato di connessione. L'enumerazione [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) è un set di valori che corrispondono a questi stati di connessione. Gli Stati di connessione possono essere divisi nei tre gruppi seguenti:

<dl> <dt>

<span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Stati in esecuzione
</dt> <dd>

Gli stati in esecuzione sono le parti dell'operazione di connessione gestite automaticamente da RAS, ad esempio la connessione ai dispositivi necessari, l'autenticazione dell'utente e l'attesa di un callback dal server remoto. A meno che non si verifichi un errore, il client RAS non deve intraprendere alcuna azione diversa da per passare la notifica all'utente.

</dd> <dt>

<span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Stati sospesi
</dt> <dd>

Gli [stati sospesi](paused-states.md) si verificano quando il server remoto sospende l'operazione di connessione per ottenere input aggiuntivi dall'utente. Durante uno stato di sospensione, l'utente può digitare un numero di [callback](callback-connections.md) , un nome utente e una password diversi in caso di errore dell'autenticazione utente o una nuova password se quella precedente è scaduta.

</dd> <dt>

<span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Stati terminali
</dt> <dd>

Gli stati terminali si verificano quando la connessione è stata stabilita correttamente, l'operazione di connessione non è riuscita o la connessione è stata interruppe da una chiamata [**RasHangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) .

</dd> </dl>

Un client RAS può utilizzare diversi meccanismi per determinare lo stato corrente di un'operazione di connessione. Quando un client RAS esegue la funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) in modo asincrono, la gestione connessione di accesso remoto invia notifiche di stato al [gestore di notifiche](notification-handlers.md) del client ogni volta che lo stato della connessione cambia. Inoltre, il client può usare la funzione [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per ottenere lo stato corrente di qualsiasi operazione di connessione RAS.

 

 