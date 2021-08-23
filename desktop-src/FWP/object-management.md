---
title: Gestione oggetti
description: In questa sezione viene illustrato l'uso corretto dei Windows di oggetti API wfp (Filtering Platform).
ms.assetid: 2625ef9a-0e62-4e21-ba93-047965d0d782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5cb51d4e78049d7911a4a5ed265091e05bc1cbb00ce470e332d59dd23c6026d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068851"
---
# <a name="object-management"></a>Gestione oggetti

In questa sezione viene illustrato l'uso corretto dei Windows di oggetti API wfp (Filtering Platform).

## <a name="sessions"></a>Sessioni

L'API WFP è orientata alle sessioni e la maggior parte delle chiamate di funzione viene effettuata nel contesto di una sessione. Viene creata una nuova sessione client chiamando [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). La sessione termina quando il client chiama [**FwpmEngineClose0 o**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0) il processo client termina. Quando una sessione viene distrutta, di proposito o dal rundown RPC, il Base Filtering Engine (BFE) interrompe prima qualsiasi transazione esistente.

Quando si crea una nuova sessione, il chiamante può creare una sessione dinamica passando il flag [**DINAMICO FWPM \_ SESSION FLAG \_ \_ a**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). Tutti gli oggetti aggiunti durante una sessione dinamica vengono eliminati automaticamente al termine della sessione.

## <a name="transactions"></a>Transazioni

L'API WFP è transazionale e la maggior parte delle chiamate di funzione viene effettuata nel contesto di una transazione. I chiamanti possono usare [**FwpmTransactionBegin0,**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) [**FwpmTransactionCommit0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactioncommit0)e [**FwpmTransactionAbort0 per**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionabort0) controllare in modo esplicito le transazioni. Tuttavia, se una chiamata di funzione viene eseguita all'esterno di una transazione esplicita, verrà eseguita all'interno di una transazione implicita. Se una transazione è in corso, al termine di una sessione viene interrotta automaticamente. Le transazioni implicite non vengono mai interrotte forzatamente.

Le transazioni sono di sola lettura o di lettura/scrittura e applicano una rigorosa semantica[ACID](../cossdk/acid-properties.md)(Atomic Consistent Isolated Durable).

Ogni sessione client può avere una sola transazione in corso alla volta. Se il chiamante tenta di avviare una seconda transazione prima di eseguire il commit o l'interruzione della prima, BFE restituisce un errore.

Se un'operazione ha esito negativo durante il corso di una transazione, non influisce sullo stato complessivo della transazione. Si supponga, ad esempio, che il client inizi una transazione e chiami [**correttamente FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) tre volte prima che una quarta chiamata abbia esito negativo. Il client ha ora la possibilità di:

-   Interruzione della transazione, nel qual caso non verrà aggiunto nessuno dei filtri.
-   Commit della transazione, nel qual caso verranno aggiunti i primi tre filtri.
-   Continuando con altre operazioni, incluso il tentativo potenzialmente non riuscito [**di FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).

Quando si inizia una transazione, BFE attenderà la scadenza del [**txnWaitTimeoutInMSec**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) della sessione per acquisire il blocco. Se il blocco non viene acquisito entro questo periodo di tempo, l'acquisizione del blocco (e la chiamata [**FwpmTransactionBegin0)**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) avranno esito negativo. In questo modo si impedisce ai client di non rispondere a tempo indefinito. Se il client non ha specificato un timeout di blocco, il valore predefinito è 15 secondi.

Ogni transazione ha anche un timeout di blocco. Si tratta della quantità massima di tempo per cui può essere proprietaria del blocco. Se il proprietario non rilascia il blocco entro questo periodo di tempo, la transazione viene interrotta forzatamente, causando il rilascio del blocco. Il timeout di blocco non è configurabile. È infinito per i chiamanti in modalità kernel e un'ora per i chiamanti in modalità utente. Se una transazione viene forzatamente interrotta, la chiamata successiva eseguita all'interno di tale transazione avrà esito negativo con **FWP \_ E \_ TXN \_ ABORTED**.

