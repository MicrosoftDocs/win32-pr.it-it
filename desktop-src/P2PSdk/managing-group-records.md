---
description: Un record di gruppo è costituito da dati specifici pubblicati in tutti i membri attivi di un gruppo peer, ad esempio un messaggio di chat o un aggiornamento dello stato specifico dell'applicazione.
ms.assetid: 073ee4e9-0e97-451a-a808-8265575d073c
title: Gestione dei record di gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6d9e3257cc597b715dc9c65eb5945c00c15286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312257"
---
# <a name="managing-group-records"></a>Gestione dei record di gruppo

Un record di gruppo è costituito da dati specifici pubblicati in tutti i membri attivi di un gruppo peer, ad esempio un messaggio di chat o un aggiornamento dello stato specifico dell'applicazione. Un record è rappresentato dalla struttura [**del \_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) e contiene le informazioni seguenti su un peer:

-   L'ID record è un valore che identifica in modo univoco un record nel gruppo peer.
-   GUID che specifica il tipo di record. Le applicazioni possono supportare tipi di record diversi. Un'applicazione interpreta il campo **dati** di un record in base al tipo di record. Alcuni GUID sono riservati e la chiamata API restituisce **peer \_ E \_ non \_ autorizzato** quando l'applicazione tenta di usarli.
-   Set di attributi di record descritto come stringa XML. Gli attributi vengono utilizzati durante la ricerca di record. Per ulteriori informazioni sugli attributi, vedere [record attribute schema](record-attribute-schema.md).
-   Tempo peer per la creazione di un record.
-   Tempo peer per la scadenza di un record.
-   Tempo peer per la modifica di un record.
-   Autore di un record.
-   Membro che modifica un record.
-   Struttura [**di \_ dati peer**](/windows/desktop/api/P2P/ns-p2p-peer_data) contenente la firma crittografica per tutti i campi in questa struttura di [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Questo campo non può essere aggiornato o modificato direttamente da un peer.
-   Struttura [**di \_ dati peer**](/windows/desktop/api/P2P/ns-p2p-peer_data) che contiene i dati specifici dell'applicazione associati a questo record sotto forma di matrice di byte. Il tipo di dati presenti in questo campo è determinato dal tipo di record definito dall'applicazione.

## <a name="obtaining-peer-group-records"></a>Recupero di record di gruppi di peer

I singoli record vengono ottenuti chiamando [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) con l'ID del record. Quando si elaborano tutti i record di un tipo specifico, il set enumerato di tutti i record del gruppo peer correnti viene ottenuto chiamando prima [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords) per aprire l'enumerazione e quindi chiamando in modo iterativo [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) fino a quando non vengono recuperati tutti i record. Al termine, chiudere l'enumerazione e rilasciare la memoria associata chiamando [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

Quando un record viene creato, eliminato o aggiornato da un peer, il record interessato viene pubblicato in tutti i membri del gruppo peer per mezzo dell'evento di **\_ modifica del \_ \_ record dell' \_ evento del gruppo peer** . Si noti che se un peer non è connesso al gruppo, riceverà il record aggiornato alla successiva connessione. È importante registrare questo evento con [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) se l'applicazione gestisce o gestisce i record in modo significativo. In alternativa, l'applicazione può eseguire query sul database di record su richiesta usando [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords).

Quando viene generato l'evento di **modifica del record dell' \_ evento del gruppo \_ \_ \_ peer** , l'ID e il tipo del record, nonché il tipo di modifica (aggiunta, aggiornamento, eliminazione) vengono ricevuti come struttura dei dati di modifica di un [**\_ record di eventi \_ \_ \_ peer**](/windows/desktop/api/P2P/ns-p2p-peer_event_record_change_data) . Questa struttura viene ottenuta con una chiamata a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Se la modifica è un'aggiunta o un aggiornamento, è necessario usare [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) per ottenere il record con l'ID fornito. Il database di record locale per l'infrastruttura viene aggiornato automaticamente.

È anche possibile cercare record specifici in base a attributi personalizzati specifici specificati nel campo **pwzAttributes** del [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record), oltre a eventuali attributi predefiniti. A tale scopo, usare la funzione [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) con una query di ricerca XML formattata come specificato nell'argomento [formato della query di ricerca di record](record-search-query-format.md) .

Per ulteriori informazioni sull'utilizzo dei record nell'infrastruttura peer, consultare l'argomento [record](records.md) in [utilizzo dell'infrastruttura peer](using-the-peer-infrastructure.md).

## <a name="administration-of-peer-group-records"></a>Amministrazione dei record del gruppo di peer

Quando gli inviti iniziali vengono emessi dal creatore del gruppo peer, è possibile specificare che alcuni membri vengono utilizzati in un ruolo amministrativo ( \_ amministratore del ruolo del gruppo peer \_ \_ ) ogni volta che vengono generate nuove credenziali per l'utente (tramite [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) o [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)). Un amministratore ha la possibilità di aggiungere, eliminare e aggiornare direttamente tutti i record del gruppo peer. Viceversa, un membro del gruppo peer con il suo ruolo impostato sul membro del **\_ \_ ruolo \_** del gruppo peer o **sul \_ ruolo del gruppo peer che invita il \_ \_ \_ membro** può solo aggiungere, aggiornare ed eliminare i propri record.

Per impostazione predefinita, l'autore ha il ruolo di amministratore.

Per aggiornare un record, ottenere il record con [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) o [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords), apportare le modifiche e passare il record aggiornato a [**PeerGroupUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord).

Per eliminare un record, passare l'ID record da eliminare a [**PeerGroupDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord).

Per aggiungere un record, creare una nuova struttura di [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) e popolare i campi seguenti:

-   **dwSize**. Questo campo contiene il valore **sizeof**([**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record)).
-   **ftExpiration**. Questo campo contiene la data e l'ora di scadenza di questo record, espresso in tempo peer come struttura **FILETIME** .
-   **digitare**. Questo campo contiene un valore **GUID** che identifica il tipo di record per l'applicazione. Se questo tipo è personalizzato per l'infrastruttura dell'applicazione, è necessario popolare anche il campo **dati** .

I campi seguenti vengono popolati dall'infrastruttura e verranno ignorati se impostati dall'applicazione:

-   **id**
-   **pwzCreatorId**
-   **pwzLastModifiedById**
-   **ftCreation**
-   **ftLastModified**
-   **securityData**

I campi rimanenti sono facoltativi. Per aggiungere il nuovo record al gruppo peer, passarlo a [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord).

## <a name="importing-and-exporting-records"></a>Importazione ed esportazione di record

I record di gruppi peer-to-peer vengono gestiti localmente come database. Per salvare uno snapshot corrente del database di record del gruppo peer in un file locale, chiamare [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)e passare l'handle al gruppo peer. Questo file può quindi essere trasportato in un altro computer o applicazione, che può estrarre e usare questo database di record chiamando [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase).

 

 



