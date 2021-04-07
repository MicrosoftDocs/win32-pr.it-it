---
description: Una tabella di routing distribuita (DRT) esiste come una mesh di nodi cooperanti, in cui ogni nodo è un'istanza di un'applicazione che usa l'API DRT.
ms.assetid: 257ad7ea-636b-45f2-b514-4a213939d107
title: Informazioni sulle tabelle di routing distribuite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfca9f81cc609d97584ef5a11f999722c696858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881826"
---
# <a name="about-distributed-routing-tables"></a>Informazioni sulle tabelle di routing distribuite

Una tabella di routing distribuita (DRT) esiste come una mesh di nodi cooperanti, in cui ogni nodo è un'istanza di un'applicazione che usa l'API DRT. I nodi che pubblicano le chiavi sono responsabili dell'assistenza di altri nodi per la pubblicazione e la risoluzione delle chiavi. I nodi possono anche partecipare a una modalità di "risoluzione solo", che non richiede l'assistenza dei peer. Il protocollo DRT viene eseguito su un trasporto UDP/IPv6.

Un nodo che pubblica una chiave compila e gestisce una tabella di routing locale di altri nodi nella rete. Questa tabella di routing è ottimizzata in modo tale che il nodo possa individuare rapidamente una chiave specifica nella mesh trovando la chiave direttamente nella tabella di routing locale oppure chiedendo ad altri nodi di pubblicare chiavi numericamente vicine alla destinazione. Questa azione viene ripetuta fino a quando non viene trovata la chiave richiesta o il nodo determina che non esiste alcuna chiave di questo tipo.

Le chiavi DRT sono interi senza segno a 256 bit. La chiusura tra le chiavi è definita dalla differenza numerica tra di esse. Lo spazio di DRT viene considerato circolare. Ad esempio, il primo valore di chiave possibile e l'ultimo valore di chiave possibile sono considerati adiacenti.

In un DRT protetto, i nodi sono necessari per autenticare le chiavi pubblicate. Il meccanismo mediante il quale i nodi autenticano le chiavi deve essere impostato tramite l'API DRT quando viene inizializzato il DRT. Questa operazione viene eseguita scegliendo un provider di sicurezza per DRT. Un provider di sicurezza è un modulo che può produrre token usati per autenticare le chiavi e verificare i token generati da altri nodi. Deve implementare l'interfaccia del provider di sicurezza definita in questa documentazione. Windows 7 DRT viene fornito con due provider di sicurezza completamente implementati che possono essere utilizzati per creare applicazioni Windows.

Durante l'inizializzazione, un'applicazione deve fornire anche DRT con un provider bootstrap. Il provider bootstrap è un modulo in grado di recuperare gli endpoint di rete dei nodi già presenti nella rete DRT e viene chiamato da DRT quando viene stabilito un nuovo nodo. Analogamente al modulo provider di sicurezza, il provider bootstrap deve implementare un'interfaccia ben definita. Windows 7 DRT viene fornito con due provider bootstrap completamente implementati.

Il DRT considera i vicini immediati di una chiave speciale. Le cinque chiavi più vicine numericamente più piccole e le cinque chiavi più vicine numericamente maggiori rispetto a una chiave pubblicata formano un set foglia. DRT segnala le modifiche apportate al set foglia di una chiave tramite l'API DRT.

## <a name="drt-life-cycle-and-state-transitions"></a>DRT ciclo di vita e transizioni di stato

Un'applicazione può inizializzare un'istanza di DRT locale usando la funzione [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen) . Questa funzione attiva il processo di bootstrap, in cui l'API DRT chiama il provider bootstrap per apprendere le chiavi e gli endpoint di rete di altri nodi che fanno già parte di DRT. Se il provider di bootstrap individua correttamente almeno un altro nodo, DRT entra nello \_ stato attivo DRT. In questo stato, l'applicazione può cercare le chiavi pubblicate da altri nodi e può pubblicare le chiavi che possono essere risolte. Se il provider bootstrap non riesce a individuare gli altri nodi, DRT entra nello \_ stato DRT alone. Il DRT resterà nello stato DRT \_ alone e tenterà di eseguire periodicamente il bootstrap per individuare i peer e passare allo \_ stato attivo DRT.

Un nodo può passare a questi stati da DRT \_ attivo.

| Stato ciclo di vita | Condizioni                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DRT \_ da solo       | Il nodo locale non ha individuato altri nodi in DRT. In questo stato, il nodo continua ad ascoltare gli altri nodi all'interno del DRT.<br/> Se un altro nodo viene aggiunto a DRT, il nodo locale passerà allo \_ stato attivo DRT. Se la rete è inattiva, verrà effettuata la transizione a DRT \_ No \_ Network. In caso di errore grave con DRT, il nodo passerà allo \_ stato DRT Faulted.<br/> |
| DRT \_ Nessuna \_ rete | Quando un nodo perde la connettività di rete, passa a DRT \_ senza \_ stato della rete. A questo punto l'applicazione può attendere il ripristino della connettività di rete e può chiudere la DRT.<br/>                                                                                                                                                                                                                    |
| DRT con \_ errori     | Si è verificato un errore grave nel nodo locale. Ad esempio, se il computer locale esaurisce la memoria fisica.<br/> Mentre un nodo entra in questo stato, l'applicazione deve chiamare l'API [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) , correggere il problema e inizializzare nuovamente il DRT con [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).<br/>                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del API Tabella di routing distribuito](using-the-distributed-routing-table-api.md)
</dt> <dt>

[Riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 




