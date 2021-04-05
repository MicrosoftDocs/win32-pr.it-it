---
title: Uso dell'API server di Servizi di distribuzione Windows
description: Negli ambienti in cui non è possibile usare la soluzione standard di servizi di distribuzione Windows (WDS), il server WDS espone un'API che consente agli sviluppatori di scrivere plug-in, detti provider, per gestire le richieste PXE (Preboot Execution Environment).
ms.assetid: 5e25654a-33c6-4c0f-acc3-e938d1f4a4e7
keywords:
- Servizi di distribuzione Windows servizi di distribuzione Windows, utilizzo dell'API server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3634dffa73eddc9b5db92be6bc807cccbc5248f
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "103724258"
---
# <a name="using-the-windows-deployment-services-server-api"></a>Uso dell'API server di Servizi di distribuzione Windows

Negli ambienti in cui non è possibile usare la soluzione standard di servizi di distribuzione Windows (WDS), il server WDS espone un'API che consente agli sviluppatori di scrivere plug-in, detti provider, per gestire le richieste PXE (Preboot Execution Environment). Gli sviluppatori devono attenersi alle linee guida seguenti per la scrittura di provider PXE per WDS.

## <a name="install-the-wds-role-on-the-server"></a>Installare il ruolo WDS nel server

-   Servizi di distribuzione Windows (WDS) è la versione modificata di servizi di installazione remota (RIS), per implementare i provider e il server PXE WDS è necessario il ruolo server WDS.
-   WDS sostituisce RIS come componente standard a partire da Windows Server 2008 e Windows Server 2003 con Service Pack 2 (SP2).
-   È necessario aggiornare il server RIS a WDS in Windows Server 2003 con Service Pack 1 (SP1). È possibile installare il ruolo server WDS con [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="register-providers"></a>Registra provider

-   Registrare la libreria di collegamento dinamico (DLL) del provider durante l'installazione e inserire il provider nell'elenco ordinato di provider registrati.
    > [!Note]  
    > Quando si installa un provider nuovo o modificato, sarà necessario riavviare il servizio PXE WDS per rendere effettive le modifiche.

     

-   Utilizzare la funzione [**PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister) per registrare il provider e aggiungerlo all'elenco. Utilizzare la funzione [**PxeProviderUnRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderunregister) per annullare la registrazione di un provider registrato e rimuoverlo dall'elenco.
-   Consente di specificare la sequenza del provider nell'elenco ordinato. L'indice di un provider nell'elenco non può essere garantito perché un altro provider può essere registrato in un secondo momento. Per inserire il provider nell'elenco prima o dopo un altro provider registrato, utilizzare innanzitutto la funzione [**PxeProviderQueryIndex**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex) per ottenere l'indice del provider registrato, quindi registrare il nuovo provider specificando un valore di indice maggiore o minore.
-   L'installazione può archiviare le informazioni di configurazione del provider nella chiave del registro di sistema restituita quando il provider è registrato. L'indirizzo della chiave del registro di sistema viene ricevuto dal *phProviderKey* di [**PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister). Il provider riceve un handle per la stessa chiave del parametro *hProviderKey* al callback [*PxeProviderInitialize*](pxeproviderinitialize.md) . Il provider deve archiviare l'indirizzo della chiave.
-   Installare sempre la libreria di collegamento dinamico (DLL) del provider nella cartella programmi del server.

## <a name="initialize"></a>Inizializzare

-   Includere una DLL che esporta la funzione di callback [*PxeProviderInitialize*](pxeproviderinitialize.md) nel provider. Ogni provider richiede un callback *PxeProviderInitialize* . Quando WDS carica un provider, chiama la funzione *PxeProviderInitialize* del provider e passa un handle alla stessa chiave usata per archiviare le informazioni di configurazione durante la registrazione del provider.
-   Quando il callback [*PxeProviderInitialize*](pxeproviderinitialize.md) restituisce e ha esito positivo, il provider deve essere completamente inizializzato e pronto per l'elaborazione delle richieste.
-   Registrare ogni callback nel provider durante l'elaborazione della funzione [*PxeProviderInitialize*](pxeproviderinitialize.md) . I callback devono essere registrati con la funzione [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) .
-   Inizializzare tutte le risorse interne del provider nell'elaborazione della relativa funzione [*PxeProviderInitialize*](pxeproviderinitialize.md) .

## <a name="shutdown"></a>Arresta

-   Implementare il callback [*PxeProviderShutdown*](pxeprovidershutdown.md) . Ogni provider deve avere un callback *PxeProviderShutdown*.
-   La funzione di callback [*PxeProviderShutdown*](pxeprovidershutdown.md) dovrebbe arrestare completamente il provider e rilasciare tutte le risorse.
-   Una volta restituito il callback [*PxeProviderShutdown*](pxeprovidershutdown.md) , l'handle *hProvider* passato alla funzione [*PxeProviderInitialize*](pxeproviderinitialize.md) non è più valido e non deve essere usato per chiamare WDS.
-   Registrare il callback [*PxeProviderShutdown*](pxeprovidershutdown.md) chiamando la funzione [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) con l' **\_ \_ arresto del callback PXE** durante l'elaborazione del callback [*PxeProviderInitialize*](pxeproviderinitialize.md) . Non chiamare il callback *PxeProviderShutdown* se la funzione *PxeProviderInitialize* ha esito negativo.

## <a name="handle-request-packet"></a>Gestisci pacchetto di richiesta

Implementare il callback [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) per il provider. Ogni provider deve avere un callback *PxeProviderRecvRequest* . Quando WDS riceve una richiesta, chiama il callback *PxeProviderRecvRequest* per il primo provider nell'elenco dei provider registrati.

-   Se il provider elaborerà la richiesta in modo sincrono, la funzione [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) dovrebbe restituire un valore **Error \_ Success**. Se e solo se il provider elaborerà la richiesta in modo asincrono, il callback di *PxeProviderRecvRequest* deve restituire l' **errore \_ io \_ in sospeso** e chiamare la funzione [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) quando la richiesta è stata elaborata.
-   Il callback [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) e la funzione [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) restituisce l'indirizzo di un'enumerazione dell' **\_ \_ azione di avvio PXE** che descrive l'azione eseguita dal provider per gestire la richiesta.

    Esistono quattro modi per gestire una richiesta da un provider:

    -   Il provider risponde al client con un pacchetto di risposta DHCP standard che contiene un percorso del programma di avvio di rete. La restituzione del valore **\_ \_ avvio di PXE BA** per l'enumerazione significa che il provider ha elaborato correttamente il pacchetto di richiesta e ha completato la richiesta inviando un pacchetto di risposta chiamando le funzioni [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) e [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) .
    -   Il provider risponde al client con un pacchetto di risposta personalizzato che non è conforme a DHCP. La restituzione del valore **\_ \_ personalizzato PXE BA** per l'enumerazione significa che il provider ha elaborato correttamente il pacchetto di richiesta e ha completato la richiesta inviando un pacchetto di risposta personalizzato chiamando le funzioni [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) e [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) .
    -   Il provider determina che la richiesta deve essere ignorata. La restituzione del valore di **\_ \_ Ignore PXE** per l'enumerazione significa che il provider ha rilasciato tutte le risorse associate alla richiesta e la richiesta non viene passata al provider successivo nell'elenco dei provider registrati. I provider possono usare questa opzione se rilevano che un pacchetto di richiesta non è valido.
    -   Il provider rifiuta di servire la richiesta. La restituzione del valore di **\_ \_ rifiuto BA PXE** per l'enumerazione indica al sistema di passare la richiesta al provider successivo nell'elenco dei provider registrati. Se questo è l'ultimo provider nell'elenco, rilascia tutte le risorse associate alla richiesta e la richiesta viene ignorata.
    -   Registrare il callback [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) chiamando la funzione [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) con la **\_ richiesta di callback PXE \_ ricezione \_** durante l'elaborazione del callback [*PxeProviderInitialize*](pxeproviderinitialize.md) .

## <a name="generate-response-packet"></a>Genera pacchetto di risposta

-   Usare l'API per scrivere i provider per gestire la richiesta DHCP e generare pacchetti di risposta.
-   La funzione [**PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) specifica gli attributi utilizzati dal provider per filtrare i pacchetti. Gli attributi del provider possono essere specificati in modo che il provider veda tutti i pacchetti, il provider vede solo i pacchetti DHCP oppure il provider vede solo i pacchetti DHCP che specificano l'opzione identificatore classe fornitore DHCP (60) come "PXEClient".
-   La funzione [**PxeDhcpIsValid**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpisvalid) verifica che un pacchetto sia un pacchetto DHCP valido. I provider possono utilizzare la funzione **PxeDhcpIsValid** per verificare se un pacchetto del client è un pacchetto DHCP quando il filtro impostato con la funzione [**PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) è impostato in modo da ricevere tutti i pacchetti per determinare se un pacchetto specificato è un pacchetto DHCP valido.
-   La funzione [**PxeDhcpInitialize**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpinitialize) Inizializza un pacchetto di risposta come pacchetto di risposta DHCP basato sulle informazioni contenute in un pacchetto ricevuto dal client. La funzione [*PxeProviderInitialize*](pxeproviderinitialize.md) accetta l'indirizzo di un pacchetto DHCP valido ricevuto dal client nel callback [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) . La funzione **PxeDhcpInitialize** accetta un puntatore a un pacchetto di risposta allocato con la funzione [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) .
-   La funzione [**PxeDhcpGetOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue) recupera un valore di opzione da un pacchetto DHCP. La funzione [**PxeDhcpGetVendorOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) recupera un valore di opzione dal campo informazioni specifiche del fornitore (43) di un pacchetto DHCP.
-   Il provider può quindi popolare il pacchetto di risposta con le informazioni e usare la funzione [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) per inviare il pacchetto di risposta al client. La funzione [**PxeDhcpAppendOption**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpappendoption) aggiunge un'opzione DHCP al pacchetto di risposta.
-   Un provider che risponde alle richieste client inviando un pacchetto deve allocare il pacchetto di risposta usando la funzione [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) . Il provider può quindi popolare il pacchetto di risposta con le informazioni e usare la funzione [**PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) per inviare il pacchetto di risposta al client.
-   Quando la memoria allocata non è più necessaria, il provider deve rilasciarla utilizzando la funzione [**PxePacketFree**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketfree) .

## <a name="enumerate-registered-providers"></a>Enumera provider registrati

-   Usare l'API per scrivere i provider che enumerano e controllano altri provider registrati nell'elenco.
-   La funzione [**PxeGetServerInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxegetserverinfo) restituisce informazioni sul server PXE. La funzione **PxeGetServerInfo** restituisce un valore **bool** che indica se la traccia è abilitata per il server. **True** indica che la traccia è abilitata.
-   La funzione [**PxeProviderEnumFirst**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) avvia un provider enumerationof nell'elenco dei provider registrati. La funzione **PxeProviderEnumFirst** avvia l'enumerazione e restituisce l'indirizzo dell'handle da usare quando si chiama la funzione [**PxeProviderEnumNext**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) . La funzione **PxeProviderEnumNext** restituisce una struttura del [**\_ provider PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider) che contiene le informazioni sul provider. La funzione [**PxeProviderFreeInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo) libera la memoria allocata per la struttura del **\_ provider PXE** tramite la funzione **PxeProviderEnumNext** . La funzione [**PxeProviderEnumClose**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumclose) chiude l'enumerazione dei provider nell'elenco dei provider registrati.

## <a name="handle-service-control-codes"></a>Gestire i codici di controllo del servizio

-   Quando viene ricevuto un messaggio di controllo del servizio, WDS chiama il callback [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) .
-   Il provider può definire una funzione di callback [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) per gestire i messaggi di controllo del servizio.
-   Registrare il callback [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) chiamando la funzione [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) con il **\_ \_ \_ controllo del servizio di callback PXE** durante l'elaborazione del callback [*PxeProviderInitialize*](pxeproviderinitialize.md) .

## <a name="add-trace-entries-to-pxe-log"></a>Aggiungere voci di traccia al log PXE

-   La funzione [**PxeTrace**](/windows/win32/api/WdsPxe/nf-wdspxe-pxetrace) aggiunge una voce di traccia al log PXE. WDSPXE fornisce la traccia per aiutare gli amministratori nella risoluzione dei problemi. I provider possono registrare voci di traccia con livelli di gravità diversi. Gli amministratori possono configurare WDSPXE solo per le voci di log per determinati livelli di gravità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API di servizi di distribuzione Windows](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Uso dell'API client di Servizi di distribuzione Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 