## <a name="object-lifetimes"></a>Durate degli oggetti

Gli oggetti possono avere una delle quattro possibili durate:

-   Dinamico: un oggetto è dinamico solo se viene aggiunto usando un handle di sessione dinamico. Gli oggetti dinamici sono in tempo reale fino a quando non vengono eliminati o la sessione proprietaria non termina.
-   Statico: gli oggetti sono statici per impostazione predefinita. Gli oggetti statici sono in tempo reale fino a quando non vengono eliminati, BFE si arresta o il sistema non viene arrestato.
-   Persistent: gli oggetti persistenti vengono creati passando il flag **PERSISTENTE FWPM \_ \* \_ \_ FLAG** appropriato a una **funzione Fwpm \* Add0.** Gli oggetti persistenti sono in tempo reale fino a quando non vengono eliminati.
-   Predefinito: gli oggetti predefiniti sono predefiniti da BFE e non possono essere aggiunti o eliminati. Vivranno per sempre.

I filtri nei livelli in modalità kernel possono essere contrassegnati come filtri in fase di avvio passando il flag appropriato a [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0). I filtri in fase di avvio vengono aggiunti al sistema all'avvio del driver TCP/IP e rimossi al termine dell'inizializzazione di BFE. Gli oggetti persistenti vengono aggiunti all'avvio di BFE.

In molti casi, un provider di criteri potrebbe non voler applicare i criteri permanenti se il provider è stato disabilitato. Quando si aggiunge un provider, il chiamante può specificare un nome di servizio Windows facoltativo. Quando si aggiungono oggetti persistenti, il chiamante può facoltativamente specificare il provider proprietario di tale oggetto. All'avvio del servizio, BFE aggiunge oggetti persistenti al sistema solo se non sono associati a un provider o se il provider associato non ha un nome di servizio Windows o se il servizio Windows associato è impostato su avvio automatico.

## <a name="object-associations"></a>Associazioni di oggetti

Alcuni oggetti hanno riferimenti ad altri oggetti. Ad esempio, un filtro fa sempre riferimento a un livello e può fare riferimento a un callout e a un contesto del provider. Gli oggetti non possono fare riferimento a oggetti che possono avere una durata più breve. Di conseguenza, un oggetto dinamico non può fare riferimento a un oggetto dinamico da una sessione diversa. Un oggetto statico non può fare riferimento a un oggetto dinamico. Un oggetto persistente non può fare riferimento a un oggetto dinamico, a un oggetto statico o a un oggetto persistente di proprietà di un provider diverso.

Un oggetto non può essere eliminato fino a quando non sono stati eliminati per la prima volta tutti gli oggetti che fanno riferimento a esso.

## <a name="luids-and-guids"></a>GUID e LUID

Tutti gli oggetti API WFP in modalità utente (FWPM) sono identificati da un identificatore univoco globale **(GUID)** e fanno riferimento ad altri oggetti in base ai **relativi GUID.** Il **GUID deve** essere univoco solo all'interno del tipo di oggetto. Ad esempio, un filtro e un contesto del provider possono avere lo stesso **GUID,** ma due filtri non possono. Quando si aggiunge un nuovo oggetto, i chiamanti possono assegnare il **GUID** dell'oggetto o lasciarlo inizializzato zero e consentire a BFE di assegnare il **GUID**.

Tutti gli oggetti API WFP (FWPS) in modalità kernel sono identificati da un identificatore univoco locale **(LUID)** e fanno riferimento ad altri oggetti in base al relativo LUID. Il passaggio da **GUID** a **LUID** consente a WFP di conservare pool non di paging e ottimizzare l'elaborazione in fase di esecuzione. La larghezza del **LUID** dipende dal tipo di oggetto e varia da **UINT16** a **UINT64.** **I FILE LUID** vengono sempre assegnati da BFE.

 

 