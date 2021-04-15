---
title: Come usare l'API client di Connessione Desktop remoto broker
description: L'API client di Connessione Desktop remoto Broker consente ai fornitori di protocolli di terze parti di sfruttare il broker di connessione per accelerare la gestione delle connessioni che usano il protocollo per connettersi alle macchine virtuali o ai server Desktop remoto in una farm.
ms.assetid: 05C2D6CA-C9C5-4783-B196-6A02918046EF
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c931245870cfb72aed54e5aaff24e12d03ddf9e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338878"
---
# <a name="how-to-use-the-remote-desktop-connection-broker-client-api"></a>Come usare l'API client di Connessione Desktop remoto broker

L'API client di Connessione Desktop remoto Broker consente ai fornitori di protocolli di terze parti di sfruttare il broker di connessione per accelerare la gestione delle connessioni che usano il protocollo per connettersi alle macchine virtuali o ai server Desktop remoto in una farm.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-obtain-the-iconnectionbrokerclient-interface"></a>Passaggio 1: ottenere l'interfaccia IConnectionBrokerClient

Quando viene inizializzato il provider dell'applicazione o del protocollo, seguire questa procedura.

1.  Chiamare la funzione [**CBCreateClientInstance**](cbcreateclientinstance.md) per ottenere l'interfaccia [**IConnectionBrokerClient**](iconnectionbrokerclient.md) .
2.  Mantieni l'interfaccia [**IConnectionBrokerClient**](iconnectionbrokerclient.md) finché ti serve.
3.  Quando l'interfaccia [**IConnectionBrokerClient**](iconnectionbrokerclient.md) non è più necessaria, chiamare il metodo [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) .

### <a name="step-2-request-the-target-information"></a>Passaggio 2: richiedere le informazioni di destinazione

Quando il provider di protocollo riceve una richiesta di connessione in ingresso, seguire questa procedura per chiamare il metodo [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) . Questo metodo ottiene, dal gestore della connessione, il server appropriato a cui reindirizzare la connessione.

1.  Creare un evento che può essere segnalato usando [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), o funzione simile, da usare per il parametro *hStatusEvent* .
2.  Allocare memoria per i parametri *pTargetInfo* e *pResult* . Questi blocchi di memoria devono rimanere sul posto finché l'intera sequenza non è completa.
3.  Compilare una struttura [**di \_ \_ informazioni di connessione CB**](cb-connection-info.md) contenente tutte le informazioni sulla connessione in ingresso.
4.  Chiamare il metodo [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) , passando tutti i parametri richiesti. Si tratta di un metodo asincrono che restituirà un'istanza dell'interfaccia [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) .
5.  Attendere l'impostazione dell'evento *hStatusEvent* .
6.  Ogni volta che viene impostato l'evento *hStatusEvent* , chiamare il metodo [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) per determinare lo stato della richiesta.
7.  Quando [**checkStatus**](iconnectionbrokerrequest-checkstatus.md) restituisce **la \_ richiesta di stato CB \_ \_ completata**, i parametri *pTargetInfo* e *pResult* conterranno le informazioni. È possibile interrompere il ciclo di attesa perché il parametro *hStatusEvent* non verrà più usato.
8.  Usare le informazioni nella struttura [**di \_ \_ informazioni di destinazione CB**](cb-target-info.md) rappresentata dal parametro *pTargetInfo* per determinare la posizione in cui reindirizzare la connessione in ingresso.
9.  Rilasciare l'interfaccia [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) .
10. Chiudere l'handle di evento *hStatusEvent* oppure riutilizzarlo per richieste di connessione successive.

 

 