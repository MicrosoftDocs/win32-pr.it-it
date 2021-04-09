---
title: Effetti sulle applicazioni Directory-Enabled
description: In questo argomento viene descritto l'impatto sulle applicazioni abilitate alla directory quando si verificano differenze di versione, aggiornamenti parziali o collisioni.
ms.assetid: 0aec6fe3-7757-4472-bc18-add2327d4e1b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061818fc791e1c75d440d0c477a321b8c4e5edfb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956319"
---
# <a name="impact-on-directory-enabled-applications"></a>Effetti sulle applicazioni Directory-Enabled

## <a name="version-skew"></a>Sfasamento della versione

L'asimmetria della versione si verifica quando le applicazioni leggono gli stessi oggetti da repliche diverse prima che una modifica venga replicata. Le applicazioni che leggono la replica remota riconoscono l'oggetto non modificato. Lo sfasamento della versione è un problema quando una determinata applicazione o un set di applicazioni utilizza i dati nella directory per interagire.

Un servizio RPC, ad esempio, può pubblicare gli endpoint nella directory usando le API RPC standard, ad esempio [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta). I client si connettono al servizio tramite la ricerca dell'endpoint desiderato nella directory ( [**RpcNsBindingLookupBegin**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), [**RpcNsBindingLookupNext**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)e così via) e l'associazione.

Si supponga che un servizio RPC ₁ pubblichi endpoint ES ₁ e successivamente si sposta in un altro computer. L'endpoint originale es ₁ viene modificato in E<sub>S2,</sub> riflettendo l'indirizzo del nuovo computer. I client che leggono le repliche remote del servizio directory non sono in grado di connettersi al servizio fino a quando l'endpoint aggiornato non viene replicato. Tuttavia, il trasferimento di un servizio da un computer a un altro è un evento raro; Pertanto, è consigliabile che si verifichino raramente interruzioni/ritardi, soprattutto se lo spostamento del servizio è ben pianificato.

## <a name="partial-updates"></a>Aggiornamenti parziali

In generale, l'aggiornamento parziale si verifica quando un'applicazione legge un set di dati mentre un'altra applicazione scrive nello stesso set di dati. Si tratta di una situazione che può verificarsi con qualsiasi applicazione in un sistema multimaster. Questa situazione può verificarsi in molti modi. È possibile che più di un'applicazione scriva contemporaneamente nello stesso set di dati. Se lo si osserva in questo modo, il servizio replica directory è semplicemente un'altra applicazione che potrebbe potenzialmente scrivere nello stesso set di dati che può essere letto da un'altra applicazione. Potrebbe trattarsi di un potenziale problema per un'applicazione. Tuttavia, l'intervallo di tempo in cui un aggiornamento parziale può influire sull'applicazione è relativamente piccolo. Questo dovrebbe essere raramente un problema per le applicazioni che non dipendono dalla sincronizzazione di più oggetti. Se l'applicazione dipende in maniera elevata dalla sincronizzazione di un set correlato di oggetti, è opportuno considerare gli effetti di un aggiornamento parziale nella progettazione dell'applicazione.

In termini di replica della directory, l'aggiornamento parziale si verifica quando le applicazioni leggono lo stesso set di oggetti da repliche diverse mentre è in corso la replica. Le applicazioni nella replica remota visualizzano alcune, ma non tutte, le modifiche.

> [!Note]  
> La finestra in cui l'aggiornamento parziale può influire su un'applicazione è di dimensioni ridotte: l'applicazione deve iniziare a leggere oggetti mentre è in corso la replica in ingresso, dopo la ricezione di uno o più oggetti modificati correlati, ma prima della ricezione di tutti. Il tempo tra gli aggiornamenti nella replica di origine influiscono direttamente sulle dimensioni di questa finestra. gli aggiornamenti che si verificano in modo ravvicinato nel tempo vengono replicati vicino nel tempo. Un aggiornamento parziale può costituire un problema quando un'applicazione utilizza un set correlato di oggetti.

 

