---
title: Gestione degli oggetti
description: Questa sezione illustra l'uso corretto dei tipi di oggetto API della piattaforma filtro Windows (WFP).
ms.assetid: 2625ef9a-0e62-4e21-ba93-047965d0d782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc41560bb85a7e79c0262d77c0b34fe6c1d9bfd6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472907"
---
# <a name="object-management"></a>Gestione degli oggetti

Questa sezione illustra l'uso corretto dei tipi di oggetto API della piattaforma filtro Windows (WFP).

## <a name="sessions"></a>Sessioni

L'API PAM è orientata alla sessione e la maggior parte delle chiamate di funzione viene eseguita nel contesto di una sessione. Viene creata una nuova sessione client chiamando [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). La sessione termina quando il client chiama [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0) o termina il processo client. Quando una sessione viene distrutta, sia a scopo che tramite il rundown RPC, il motore di filtro di base (BFE) interrompe prima di tutto qualsiasi transazione esistente.

Quando si crea una nuova sessione, il chiamante può creare una sessione dinamica passando il [**flag \_ \_ \_ dinamico del flag di sessione FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) a [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). Tutti gli oggetti aggiunti durante una sessione dinamica vengono eliminati automaticamente al termine della sessione.

## <a name="transactions"></a>Transazioni

L'API PAM è transazionale e la maggior parte delle chiamate di funzione viene eseguita nel contesto di una transazione. I chiamanti possono usare [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0), [**FwpmTransactionCommit0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactioncommit0)e [**FwpmTransactionAbort0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionabort0) per controllare in modo esplicito le transazioni. Tuttavia, se una chiamata di funzione viene eseguita all'esterno di una transazione esplicita, verrà eseguita all'interno di una transazione implicita. Se è in corso una transazione, quando una sessione viene terminata, viene automaticamente interrotta. Le transazioni implicite non vengono mai interrotte forzatamente.

Le transazioni sono di sola lettura o di lettura/scrittura e impongono una semantica[acid](../cossdk/acid-properties.md)(isolable Durable) rigorosa e coerente.

In ogni sessione client può essere in corso una sola transazione alla volta. Se il chiamante tenta di avviare una seconda transazione prima di eseguire il commit o l'interruzione del primo, BFE restituisce un errore.

Se un'operazione ha esito negativo nel corso di una transazione, non influisce sullo stato complessivo della transazione. Si supponga, ad esempio, che il client avvii una transazione e chiami [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) tre volte prima che una quarta chiamata abbia esito negativo. Il client ha ora la possibilità di:

-   L'interruzione della transazione, nel qual caso non verrà aggiunto alcun filtro.
-   Viene eseguito il commit della transazione, nel qual caso verranno aggiunti i primi tre filtri.
-   Continuando con più operazioni, tra cui potenzialmente ritentare il [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)non riuscito.

Quando si inizia una transazione, BFE attende finché il [**txnWaitTimeoutInMSec**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) della sessione non scade per acquisire il blocco. Se il blocco non viene acquisito entro questo intervallo di tempo, l'acquisizione del blocco (e la chiamata [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) ) avranno esito negativo. Ciò impedisce ai client di rispondere in modo indefinito. Se il client non ha specificato un timeout di blocco, il valore predefinito è 15 secondi.

Ogni transazione dispone anche di un timeout di blocco. Si tratta dell'intervallo di tempo massimo che può essere proprietario del blocco. Se il proprietario non rilascia il blocco entro questo intervallo di tempo, la transazione viene interrotta forzatamente, causando il rilascio del blocco. Il timeout del blocco non è configurabile. È infinito per i chiamanti in modalità kernel e un'ora per i chiamanti in modalità utente. Se una transazione viene interrotta forzatamente, la chiamata successiva effettuata all'interno di tale transazione avrà esito negativo con **FWP \_ E \_ transazione \_ interrotti**.

## <a name="object-lifetimes"></a>Durata degli oggetti

Gli oggetti possono avere una delle quattro durate possibili:

-   Dinamico: un oggetto è dinamico solo se viene aggiunto usando un handle di sessione dinamico. Gli oggetti dinamici sono attivi fino a quando non vengono eliminati o la sessione di appartenenza non viene terminata.
-   Static: gli oggetti sono statici per impostazione predefinita. Gli oggetti statici rimangono attivi fino a quando non vengono eliminati, BFE si interrompe o il sistema viene arrestato.
-   Persistente: gli oggetti permanenti vengono creati passando il flag **\_ \* \_ \_ permanente del flag FWPM** appropriato a una funzione **\* Add0 FWPM** . Gli oggetti permanenti rimangono attivi fino a quando non vengono eliminati.
-   Incorporati: gli oggetti predefiniti sono predefiniti da BFE e non possono essere aggiunti o eliminati. Si trovano per sempre.

I filtri nei livelli in modalità kernel possono essere contrassegnati come filtri della fase di avvio passando il flag appropriato a [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0). I filtri dell'ora di avvio vengono aggiunti al sistema all'avvio del driver TCP/IP e vengono rimossi al termine dell'inizializzazione di BFE. Quando BFE viene avviato, vengono aggiunti oggetti permanenti.

In molti casi, è possibile che un provider di criteri non desideri applicare i criteri permanenti se il provider è stato disabilitato. Quando si aggiunge un provider, il chiamante può specificare un nome di servizio Windows facoltativo. Quando si aggiungono oggetti permanenti, il chiamante può facoltativamente specificare il provider di cui è proprietario tale oggetto. All'avvio del servizio, BFE aggiunge solo oggetti permanenti al sistema se non sono associati a un provider oppure il provider associato non dispone di un nome di servizio Windows o se il servizio Windows associato è impostato su avvio automatico.

## <a name="object-associations"></a>Associazioni di oggetti

Alcuni oggetti contengono riferimenti ad altri oggetti. Un filtro, ad esempio, fa sempre riferimento a un livello e può fare riferimento a un callout e a un contesto del provider. Gli oggetti non possono fare riferimento a oggetti che possono avere una durata più breve. Un oggetto dinamico, quindi, non può fare riferimento a un oggetto dinamico da un'altra sessione. Un oggetto statico non può fare riferimento a un oggetto dinamico. Un oggetto persistente non può fare riferimento a un oggetto dinamico, a un oggetto statico o a un oggetto persistente di proprietà di un provider diverso.

Non è possibile eliminare un oggetto finché non vengono eliminati prima tutti gli oggetti che vi fanno riferimento.

## <a name="luids-and-guids"></a>Gli LUID e GUID

Tutti gli oggetti API PAM in modalità utente (FWPM) sono identificati da un identificatore univoco globale (**GUID**) e fanno riferimento ad altri oggetti in base ai relativi **GUID**. Il **GUID** deve essere univoco solo all'interno del tipo di oggetto. Ad esempio, un filtro e un contesto del provider possono avere lo stesso **GUID**, ma due filtri non possono. Quando si aggiunge un nuovo oggetto, i chiamanti possono assegnare il **GUID** dell'oggetto o lasciarlo inizializzato a zero e consentire a BFE di assegnare il **GUID**.

Tutti gli oggetti API PAM in modalità kernel (FWPS) sono identificati da un identificatore univoco locale (**LUID**) e fanno riferimento ad altri oggetti in base al relativo LUID. Il passaggio da **GUID** a **LUID** consente a WFP di conservare il pool non di paging e di ottimizzare l'elaborazione in fase di esecuzione. La larghezza di **LUID** dipende dal tipo di oggetto e dagli intervalli da un **UInt16** a un **UInt64**. **LUID** s sono sempre assegnati da BFE.

 

 