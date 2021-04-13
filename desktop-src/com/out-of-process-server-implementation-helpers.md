---
title: Helper di implementazione del server out-of-process
description: Helper di implementazione del server out-of-process
ms.assetid: 18641a84-56f8-4d27-9ddb-fa64011ac8ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 264d3f26b179b3ecb659ef93785c8c223b6c524e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399780"
---
# <a name="out-of-process-server-implementation-helpers"></a>Helper di implementazione del server out-of-process

Sono disponibili quattro funzioni helper che possono essere chiamate da server out-of-process per semplificare il processo di scrittura del codice server. I client COM e i server COM in-process non li chiamano in genere. Queste funzioni sono progettate per evitare race condition nell'attivazione del server quando i server hanno più Apartment o più oggetti classe. Tuttavia, possono essere usati anche per i server a thread singolo e per gli oggetti a singolo livello. Le funzioni sono le seguenti:

-   [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess)
-   [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)
-   [**CoSuspendClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects)
-   [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects)

Per arrestare correttamente, un server COM deve tenere traccia del numero di istanze dell'oggetto di cui è stata creata un'istanza e il numero di volte in cui è stato chiamato il metodo [**IClassFactory:: LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) . Solo quando entrambi i conteggi raggiungono zero può arrestare un server. Nei server COM a thread singolo la decisione di arrestare è stata coordinata con le richieste di attivazione in ingresso, che sono state serializzate dalla coda di messaggi. Il server, alla ricezione di un rilascio sull'istanza dell'oggetto finale e la decisione di arrestarsi, potrebbe revocare gli oggetti classe prima che venissero inviate altre richieste di attivazione. Se dopo questo punto è stata rilevata una richiesta di attivazione, COM riconoscerebbe che gli oggetti classe sono stati revocati e restituirebbe un errore a gestione controllo servizi (SCM), che provocherebbe quindi una nuova istanza del processo server locale da eseguire.

Tuttavia, in un server modello di Apartment, in cui gli oggetti classe diversi sono registrati in diversi Apartment e in tutti i server a thread libero, questa decisione di arrestare deve essere coordinata con richieste di attivazione su più thread, in modo che un thread del server non decida di arrestarsi mentre un altro thread del server è occupato a distribuire oggetti classe o istanze di oggetti. Un approccio classico ma complesso per risolvere questo problema consiste nel fare in modo che il server, dopo aver revocato gli oggetti classe, ricontrollare il numero di istanze e rimanere attivo fino a quando tutte le istanze non sono state rilasciate.

Per semplificare la gestione di questi tipi di race condition da parte dei writer di server, COM fornisce due funzioni di conteggio dei riferimenti:

-   [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) incrementa un conteggio di riferimenti globali per processo.
-   [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) decrementa il conteggio dei riferimenti globali per processo.

Quando il conteggio dei riferimenti globali per processo raggiunge zero, COM chiama automaticamente [**CoSuspendClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-cosuspendclassobjects), che impedisce l'arrivo di nuove richieste di attivazione. Il server può quindi annullare la registrazione dei vari oggetti classe dai diversi thread a piacimento senza preoccuparsi di poter entrare in un'altra richiesta di attivazione. Tutte le nuove richieste di attivazione verranno gestite dal gestore SCM per avviare una nuova istanza del processo del server locale.

Il modo più semplice per usare queste funzioni in un'applicazione server locale è chiamare [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) nel costruttore per ognuno dei relativi oggetti istanza e in ognuno dei relativi metodi [**IClassFactory:: LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) quando il parametro *Flock* è **true**. L'applicazione server deve chiamare anche [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess) nel distruttore di ognuno dei relativi oggetti istanza e in ognuno dei relativi metodi IClassFactory::**LockServer** quando il parametro *Flock* è **false**.

