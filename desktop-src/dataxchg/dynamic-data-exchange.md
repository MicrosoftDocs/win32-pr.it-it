---
title: Dynamic Data Exchange
description: In questa sezione vengono fornite linee guida per l'implementazione dello scambio di dati dinamico per le applicazioni che non possono usare Dynamic Data Exchange Management Library (DDEML).
ms.assetid: vs|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange.htm
keywords:
- Dynamic Data Exchange (DDE),about
- DDE (Dynamic Data Exchange),about
- scambio di dati, Dynamic Data Exchange (DDE)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db58f1027f0dfaacf28c4b2ec8d4208747929b0d40ca55d7d377831777f78a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678041"
---
# <a name="dynamic-data-exchange"></a>Dynamic Data Exchange

In questa sezione vengono fornite linee guida per l'implementazione dello scambio di dati dinamico per le applicazioni che non possono usare Dynamic Data Exchange Management Library (DDEML). Per altre informazioni su DDEML, vedere Dynamic Data Exchange [Management Library.](dynamic-data-exchange-management-library.md)

### <a name="overviews"></a>Cenni preliminari



| Nome                                                           | Descrizione                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------|
| [Informazioni Dynamic Data Exchange](about-dynamic-data-exchange.md) | Viene illustrato il trasferimento di dati tra applicazioni.<br/>       |
| [Uso di Dynamic Data Exchange](using-dynamic-data-exchange.md) | Fornisce esempi di codice relativi a Dynamic Data Exchange.<br/> |
| [Informazioni di riferimento su DDE](dynamic-data-exchange-reference.md)           | Informazioni di riferimento sulle API.<br/>                                      |



 

### <a name="dde-functions"></a>Funzioni DDE



| Nome                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice)         | Specifica la qualità del servizio (QOS) che un'applicazione Dynamic Data Exchange (DDE) non elaborata desidera per le conversazioni DDE future avviate. L'oggetto QOS specificato si applica a tutte le conversazioni avviate mentre sono presenti tali impostazioni. La qualità del servizio di una conversazione DDE dura per la durata della conversazione; Le chiamate alla [**funzione DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) durante una conversazione non influiscono sul QOS della conversazione. <br/> |
| [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)                           | Libera la memoria specificata dal *parametro lParam* di un messaggio DDE inviato. Un'applicazione che riceve un messaggio DDE inviato deve chiamare questa funzione dopo aver usato la funzione [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) per decomprimere il *valore lParam.* <br/>                                                                                                                                                                                                     |
| [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) | Consente a un'applicazione server DDE di rappresentare il contesto di sicurezza di un'applicazione client DDE. Ciò consente di proteggere i dati del server da client DDE non autorizzati. <br/>                                                                                                                                                                                                                                                                                                      |
| [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)                           | Complica un valore *lParam DDE* in una struttura interna usata per la condivisione dei dati DDE tra processi.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)                         | Consente a un'applicazione di riutilizzare un parametro *lParam* DDE di tipo pack, anziché allocare un nuovo *lParam di tipo packed.* L'uso di questa funzione riduce le rilocazioni per le applicazioni che passano messaggi DDE di tipo pack. <br/>                                                                                                                                                                                                                                                          |
| [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)                       | Decomprime un valore *lParam* DDE ricevuto da un messaggio DDE inviato. <br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="dde-messages"></a>Messaggi DDE



| Nome                                         | Descrizione                                                                                                                                                                                                                                                                                      |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md) | Avvia una conversazione con un'applicazione server che risponde ai nomi di applicazione e argomento specificati. Quando si riceve questo messaggio, è previsto che tutte le applicazioni server con nomi corrispondenti all'applicazione specificata e che supportano l'argomento specificato lo riconosca.<br/> |



 

### <a name="dde-notifications"></a>Notifiche DDE



