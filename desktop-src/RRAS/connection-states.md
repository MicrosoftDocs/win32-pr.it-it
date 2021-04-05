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
# <a name="connection-states"></a><span data-ttu-id="869da-103">Stati di connessione</span><span class="sxs-lookup"><span data-stu-id="869da-103">Connection States</span></span>

<span data-ttu-id="869da-104">Durante il processo di connessione a un server remoto, la gestione connessione di accesso remoto e il server RAS sul computer remoto eseguono diversi passaggi per stabilire la connessione.</span><span class="sxs-lookup"><span data-stu-id="869da-104">During the process of connecting to a remote server, the Remote Access Connection Manager and the RAS server on the remote computer perform several steps to establish the connection.</span></span> <span data-ttu-id="869da-105">Ognuno di questi passaggi è identificato da uno stato di connessione.</span><span class="sxs-lookup"><span data-stu-id="869da-105">Each of these steps is identified by a connection state.</span></span> <span data-ttu-id="869da-106">L'enumerazione [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) è un set di valori che corrispondono a questi stati di connessione.</span><span class="sxs-lookup"><span data-stu-id="869da-106">The [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumeration is a set of values that correspond to these connection states.</span></span> <span data-ttu-id="869da-107">Gli Stati di connessione possono essere divisi nei tre gruppi seguenti:</span><span class="sxs-lookup"><span data-stu-id="869da-107">The connection states can be divided into the following three groups:</span></span>

<dl> <dt>

<span data-ttu-id="869da-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Stati in esecuzione</span><span class="sxs-lookup"><span data-stu-id="869da-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Running states</span></span>
</dt> <dd>

<span data-ttu-id="869da-109">Gli stati in esecuzione sono le parti dell'operazione di connessione gestite automaticamente da RAS, ad esempio la connessione ai dispositivi necessari, l'autenticazione dell'utente e l'attesa di un callback dal server remoto.</span><span class="sxs-lookup"><span data-stu-id="869da-109">The running states are the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="869da-110">A meno che non si verifichi un errore, il client RAS non deve intraprendere alcuna azione diversa da per passare la notifica all'utente.</span><span class="sxs-lookup"><span data-stu-id="869da-110">Unless an error occurs, the RAS client need take no action other than to pass the notification on to the user.</span></span>

</dd> <dt>

<span data-ttu-id="869da-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Stati sospesi</span><span class="sxs-lookup"><span data-stu-id="869da-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Paused states</span></span>
</dt> <dd>

<span data-ttu-id="869da-112">Gli [stati sospesi](paused-states.md) si verificano quando il server remoto sospende l'operazione di connessione per ottenere input aggiuntivi dall'utente.</span><span class="sxs-lookup"><span data-stu-id="869da-112">The [paused states](paused-states.md) occur when the remote server pauses the connection operation to get additional input from the user.</span></span> <span data-ttu-id="869da-113">Durante uno stato di sospensione, l'utente può digitare un numero di [callback](callback-connections.md) , un nome utente e una password diversi in caso di errore dell'autenticazione utente o una nuova password se quella precedente è scaduta.</span><span class="sxs-lookup"><span data-stu-id="869da-113">During a paused state, the user can type a [callback](callback-connections.md) number, a different user name and password if the user authentication fails, or a new password if the old one has expired.</span></span>

</dd> <dt>

<span data-ttu-id="869da-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Stati terminali</span><span class="sxs-lookup"><span data-stu-id="869da-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Terminal states</span></span>
</dt> <dd>

<span data-ttu-id="869da-115">Gli stati terminali si verificano quando la connessione è stata stabilita correttamente, l'operazione di connessione non è riuscita o la connessione è stata interruppe da una chiamata [**RasHangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) .</span><span class="sxs-lookup"><span data-stu-id="869da-115">The terminal states occur when the connection has been successfully established, the connection operation has failed, or the connection has been broken by a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) call.</span></span>

</dd> </dl>

<span data-ttu-id="869da-116">Un client RAS può utilizzare diversi meccanismi per determinare lo stato corrente di un'operazione di connessione.</span><span class="sxs-lookup"><span data-stu-id="869da-116">There are several mechanisms that a RAS client can use to determine the current state of a connection operation.</span></span> <span data-ttu-id="869da-117">Quando un client RAS esegue la funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) in modo asincrono, la gestione connessione di accesso remoto invia notifiche di stato al [gestore di notifiche](notification-handlers.md) del client ogni volta che lo stato della connessione cambia.</span><span class="sxs-lookup"><span data-stu-id="869da-117">When a RAS client executes the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function asynchronously, the Remote Access Connection Manager sends progress notifications to the client's [notification handler](notification-handlers.md) whenever the connection state changes.</span></span> <span data-ttu-id="869da-118">Inoltre, il client può usare la funzione [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per ottenere lo stato corrente di qualsiasi operazione di connessione RAS.</span><span class="sxs-lookup"><span data-stu-id="869da-118">In addition, the client can use the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the current state of any RAS connection operation.</span></span>

 

 