---
title: Impatto sulle Directory-Enabled applicazioni
description: Questo argomento descrive l'impatto sulle applicazioni abilitate per la directory quando si verificano affollamenti della versione, aggiornamenti parziali o conflitti.
ms.assetid: 0aec6fe3-7757-4472-bc18-add2327d4e1b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601a5bbffda08f0789875176193977cbecfc34596a9900c870f81cfd677b9ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187676"
---
# <a name="impact-on-directory-enabled-applications"></a>Impatto sulle Directory-Enabled applicazioni

## <a name="version-skew"></a>A inclinazione della versione

L'avallamento delle versioni si verifica quando le applicazioni leggono gli stessi oggetti da repliche diverse prima della replica di una modifica. Le applicazioni che leggono la replica remota riconoscono l'oggetto non modificato. L'afa delle versioni è un problema quando un'applicazione o un set di applicazioni specifico usa i dati nella directory per interagire.

Ad esempio, un servizio RPC può pubblicare i propri endpoint nella directory usando API RPC standard , ad esempio [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta). I client si connettono al servizio cercando l'endpoint desiderato nella directory ( [**RpcNsBindingLookupBegin,**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) [**RpcNsBindingLookupNext**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)e così via) e associandovi.

Si supponga che un servizio RPC S₁ pubblica l'endpoint Es₁ e successivamente si sposta in un computer diverso. L'endpoint originale Es₁ viene modificato in E<sub>s2,</sub> che riflette l'indirizzo del nuovo computer. I client che leggono le repliche remote del servizio directory non possono connettersi al servizio finché non viene replicato l'endpoint aggiornato. Tuttavia, lo spostamento di un servizio da un computer a un altro è un evento raro. Pertanto, questa interruzione/ritardo deve essere rilevata raramente, soprattutto se lo spostamento del servizio è ben pianificato.

## <a name="partial-updates"></a>Aggiornamenti parziali

In generale, l'aggiornamento parziale si verifica quando un'applicazione legge un set di dati mentre un'altra applicazione scrive nello stesso set di dati. Si tratta di una situazione che può verificarsi con qualsiasi applicazione in un sistema multi-master. Questo problema può verificarsi in molti modi. È possibile avere più applicazioni che scrivono nello stesso set di dati contemporaneamente. Se si osserva in questo modo, il servizio di replica directory è solo un'altra applicazione che potrebbe potenzialmente scrivere nello stesso set di dati che un'altra applicazione potrebbe leggere. Questo potrebbe essere un potenziale problema per un'applicazione. Tuttavia, la finestra temporale in cui un aggiornamento parziale può influire sull'applicazione è relativamente piccola. Questo dovrebbe essere raramente un problema per le applicazioni che non dipendono dalla sincronizzazione di più oggetti. Se l'applicazione dipende fortemente dalla sincronizzazione di un set correlato di oggetti, è necessario considerare gli effetti di un aggiornamento parziale nella progettazione dell'applicazione.

In termini di replica della directory, l'aggiornamento parziale si verifica quando le applicazioni leggono lo stesso set di oggetti da repliche diverse mentre è in corso la replica. Le applicazioni nella replica remota visualizzano alcune, ma non tutte, le modifiche.

> [!Note]  
> La finestra in cui l'aggiornamento parziale può influire su un'applicazione è ridotta: l'applicazione deve iniziare a leggere gli oggetti mentre è in corso la replica in ingresso, dopo la ricezione di uno o più oggetti modificati correlati, ma prima che siano stati ricevuti tutti. Il tempo tra gli aggiornamenti nella replica di origine influisce direttamente sulle dimensioni di questa finestra. Gli aggiornamenti che si verificano vicini nel tempo vengono replicati vicini nel tempo. L'aggiornamento parziale può essere un problema quando un'applicazione usa un set correlato di oggetti.

 

Ad esempio, un servizio di accesso remoto può usare la directory per archiviare i dati dei criteri e del profilo. I dati dei criteri vengono archiviati in un set di oggetti e il profilo in un altro set. Quando un utente si connette al servizio di accesso remoto, il servizio di accesso remoto legge i criteri per determinare se l'utente è autorizzato a connettersi e, in tal caso, quale profilo applicare alla sessione utente. L'aggiornamento parziale può influire sul servizio di accesso remoto in diversi modi:

-   Se il criterio è complesso ed è costituito da più oggetti, il servizio di accesso remoto potrebbe leggere un criterio parzialmente aggiornato con conseguente negazione o concessione non corretta del servizio all'utente, impossibilità di elaborare i criteri a causa di incoerenza interna e così via.
-   Se i criteri e i profili sono stati aggiornati, il servizio potrebbe elaborare correttamente i criteri ma applicare un profilo non aggiornato, perché gli oggetti criteri sono stati replicati, ma gli oggetti profilo non lo hanno.
-   Se il profilo è complesso ed è costituito da più oggetti, il servizio potrebbe elaborare correttamente i criteri, ma applicare un profilo parzialmente aggiornato perché gli oggetti criteri sono stati replicati, ma solo alcuni oggetti profilo lo hanno fatto.

## <a name="collisions"></a>Conflitti

Le collisioni si verificano quando gli stessi attributi di due o più repliche di un determinato oggetto vengono modificati durante lo stesso intervallo di replica. Il processo di replica riconcilia la collisione. a causa della riconciliazione, un utente o un'applicazione può "vedere" un valore diverso da quello scritto.

Un esempio semplice sono le informazioni sull'indirizzo utente: un utente modifica un indirizzo postale nella replica R1 e un amministratore modifica lo stesso indirizzo postale nella replica R2. Un valore scritto viene propagato fino a quando non viene selezionato un altro valore su tale valore dal meccanismo di riconciliazione delle collisioni. Finché un valore continua a "conquistare" rispetto ad altri valori nel processo di risoluzione delle collisioni, il valore continua a propagarsi. In definitiva, questo valore "vincente" verrà propagato a R1,R2 e a tutte le altre repliche se non vengono apportate altre modifiche.

La risoluzione delle collisioni è un problema per le applicazioni che fanno supposizioni sulla coerenza interna di oggetti o set di oggetti. Ad esempio, un servizio di gestione dell'allocazione della larghezza di banda di rete archivia i dati della larghezza di banda di rete per un determinato segmento di rete nella directory in un oggetto O1. L'oggetto contiene la larghezza di banda disponibile in bit al secondo e la larghezza di banda massima che un singolo utente può riservare. Il servizio prevede che la larghezza di banda riservata dell'utente sia sempre minore o uguale alla larghezza di banda disponibile.

Considerare la sequenza di eventi seguente:

-   L'oggetto nello stato iniziale completamente replicato offre la larghezza di banda disponibile come 56 kilobit al secondo e la larghezza di banda riservata dall'utente come 9.600 bit al secondo.
-   Un amministratore della replica R₁ i valori vengono rispettivamente 64.000 e 19.200.
-   Un amministratore della replica R I modifica i valori rispettivamente in 10 milioni e 1 milione prima dell'arrivo dell₁ aggiornamento da R.

Supponendo che gli attributi in questione hanno numeri di versione uguali quando si verificano gli aggiornamenti, esiste una piccola, ma reale, possibilità che l'oggetto finirà con una larghezza di banda massima di 64.000 e un valore massimo riservabile dall'utente di 1 milione, se l'applicazione esegue gli aggiornamenti come operazioni di scrittura separate. L'applicazione deve sempre aggiornare entrambe le proprietà in una singola operazione.

 

 