| Nome                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DDE \_ ACK**](wm-dde-ack.md)             | Notifica a un'applicazione DDE la ricezione e l'elaborazione dei messaggi seguenti: [**WM \_ DDE \_ POKE,**](wm-dde-poke.md) [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md) [**WM \_ DDE \_ DATA,**](wm-dde-data.md) [**WM \_ DDE \_ ADVISE,**](wm-dde-advise.md) [**WM \_ DDE \_ UNADVISE,**](wm-dde-unadvise.md) [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)o [**WM \_ DDE \_ REQUEST**](wm-dde-request.md) (in alcuni casi). <br/> |
| [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)       | Un'applicazione client DDE invia il messaggio [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md) a un'applicazione server DDE per richiedere al server di fornire un aggiornamento per un elemento di dati ogni volta che l'elemento viene modificato. <br/>                                                                                                                                                                                                              |
| [**DATI \_ WM DDE \_**](wm-dde-data.md)           | Un'applicazione server DDE invia un messaggio [**WM \_ DDE \_ DATA**](wm-dde-data.md) a un'applicazione client DDE per passare un elemento di dati al client o per notificare al client la disponibilità di un elemento di dati. <br/>                                                                                                                                                                                                           |
| [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md)     | Un'applicazione client DDE invia un messaggio [**EXECUTE DI WM \_ DDE \_**](wm-dde-execute.md) a un'applicazione server DDE per inviare una stringa al server da elaborare come una serie di comandi. L'applicazione server deve inviare un [**messaggio \_ WM DDE \_ ACK**](wm-dde-ack.md) in risposta. <br/>                                                                                                                      |
| [**WM \_ DDE \_ POKE**](wm-dde-poke.md)           | Un'applicazione client DDE invia un [**messaggio \_ \_ POKE WM DDE**](wm-dde-poke.md) a un'applicazione server DDE. Un client utilizza questo messaggio per richiedere al server di accettare un elemento di dati non richiesto. Il server deve rispondere con un messaggio [**WM \_ DDE \_ ACK**](wm-dde-ack.md) che indica se ha accettato l'elemento di dati. <br/>                                                                                   |
| [**RICHIESTA \_ WM DDE \_**](wm-dde-request.md)     | Un'applicazione client DDE invia un messaggio [**WM \_ DDE \_ REQUEST**](wm-dde-request.md) a un'applicazione server DDE per richiedere il valore di un elemento di dati. <br/>                                                                                                                                                                                                                                                              |
| [**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) | Un'applicazione DDE (client o server) invia un [**messaggio WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) per terminare una conversazione. <br/>                                                                                                                                                                                                                                                                                  |
| [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)   | Un'applicazione client DDE invia un messaggio [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md) per informare un'applicazione server DDE che l'elemento specificato o un particolare formato degli Appunti per l'elemento non deve più essere aggiornato. In questo modo viene terminato il collegamento dati ad accesso più caldo per l'elemento specificato. <br/>                                                                                                                     |



 

### <a name="dde-structures"></a>Strutture DDE



| Nome                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)       | Contiene i flag di stato che un'applicazione DDE passa al partner come parte del messaggio [**\_ WM DDE \_ ACK.**](wm-dde-ack.md) I flag forniscono informazioni dettagliate sulla risposta dell'applicazione ai messaggi [**WM \_ DDE \_ DATA,**](wm-dde-data.md) [**WM \_ DDE \_ POKE,**](wm-dde-poke.md) [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md) [**WM \_ DDE \_ ADVISE,**](wm-dde-advise.md) [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)e [**WM \_ DDE \_ REQUEST.**](wm-dde-request.md) <br/> |
| [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) | Contiene flag che specificano come un'applicazione server DDE deve inviare dati a un'applicazione client durante un ciclo di consulenza. Un client passa un handle a [**una struttura DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) a un server come parte di un [**messaggio WM \_ DDE \_ ADVISE.**](wm-dde-advise.md) <br/>                                                                                                                                                                                               |
| [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)     | Contiene i dati e le informazioni sui dati inviati come parte di un messaggio [**WM \_ DDE \_ DATA.**](wm-dde-data.md) <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)     | Contiene i dati e le informazioni sui dati inviati come parte di un messaggio [**\_ \_ POKE WM DDE.**](wm-dde-poke.md) <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)     | Contiene un nome di servizio DDE e un nome di argomento. Un'applicazione server DDE può utilizzare questa struttura durante una transazione [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) per enumerare le coppie servizio-argomento supportate. <br/>                                                                                                                                                                                                                                                   |



 

 

 





