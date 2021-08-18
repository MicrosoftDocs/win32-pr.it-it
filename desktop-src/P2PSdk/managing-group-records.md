---
description: Un record di gruppo è un dato specifico pubblicato per tutti i membri attivi di un gruppo peer, ad esempio un messaggio di chat o un aggiornamento dello stato specifico dell'applicazione.
ms.assetid: 073ee4e9-0e97-451a-a808-8265575d073c
title: Gestione dei record di gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2d0ba77a315043e638ddaa28615cf84654852a13e73347ee36ee4c7d66a6e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061399"
---
# <a name="managing-group-records"></a>Gestione dei record di gruppo

Un record di gruppo è un dato specifico pubblicato per tutti i membri attivi di un gruppo peer, ad esempio un messaggio di chat o un aggiornamento dello stato specifico dell'applicazione. Un record è rappresentato dalla [**struttura PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) e contiene le informazioni seguenti su un peer:

-   L'ID record è un valore che identifica in modo univoco un record nel gruppo peer.
-   GUID che specifica il tipo di record. Le applicazioni possono supportare tipi di record diversi. Un'applicazione interpreta il **campo dati** di un record in base al tipo di record. Alcuni GUID sono riservati e la chiamata API restituisce **PEER \_ E NOT \_ \_ AUTHORIZED** quando l'applicazione tenta di usarli.
-   Set di attributi di record descritti come stringa XML. Gli attributi vengono usati durante la ricerca di record. Per altre informazioni sugli attributi, vedere [Record Attribute Schema](record-attribute-schema.md).
-   Ora peer in cui viene creato un record.
-   Ora di scadenza di un record.
-   Ora di peer in cui viene modificato un record.
-   Autore di un record.
-   Membro che modifica un record.
-   Struttura [**PEER \_ DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) che contiene la firma crittografica per tutti i campi in questa [**struttura PEER \_ RECORD.**](/windows/desktop/api/P2P/ns-p2p-peer_record) Questo campo non può essere aggiornato o modificato direttamente da un peer.
-   Struttura [**PEER \_ DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) che contiene i dati specifici dell'applicazione associati a questo record come matrice di byte. Il tipo di dati presenti in questo campo è determinato dal tipo di record definito dall'applicazione.

## <a name="obtaining-peer-group-records"></a>Recupero di record di gruppi peer

I singoli record vengono ottenuti chiamando [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) con l'ID del record. Quando si elaborano tutti i record di un tipo specifico, il set enumerato di tutti i record del gruppo peer corrente viene ottenuto chiamando prima [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords) per aprire l'enumerazione e quindi chiamando in modo iterativo [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) finché non vengono recuperati tutti i record. Al termine, chiudere l'enumerazione e rilasciare la memoria associata chiamando [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

Quando un record viene creato, eliminato o aggiornato da un peer, il record interessato viene pubblicato in tutti i membri del gruppo peer tramite l'evento **PEER GROUP EVENT RECORD \_ \_ \_ \_ CHANGE.** Si noti che se un peer non è connesso al gruppo, riceverà il record aggiornato alla successiva connessione. È importante registrarsi per questo evento con [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) se l'applicazione gestisce i record in modo significativo. In alternativa, l'applicazione può eseguire una query sul database di record su richiesta [**usando PeerGroupSearchRecords.**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords)

Quando viene generato l'evento **PEER GROUP EVENT RECORD \_ \_ \_ \_ CHANGE,** l'ID e il tipo di record specifici, nonché il tipo di modifica (aggiunta, aggiornamento, eliminazione) vengono ricevuti come struttura [**PEER EVENT RECORD CHANGE \_ \_ \_ \_ DATA.**](/windows/desktop/api/P2P/ns-p2p-peer_event_record_change_data) Questa struttura viene ottenuta con una chiamata a [**PeerGroupGetEventData.**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) Se la modifica è un'aggiunta o un aggiornamento, è necessario usare [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) per ottenere il record con l'ID specificato. Il database di record locale per l'infrastruttura viene aggiornato automaticamente.

È anche possibile cercare record specifici in base ad attributi personalizzati specifici forniti nel campo **pwzAttributes** di [**PEER \_ RECORD,**](/windows/desktop/api/P2P/ns-p2p-peer_record)nonché a qualsiasi attributo predefinito. A tale scopo, usare la [**funzione PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) con una query di ricerca XML formattata come specificato nell'argomento Formato query [di ricerca](record-search-query-format.md) record.

Per altre informazioni sull'uso dei record nell'infrastruttura peer, vedere l'argomento [Record](records.md) in [Uso dell'infrastruttura peer.](using-the-peer-infrastructure.md)

## <a name="administration-of-peer-group-records"></a>Amministrazione dei record del gruppo peer

Quando gli inviti iniziali vengono emessi dall'autore del gruppo peer, è possibile specificare che determinati membri svolga un ruolo amministrativo (AMMINISTRATORE RUOLO GRUPPO PEER) ogni volta che emette nuove credenziali per l'utente \_ \_ \_ (tramite [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) o [**PeerGroupIssueCredentials).**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) Un amministratore ha la possibilità di aggiungere, eliminare e aggiornare direttamente tutti i record del gruppo peer. Viceversa, un membro del gruppo peer con il ruolo impostato su **PEER \_ GROUP ROLE \_ \_ MEMBER** o **PEER GROUP ROLE INVITING \_ \_ \_ \_ MEMBER** può solo aggiungere, aggiornare ed eliminare i propri record.

L'autore ha il ruolo di amministratore per impostazione predefinita.

Per aggiornare un record, ottenere il record con [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) o [**PeerGroupEnumRecords,**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)apportare le modifiche e passare il record aggiornato a [**PeerGroupUpdateRecord.**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)

Per eliminare un record, passare l'ID record da eliminare a [**PeerGroupDeleteRecord.**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)

Per aggiungere un record, creare una nuova [**struttura PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) e popolare i campi seguenti:

-   **dwSize**. Questo campo contiene il valore **sizeof**([**PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record)).
-   **ftExpiration**. Questo campo contiene la data e l'ora di scadenza del record, espresse in tempo peer come **struttura FILETIME.**
-   **Digitare**. Questo campo contiene un **valore GUID** che identifica il tipo di record per l'applicazione. Se questo tipo è personalizzato per l'infrastruttura dell'applicazione, è necessario popolare anche il **campo dati.**

I campi seguenti vengono popolati dall'infrastruttura e verranno ignorati se impostati dall'applicazione:

-   **id**
-   **pwzCreatorId**
-   **pwzLastModifiedById**
-   **ftCreation**
-   **ftLastModified**
-   **securityData**

I campi rimanenti sono facoltativi. Per aggiungere questo nuovo record al gruppo peer, passarlo a [**PeerGroupAddRecord.**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)

## <a name="importing-and-exporting-records"></a>Importazione ed esportazione di record

I record del gruppo peer-to-peer vengono mantenuti in locale come database. Per salvare uno snapshot corrente del database dei record del gruppo peer in un file locale, chiamare [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)e passarlo all'handle al gruppo peer. Questo file può quindi essere trasportato in un computer o in un'applicazione diversa, che può estrarre e usare questo database di record chiamando [**PeerGroupImportDatabase.**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