Ad esempio, un servizio di accesso remoto può utilizzare la directory per archiviare i dati dei criteri e del profilo. I dati dei criteri vengono archiviati in un set di oggetti e il profilo in un altro set. Quando un utente si connette al servizio di accesso remoto, il servizio di accesso remoto legge i criteri per determinare se l'utente è autorizzato a connettersi e, in tal caso, il profilo da applicare alla sessione utente. L'aggiornamento parziale può influire sul servizio di accesso remoto in diversi modi:

-   Se il criterio è complesso ed è costituito da più oggetti, il servizio di accesso remoto potrebbe leggere un criterio parzialmente aggiornato, causando un rifiuto errato o la concessione del servizio all'utente, l'impossibilità di elaborare i criteri a causa di un'incoerenza interna e così via.
-   Se i criteri e i profili sono stati aggiornati, il servizio potrebbe elaborare correttamente i criteri ma applicare un profilo non aggiornato, perché gli oggetti criteri sono stati replicati, ma gli oggetti profilo non lo sono.
-   Se il profilo è complesso ed è costituito da più oggetti, il servizio potrebbe elaborare correttamente il criterio, ma applicare un profilo parzialmente aggiornato perché gli oggetti criteri sono stati replicati, ma solo alcuni degli oggetti del profilo hanno eseguito questa operazione.

## <a name="collisions"></a>Conflitti

I conflitti si verificano quando gli stessi attributi di due o più repliche di un determinato oggetto vengono modificati durante lo stesso intervallo di replica. Il processo di replica riconcilia la collisione; a causa della riconciliazione, un utente o un'applicazione può "vedere" un valore diverso da quello che ha scritto.

Un esempio semplice è quello di informazioni sull'indirizzo utente: un utente modifica un indirizzo postale nella replica R1 e un amministratore modifica lo stesso indirizzo di posta elettronica presso replica R2. Un valore scritto viene propagato fino a quando non viene selezionato un altro valore per quel valore dal meccanismo di riconciliazione dei conflitti. Finché un valore continua a "vincere" con altri valori nel processo di risoluzione dei conflitti, il valore continua a propagarsi. In definitiva, questo valore "vincente" verrà propagato in R1, R2 e in tutte le altre repliche se non vengono apportate altre modifiche.

La risoluzione dei conflitti è un problema per le applicazioni che fanno supposizioni sulla coerenza interna degli oggetti o dei set di oggetti. Ad esempio, un servizio di gestione dell'allocazione della larghezza di banda di rete archivia i dati della larghezza di banda di rete per un determinato segmento di rete nella directory in un oggetto O1 L'oggetto contiene la larghezza di banda disponibile in bit al secondo e la larghezza di banda massima che ogni singolo utente può riservare. Il servizio prevede che la larghezza di banda riservabile dall'utente sarà sempre minore o uguale alla larghezza di banda disponibile.

Considerare la sequenza di eventi seguente:

-   L'oggetto nello stato iniziale con replica completa fornisce la larghezza di banda disponibile come 56 kilobit al secondo e la larghezza di banda riservata dall'utente come 9.600 bit al secondo.
-   Un amministratore della replica R ₁ modifica i valori rispettivamente in 64K e 19.200.
-   Un amministratore presso la replica R ₂ modifica i valori rispettivamente in 10 milioni e 1 milione prima dell'arrivo dell'aggiornamento da R ₁.

Supponendo che gli attributi in questione abbiano numeri di versione uguali quando si verificano gli aggiornamenti, c'è una piccola, ma reale possibilità che l'oggetto finisca con una larghezza di banda massima di 64K e un massimo di 1 milione di utenti, se l'applicazione esegue gli aggiornamenti come operazioni di scrittura separate. L'applicazione deve aggiornare sempre entrambe le proprietà in una singola operazione.

 

 