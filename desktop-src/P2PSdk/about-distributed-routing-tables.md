---
description: Una tabella di routing distribuito (DRT) esiste come mesh di nodi cooperanti, in cui ogni nodo è un'istanza di un'applicazione che usa l'API DRT.
ms.assetid: 257ad7ea-636b-45f2-b514-4a213939d107
title: Informazioni sulle tabelle di routing distribuito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8e82b25fee0bb6733bb21db82193d14e6cc8d621148b6d5c671fb04a3b2d85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011839"
---
# <a name="about-distributed-routing-tables"></a>Informazioni sulle tabelle di routing distribuito

Una tabella di routing distribuito (DRT) esiste come mesh di nodi cooperanti, in cui ogni nodo è un'istanza di un'applicazione che usa l'API DRT. I nodi che pubblicano chiavi sono responsabili dell'assistenza per la pubblicazione e la risoluzione delle chiavi da parte di altri nodi. I nodi possono anche partecipare a una modalità di "solo risoluzione", che non richiede l'assistenza dei peer. Il protocollo DRT viene eseguito su un trasporto UDP/IPv6.

Un nodo che pubblica una chiave compila e gestisce una tabella di routing locale di altri nodi nella rete. Questa tabella di routing è ottimizzata in modo che il nodo possa individuare rapidamente una chiave specifica nella rete individuando la chiave direttamente nella tabella di routing locale o richiedendo ad altri nodi di pubblicare chiavi numericamente vicine alla destinazione. Questa azione viene ripetuta fino a quando non viene trovata la chiave richiesta o il nodo non determina che tale chiave non esiste.

Le chiavi DRT sono interi senza segno a 256 bit. La vicinanza tra le chiavi è definita dalla differenza numerica tra di esse. Il keyspace DRT è considerato circolare. Ad esempio, il primo valore di chiave possibile e l'ultimo valore di chiave possibile sono considerati adiacenti.

In una libreria DRT sicura, i nodi sono necessari per autenticare le chiavi che pubblicano. Il meccanismo con cui i nodi autenticano le chiavi deve essere impostato usando l'API DRT quando viene inizializzata la libreria DRT. Questa operazione viene eseguita scegliendo un provider di sicurezza per DRT. Un provider di sicurezza è un modulo che può produrre token usati per autenticare le chiavi e verificare i token prodotti da altri nodi. Deve implementare l'interfaccia del provider di sicurezza definita in questa documentazione. Il Windows 7 DRT viene fornito con due provider di sicurezza completamente implementati che possono essere usati per compilare Windows applicazioni.

Durante l'inizializzazione, un'applicazione deve anche fornire la libreria DRT con un provider bootstrap. Il provider bootstrap è un modulo che può recuperare gli endpoint di rete dei nodi già presenti nella mesh DRT e viene chiamato da DRT quando viene stabilito un nuovo nodo. Analogamente al modulo del provider di sicurezza, il provider bootstrap deve implementare un'interfaccia ben definita. Il Windows 7 DRT viene fornito con due provider bootstrap completamente implementati.

DRT considera speciali gli elementi adiacenti immediati di una chiave. Le cinque chiavi più vicine numericamente più piccole e le cinque chiavi più vicine numericamente più grandi di un modulo di chiave pubblicato, chiamato set foglia. La libreria DRT segnala le modifiche al set foglia di una chiave tramite l'API DRT.

## <a name="drt-life-cycle-and-state-transitions"></a>Cicli di vita DRT e transizioni di stato

Un'applicazione può inizializzare un'istanza DRT locale usando [**la funzione DrtOpen.**](/windows/desktop/api/drt/nf-drt-drtopen) Questa funzione attiva il processo di bootstrap, in cui l'API DRT chiama il provider bootstrap per apprendere le chiavi e gli endpoint di rete di altri nodi che già partecipano alla libreria DRT. Se il provider bootstrap individua correttamente almeno un altro nodo, il DRT entra nello stato DRT \_ ACTIVE. In questo stato, l'applicazione può cercare le chiavi pubblicate da altri nodi e pubblicare chiavi che possono essere risolte. Se il provider bootstrap non riesce a individuare correttamente altri nodi, DRT entra nello stato DRT \_ ALONE. DRT rimarrà nello stato DRT ALONE e tenterà di eseguire periodicamente il bootstrap per individuare i peer e passare allo stato \_ DRT \_ ACTIVE.

Un nodo può eseguire la transizione a questi stati da DRT \_ ACTIVE.

| Stato del ciclo di vita | Condizioni                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DRT \_ ALONE       | Il nodo locale non ha individuato altri nodi nella libreria DRT. In questo stato, il nodo continua a restare in ascolto di altri nodi all'interno della libreria DRT.<br/> Se un altro nodo si unisce alla libreria DRT, il nodo locale passa allo stato DRT \_ ACTIVE. Se la rete non è disponibile, passa a DRT \_ NO \_ NETWORK. In caso di errore grave con DRT, il nodo passa allo stato DRT \_ FAULTED.<br/> |
| DRT \_ NO \_ NETWORK | Quando un nodo perde la connettività di rete, passa allo stato DRT \_ NO \_ NETWORK. A questo punto l'applicazione può attendere il ripristino della connettività di rete e può chiudere la libreria DRT.<br/>                                                                                                                                                                                                                    |
| ERRORE \_ DRT     | Si è verificato un errore grave all'interno del nodo locale. Ad esempio, se il computer locale esauri la memoria fisica.<br/> Mentre un nodo entra in questo stato, l'applicazione deve chiamare l'API [**DrtClose,**](/windows/desktop/api/drt/nf-drt-drtclose) correggere il problema e inizializzare nuovamente DRT con [**DrtOpen.**](/windows/desktop/api/drt/nf-drt-drtopen)<br/>                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del servizio routing distribuito API Tabella](using-the-distributed-routing-table-api.md)
</dt> <dt>

[Informazioni di riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 