Infine, l'applicazione server deve prestare attenzione al codice restituito da [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess)e se restituisce 0, l'applicazione server deve avviare la pulitura, che, per un server con più thread, significa in genere che deve segnalare i vari thread per uscire dai cicli di messaggi e chiamare [**CoAddRefServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coaddrefserverprocess) e [**CoReleaseServerProcess**](/windows/desktop/api/combaseapi/nf-combaseapi-coreleaseserverprocess). Se vengono utilizzate le funzioni di gestione della durata del processo server, devono essere utilizzate sia nelle istanze dell'oggetto che nel metodo [**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) . in caso contrario, l'applicazione server potrebbe essere arrestata in modo anomalo.

Quando viene effettuata una richiesta [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) , com Contatta il server, esegue il marshalling dell'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) dell'oggetto classe, torna al processo client, esegue l'unmarshalling dell'interfaccia **IClassFactory** e la restituisce al client. A questo punto, i client in genere chiamano [**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver) con **true** per impedire l'arresto del processo server. Tuttavia, esiste una finestra di tempo tra il marshalling dell'oggetto classe e il momento in cui il client chiama **LockServer** in cui un altro client può connettersi allo stesso server, ottenere un'istanza e rilasciare tale istanza, causando l'arresto del server e l'interruzione del primo client con un puntatore **IClassFactory** disconnesso. Per evitare questo race condition, COM aggiunge una chiamata implicita a **LockServer** con **true** all'oggetto classe quando esegue il marshalling dell'interfaccia **IClassFactory** e una chiamata implicita a **LockServer** con **false** quando il client rilascia l'interfaccia **IClassFactory** . Di conseguenza, non è necessario eseguire chiamate **LockServer** remote al server e il proxy per **LockServer** restituisce semplicemente S \_ OK senza eseguire effettivamente la comunicazione remota della chiamata.

Durante l'inizializzazione di un processo server out-of-process è presente un'altra race condition correlata all'attivazione. Un server COM che registra più classi chiama in genere [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con il \_ server locale REGCLS \_ per ogni CLSID supportato. Una volta eseguita questa operazione per tutte le classi, il server immette il relativo ciclo di messaggi. Per un server COM a thread singolo, tutte le richieste di attivazione vengono bloccate fino a quando il server non entra nel ciclo di messaggi. Tuttavia, per un server del modello di Apartment che registra oggetti classe diversi in Apartment diversi e per tutti i server a thread libero, le richieste di attivazione possono arrivare prima di questo. Nel caso dei server del modello di Apartment, le richieste di attivazione potrebbero arrivare non appena un thread entra in un ciclo di messaggi. Nel caso di server a thread libero, una richiesta di attivazione potrebbe arrivare non appena viene registrato il primo oggetto classe. Poiché un'attivazione può avvenire in anticipo, è anche possibile che si verifichi la versione finale (e di conseguenza causare l'arresto del server) prima che il resto del server abbia avuto la possibilità di completare l'inizializzazione.

Per eliminare queste race condition e semplificare il processo del writer del server, tutti i server che vogliono registrare più oggetti classe con COM devono chiamare [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con REGCLS \_ \_ server locale \| REGCLS \_ sospeso per ogni CLSID diverso supportato dal server. Dopo che tutte le classi sono state registrate e il processo server è pronto per accettare le richieste di attivazione in ingresso, il server deve effettuare una chiamata a [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects). Questa funzione indica a COM di informare il SCM su tutte le classi registrate e inizia a consentire le richieste di attivazione al processo server. L'utilizzo di queste funzioni offre i vantaggi seguenti:

-   Viene eseguita una sola chiamata a SCM, indipendentemente dal numero di CLSID registrati, riducendo così l'ora di registrazione complessiva (e quindi il tempo di avvio dell'applicazione server).
-   Se il server dispone di più Apartment e CLSID diversi sono registrati in Apartment diversi o se il server è un server a thread libero, nessuna richiesta di attivazione sarà disponibile fino a quando il server non chiamerà [**CoResumeClassObjects**](/windows/desktop/api/combaseapi/nf-combaseapi-coresumeclassobjects), offrendo al server la possibilità di registrare tutti i relativi CLSID e di essere impostati correttamente prima di gestire le richieste di attivazione e di arrestare le richieste.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Responsabilità server COM](com-server-responsibilities.md)
</dt> </dl>

 

 