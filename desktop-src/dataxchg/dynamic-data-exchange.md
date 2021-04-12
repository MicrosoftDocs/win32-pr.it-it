---
title: Dynamic Data Exchange
description: In questa sezione vengono fornite le linee guida per l'implementazione di Dynamic Data Exchange per le applicazioni che non possono utilizzare la libreria di gestione Dynamic Data Exchange (DDEML).
ms.assetid: vs|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange.htm
keywords:
- Dynamic Data Exchange (DDE), informazioni
- DDE (Dynamic Data Exchange), informazioni
- scambio di dati, Dynamic Data Exchange (DDE)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d5fa52078c2fa1d2e67a74d019535c801c4c96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330332"
---
# <a name="dynamic-data-exchange"></a>Dynamic Data Exchange

In questa sezione vengono fornite le linee guida per l'implementazione di Dynamic Data Exchange per le applicazioni che non possono utilizzare la libreria di gestione Dynamic Data Exchange (DDEML). Per ulteriori informazioni su DDEML, vedere [Dynamic Data Exchange Management Library](dynamic-data-exchange-management-library.md).

### <a name="overviews"></a>Cenni preliminari



| Nome                                                           | Descrizione                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------|
| [Informazioni su Dynamic Data Exchange](about-dynamic-data-exchange.md) | Viene illustrato il trasferimento dei dati tra le applicazioni.<br/>       |
| [Utilizzo di Dynamic Data Exchange](using-dynamic-data-exchange.md) | Fornisce esempi di codice relativi allo scambio dinamico di dati.<br/> |
| [Riferimento a DDE](dynamic-data-exchange-reference.md)           | Riferimento all'API.<br/>                                      |



 

### <a name="dde-functions"></a>Funzioni DDE



| Nome                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice)         | Specifica la qualità del servizio (QOS) di un'applicazione di Dynamic Data Exchange non elaborata (DDE) per le future conversazioni DDE avviate. Il QOS specificato si applica a tutte le conversazioni avviate durante l'esecuzione di tali impostazioni. La qualità del servizio della conversazione DDE dura per la durata della conversazione; le chiamate alla funzione [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) durante una conversazione non influiscono sul QoS della conversazione. <br/> |
| [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)                           | Libera la memoria specificata dal parametro *lParam* di un messaggio DDE inviato. Un'applicazione che riceve un messaggio DDE inviato deve chiamare questa funzione dopo che ha utilizzato la funzione [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) per decomprimere il valore *lParam* . <br/>                                                                                                                                                                                                     |
| [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) | Consente a un'applicazione server DDE di rappresentare il contesto di sicurezza di un'applicazione client DDE. Questa operazione protegge i dati del server protetto da client DDE non autorizzati. <br/>                                                                                                                                                                                                                                                                                                      |
| [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)                           | Comprime un valore di *lParam* DDE in una struttura interna utilizzata per la condivisione di dati DDE tra processi.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)                         | Consente a un'applicazione di riutilizzare un parametro *lParam* DDE compresso, anziché allocare un nuovo *lParam* compresso. L'utilizzo di questa funzione riduce le riallocazioni per le applicazioni che passano messaggi DDE compressi. <br/>                                                                                                                                                                                                                                                          |
| [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)                       | Decomprime un valore *lParam* DDE ricevuto da un messaggio DDE inviato. <br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="dde-messages"></a>Messaggi DDE



| Nome                                         | Descrizione                                                                                                                                                                                                                                                                                      |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_avvio DDE \_ WM**](wm-dde-initiate.md) | Avvia una conversazione con un'applicazione server che risponde ai nomi di applicazione e di argomento specificati. Al momento della ricezione di questo messaggio, è previsto che tutte le applicazioni server con nomi corrispondenti all'applicazione specificata e che supportano l'argomento specificato lo riconosca.<br/> |



 

### <a name="dde-notifications"></a>Notifiche DDE



