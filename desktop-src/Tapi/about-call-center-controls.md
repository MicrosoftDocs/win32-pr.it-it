---
description: TAPI 3 definisce cinque oggetti ACD principali che l'agente gestore Accoda il gruppo ACD, l'agente e la sessione di Agent. Estende anche l'oggetto TAPI con un'interfaccia aggiuntiva ITTAPICallCenter.
ms.assetid: 6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7
title: Informazioni sui controlli Call Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c91601fadeb1c3ba83e3ed5756eefb3ed34427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131646"
---
# <a name="about-call-center-controls"></a>Informazioni sui controlli Call Center

TAPI 3 definisce cinque oggetti ACD principali: il gestore dell'agente, la coda, il gruppo ACD, l'agente e la sessione dell'agente. Estende anche l'oggetto TAPI con un'interfaccia aggiuntiva, [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter).

## <a name="agent-object"></a>Oggetto Agent

L'oggetto Agent rappresenta un agente in grado di gestire le chiamate. Si tratta in genere di una persona, ma può trattarsi di un IVR o di un'altra combinazione di software e hardware. Gli agenti sono chiave per un Call Center; sono responsabili della ricezione e dell'elaborazione delle chiamate in ingresso e, in alcuni casi, dell'esecuzione di chiamate in uscita a clienti o Prospect.

In TAPI l'oggetto Agent è direttamente correlato a un account utente per garantire la compatibilità con i sistemi di cambio legacy esistenti. Inoltre, per garantire la compatibilità con i sistemi di commutazione legacy esistenti, è possibile che l'agente sia correlato anche a un ID agente commutatore.

L'oggetto Agent espone l'interfaccia [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent) . Questa interfaccia implementa i metodi che consentono di creare una sessione di Agent e recuperare le statistiche, ad esempio le chiamate totali gestite. Le applicazioni possono utilizzare l'oggetto Agent per modificare lo stato dell'agente e determinare le statistiche globali degli agenti.

## <a name="agent-handler-object"></a>Oggetto gestore agente

Un gestore agenti rappresenta il software o l'hardware in grado di passare le chiamate a un gruppo di agenti. Si tratta in genere di un Commuter proprietario che si connette all'esterno delle righe ai telefoni delle stazioni degli agenti. La maggior parte dei sistemi ACD dispone di un solo switch, ma le operazioni di grandi dimensioni potrebbero essere maggiori. Nel caso in cui un agente disponga di dispositivi in più di un sistema ACD, l'agente visualizzerà un numero corrispondente di oggetti gestore agenti. In ogni sistema ACD sarà presente anche un'istanza dell'oggetto Agent relativa all'aspetto dell'agente.

L'oggetto gestore agenti espone l'interfaccia [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) . Questa interfaccia implementa i metodi che forniscono informazioni sui [gruppi ACD](#acd-group-object) associati al gestore dell'agente e sugli indirizzi che possono usare.

## <a name="agent-session-object"></a>Oggetto sessione agente

Una sessione di Agent rappresenta un agente che ha eseguito l'accesso ed è qualificato per gestire le chiamate per un particolare [Gruppo ACD](#acd-group-object). Una sessione di Agent è un oggetto creato dinamicamente che mette in correlazione un agente a un gruppo ACD, per il quale fornirà il servizio e anche all'indirizzo, dove riceveranno le chiamate (torretta, stazione, telefono e così via). Le applicazioni possono utilizzare l'oggetto sessione agente per tenere traccia dell'attività dell'agente in un particolare gruppo ACD.

L'oggetto Session dell'agente espone l'interfaccia [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession) . Questa interfaccia implementa metodi che consentono di recuperare informazioni, ad esempio il tempo medio di conversazione per una chiamata.

## <a name="acd-group-object"></a>Oggetto gruppo ACD

Un gruppo ACD rappresenta una classe di chiamate che richiede un particolare tipo di gestione. Ad esempio, alcune chiamate in ingresso per il Call Center di una banca possono riguardare gli account esistenti e altri potrebbero essere correlati a nuovi account. Alcuni agenti possono avere competenze in entrambe le aree, ma la maggior parte sarà specializzata in uno. Verranno creati gruppi ACD per gestire ogni tipo di chiamata. Un gruppo ACD servizi una o più code. Poiché le chiamate in ingresso vengono classificate, verranno passate alle code associate al gruppo ACD pertinente. Una chiamata proveniente dalla coda viene passata a un agente che ha creato un [oggetto sessione di Agent](#agent-session-object) indicante che è in grado di gestire le chiamate da tale gruppo ACD.

L'oggetto gruppo ACD espone l'interfaccia [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup) . Questa interfaccia implementa i metodi che consentono di accedere alle code associate al gruppo ACD corrente.

## <a name="queue-object"></a>Queue (oggetto)

L'oggetto Queue rappresenta un punto all'interno del sistema ACD in cui le chiamate vengono temporaneamente mantenute in sospeso. L'oggetto Queue espone l'interfaccia [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue) . Questa interfaccia implementa i metodi che raccolgono statistiche in una coda, ad esempio il numero di chiamate attualmente accodate. Il [proxy ACD](acd-proxy.md) usa queste informazioni per distribuire le chiamate agli agenti e per produrre report amministrativi.

L'accesso a un oggetto Queue consente a un'applicazione di leggere una serie di statistiche standard relative all'utilizzo della coda, ma non offre la possibilità di controllare le chiamate sulla coda. Solo le applicazioni con accesso agli indirizzi e alle righe associate (in genere l'applicazione proxy ACD) sarebbero in grado di controllare le chiamate sulla coda.

La maggior parte delle code si riferisce direttamente a un [oggetto gruppo ACD](#acd-group-object)e manterrà una chiamata fino a quando un agente non è in grado di gestirlo. È possibile che esistano altre code per consentire guide di chiamata complesse (il percorso definito che una chiamata senza risposta verrà eseguita tramite un'opzione). Ad esempio, le chiamate possono essere inserite nelle code di attesa prima di essere indirizzate a una coda gestita da un gruppo ACD.

 

 