| Nome                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ACK DDE \_ WM**](wm-dde-ack.md)             | Nnotifies un'applicazione DDE della ricezione e dell'elaborazione dei messaggi seguenti: [**WM \_ DDE \_ poke**](wm-dde-poke.md), [**WM \_ DDE \_ Execute**](wm-dde-execute.md), [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM \_ DDE \_ Advise**](wm-dde-advise.md), [**WM \_ DDE \_ Unadvise**](wm-dde-unadvise.md), [**WM \_ DDE \_ Initiation**](wm-dde-initiate.md)o [**WM \_ DDE \_ Request**](wm-dde-request.md) (in alcuni casi). <br/> |
| [**\_avviso DDE di WM \_**](wm-dde-advise.md)       | Un'applicazione client DDE invia il messaggio di [**\_ \_ notifica DDE di WM**](wm-dde-advise.md) a un'applicazione server DDE per richiedere al server di fornire un aggiornamento per un elemento di dati ogni volta che l'elemento viene modificato. <br/>                                                                                                                                                                                                              |
| [**\_dati DDE di WM \_**](wm-dde-data.md)           | Un'applicazione server DDE inserisce un messaggio di [**\_ \_ dati DDE di WM**](wm-dde-data.md) in un'applicazione client DDE per passare un elemento dati al client o per notificare al client la disponibilità di un elemento di dati. <br/>                                                                                                                                                                                                           |
| [**esecuzione di WM \_ DDE \_**](wm-dde-execute.md)     | Un'applicazione client DDE invia un messaggio di [**\_ \_ esecuzione DDE di WM**](wm-dde-execute.md) a un'applicazione server DDE per inviare una stringa al server da elaborare come una serie di comandi. Si prevede che l'applicazione server invii un [**messaggio \_ \_ ACK DDE WM**](wm-dde-ack.md) in risposta. <br/>                                                                                                                      |
| [**\_poke DDE \_ WM**](wm-dde-poke.md)           | Un'applicazione client DDE invia un [**messaggio \_ \_ poke DDE di WM**](wm-dde-poke.md) a un'applicazione server DDE. Un client utilizza questo messaggio per richiedere al server di accettare un elemento di dati non richiesto. Si prevede che il server risponda con un messaggio di [**\_ \_ ACK DDE WM**](wm-dde-ack.md) che indica se l'elemento di dati è stato accettato. <br/>                                                                                   |
| [**\_richiesta DDE \_ WM**](wm-dde-request.md)     | Un'applicazione client DDE invia un messaggio di [**\_ \_ richiesta DDE di WM**](wm-dde-request.md) a un'applicazione server DDE per richiedere il valore di un elemento di dati. <br/>                                                                                                                                                                                                                                                              |
| [**\_ \_ terminazione DDE WM**](wm-dde-terminate.md) | Un'applicazione DDE (client o server) Invia un messaggio di [**\_ \_ terminazione DDE WM**](wm-dde-terminate.md) per terminare una conversazione. <br/>                                                                                                                                                                                                                                                                                  |
| [**\_Unadvise DDE WM \_**](wm-dde-unadvise.md)   | Un'applicazione client DDE invia un messaggio di avviso [**\_ \_ DDE di WM**](wm-dde-unadvise.md) per informare un'applicazione server DDE che l'elemento specificato o un particolare formato degli Appunti per l'elemento non deve più essere aggiornato. Questa operazione interrompe il collegamento dati caldo o attivo per l'elemento specificato. <br/>                                                                                                                     |



 

### <a name="dde-structures"></a>Strutture DDE



| Nome                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)       | Contiene i flag di stato che un'applicazione DDE passa al proprio partner come parte del messaggio [**\_ \_ ACK DDE WM**](wm-dde-ack.md) . I flag forniscono informazioni dettagliate sulla risposta dell'applicazione ai messaggi [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM \_ DDE \_ poke**](wm-dde-poke.md), [**WM \_ DDE \_ Execute**](wm-dde-execute.md), [**WM \_ DDE \_ Advise**](wm-dde-advise.md), [**WM \_ DDE \_ Unadvise**](wm-dde-unadvise.md)e [**WM \_ DDE \_ Request**](wm-dde-request.md). <br/> |
| [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) | Contiene i flag che specificano come un'applicazione server DDE deve inviare i dati a un'applicazione client durante un ciclo di notifica. Un client passa un handle a una struttura [**DDEAdvise**](/windows/desktop/api/Dde/ns-dde-ddeadvise) a un server come parte di un messaggio di [**\_ \_ avviso DDE di WM**](wm-dde-advise.md) . <br/>                                                                                                                                                                                               |
| [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)     | Contiene i dati e le informazioni sui dati inviati come parte di un messaggio di [**\_ \_ dati DDE di WM**](wm-dde-data.md) . <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)     | Contiene i dati e le informazioni sui dati inviati come parte di un messaggio [**\_ \_ poke DDE di WM**](wm-dde-poke.md) . <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)     | Contiene un nome di servizio e un nome di argomento DDE. Un'applicazione server DDE può utilizzare questa struttura durante una transazione [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) per enumerare le coppie di argomenti di servizio supportate. <br/>                                                                                                                                                                                                                                                   |



 

 

 





