---
title: Uso dell'API server di Servizi di distribuzione Windows
description: Negli ambienti in cui non è possibile usare la soluzione servizi di distribuzione Windows standard (WDS), il server wds espone un'API che consente agli sviluppatori di scrivere plug-in, denominati provider, per gestire le richieste dell'ambiente di esecuzione pre-avvio (PXE).
ms.assetid: 5e25654a-33c6-4c0f-acc3-e938d1f4a4e7
keywords:
- Windows Servizi di Windows distribuzione di , usando l'API server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ce7516e5279fecdfeecfa90edd8e3a0dad265562fa5ea59336367dbe157c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999571"
---
# <a name="using-the-windows-deployment-services-server-api"></a>Uso dell'API server di Servizi di distribuzione Windows

Negli ambienti in cui non è possibile usare la soluzione servizi di distribuzione Windows standard (WDS), il server wds espone un'API che consente agli sviluppatori di scrivere plug-in, denominati provider, per gestire le richieste dell'ambiente di esecuzione pre-avvio (PXE). Gli sviluppatori devono rispettare le linee guida seguenti quando scrivono provider PXE per WDS.

## <a name="install-the-wds-role-on-the-server"></a>Installare il ruolo wds nel server

-   Windows Servizi di distribuzione (WDS) è la versione aggiornata di Servizi di installazione remota (RIS). Per implementare il server e i provider PXE di WDS è necessario il ruolo del server WDS.
-   WDS sostituisce RIS come componente standard a partire da Windows Server 2008 e Windows Server 2003 con Service Pack 2 (SP2).
-   È necessario aggiornare il server RIS a WDS in Windows Server 2003 con Service Pack 1 (SP1). È possibile installare il ruolo del server WDS [con Windows Automated Installation Kit (WAIK).](https://www.microsoft.com/download/details.aspx?id=10333)

## <a name="register-providers"></a>Registrare i provider

-   Registrare la libreria a collegamento dinamico (DLL) del provider durante l'installazione e inserire il provider nell'elenco ordinato dei provider registrati.
    > [!Note]  
    > Quando si installa un provider nuovo o modificato, è necessario riavviare il servizio WDS PXE per l'applicazione delle modifiche.

     

-   Usare la [**funzione PxeProviderRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister) per registrare il provider e aggiungerlo all'elenco. Usare la [**funzione PxeProviderUnRegister**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderunregister) per annullare la registrazione di un provider registrato e rimuoverlo dall'elenco.
-   Specificare la sequenza del provider nell'elenco ordinato. Non è possibile garantire l'indice di un provider nell'elenco perché un altro provider potrebbe essere registrato in un secondo momento prima di esso. Per inserire il provider nell'elenco prima o dopo un altro provider registrato, usare prima la funzione [**PxeProviderQueryIndex**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex) per ottenere l'indice del provider registrato e quindi registrare il nuovo provider specificando un valore di indice maggiore o minore.
-   L'installazione può archiviare le informazioni di configurazione del provider nella chiave del Registro di sistema restituita quando il provider viene registrato. L'indirizzo della chiave del Registro di sistema viene ricevuto dalla *chiave phProviderKey* di [**PxeProviderRegister.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderregister) Il provider riceve un handle per questa stessa chiave del parametro *hProviderKey* per il callback [*PxeProviderInitialize.*](pxeproviderinitialize.md) Il provider deve archiviare l'indirizzo di questa chiave.
-   Installare sempre la libreria a collegamento dinamico (DLL) del provider nella cartella Programmi del server.

## <a name="initialize"></a>Inizializzare

-   Includere una DLL che esporta la funzione di callback [*PxeProviderInitialize*](pxeproviderinitialize.md) nel provider. Ogni provider richiede un callback *PxeProviderInitialize.* Quando WDS carica un provider, chiama la funzione *PxeProviderInitialize* del provider e passa un handle alla stessa chiave usata per archiviare le informazioni di configurazione durante la registrazione del provider.
-   Quando il callback [*PxeProviderInitialize*](pxeproviderinitialize.md) restituisce e ha esito positivo, il provider deve essere completamente inizializzato e pronto per elaborare le richieste.
-   Registrare ogni callback nel provider durante l'elaborazione [*della funzione PxeProviderInitialize.*](pxeproviderinitialize.md) I callback devono essere registrati con [**la funzione PxeRegisterCallback.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback)
-   Inizializzare tutte le risorse interne del provider all'interno dell'elaborazione della relativa [*funzione PxeProviderInitialize.*](pxeproviderinitialize.md)

## <a name="shutdown"></a>Arresta

-   Implementare il callback [*PxeProviderShutdown.*](pxeprovidershutdown.md) Ogni provider deve avere un callback *PxeProviderShutdown.*
-   La funzione di callback [*PxeProviderShutdown*](pxeprovidershutdown.md) deve arrestare completamente il provider e rilasciare tutte le relative risorse.
-   Al termine del callback [*PxeProviderShutdown,*](pxeprovidershutdown.md) l'handle *hProvider* passato alla funzione [*PxeProviderInitialize*](pxeproviderinitialize.md) non è più valido e non deve essere usato per chiamare WDS.
-   Registrare il callback [*PxeProviderShutdown*](pxeprovidershutdown.md) chiamando la funzione [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) con **PXE \_ CALLBACK \_ SHUTDOWN** durante l'elaborazione del callback [*PxeProviderInitialize.*](pxeproviderinitialize.md) Non chiamare il callback *PxeProviderShutdown* se la *funzione PxeProviderInitialize* ha esito negativo.

## <a name="handle-request-packet"></a>Gestire il pacchetto di richiesta

Implementare il callback [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) per il provider. Ogni provider deve avere un callback *PxeProviderRecvRequest.* Quando WDS riceve una richiesta, chiama il callback *PxeProviderRecvRequest* per il primo provider nell'elenco di provider registrati.

-   Se il provider eelaborare la richiesta in modo sincrono, la [*funzione PxeProviderRecvRequest*](pxeproviderrecvrequest.md) deve restituire il valore **ERROR \_ SUCCESS.** Se e solo se il provider eelaborare la richiesta in modo asincrono, il callback *PxeProviderRecvRequest* deve restituire **ERROR IO \_ \_ PENDING** e chiamare la funzione [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) dopo l'elaborazione della richiesta.
-   Il callback [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) e la funzione [**PxeAsyncRecvDone**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) restituisce l'indirizzo di un'enumerazione **BOOT \_ \_ ACTION PXE** che descrive l'azione eseguita dal provider per gestire la richiesta.

    Un provider può gestire una richiesta in quattro modi:

    -   Il provider risponde al client con un pacchetto di risposta DHCP standard che contiene un percorso al programma di avvio di rete. La restituzione del valore **\_ \_ NBP** della ba PXE per l'enumerazione significa che il provider ha elaborato correttamente il pacchetto della richiesta e ha completato la richiesta inviando un pacchetto di risposta chiamando le funzioni [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) e [**PxeSendReply.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply)
    -   Il provider risponde al client con un pacchetto di risposta personalizzato non conforme a DHCP. La restituzione del valore **PXE \_ BA \_ CUSTOM** per l'enumerazione significa che il provider ha elaborato correttamente il pacchetto della richiesta e ha completato la richiesta inviando un pacchetto di risposta personalizzato chiamando le funzioni [**PxePacketAllocate**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) e [**PxeSendReply.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply)
    -   Il provider determina che la richiesta deve essere ignorata. La restituzione del valore **IGNORE di tipo BA PXE \_ \_** per l'enumerazione indica che il provider ha rilasciato tutte le risorse associate alla richiesta e la richiesta non viene passata al provider successivo nell'elenco dei provider registrati. I provider possono usare questa opzione se rilevano che un pacchetto di richiesta non è valido.
    -   Il provider rifiuta di eseguire la richiesta. La restituzione del valore REJECT della ba **PXE \_ \_** per l'enumerazione indica al sistema di passare la richiesta al provider successivo nell'elenco dei provider registrati. Se si tratta dell'ultimo provider nell'elenco, vengono rilasciate tutte le risorse associate alla richiesta e la richiesta viene ignorata.
    -   Registrare il callback [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md) chiamando la funzione [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) con **PXE \_ CALLBACK \_ RECV \_ REQUEST** durante l'elaborazione del callback [*PxeProviderInitialize.*](pxeproviderinitialize.md)

## <a name="generate-response-packet"></a>Genera pacchetto di risposta

-   Usare l'API per scrivere provider per gestire le richieste DHCP e generare pacchetti di risposta.
-   La [**funzione PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) specifica gli attributi usati dal provider per filtrare i pacchetti. Gli attributi del provider possono essere specificati in modo che il provider possa visualizzare tutti i pacchetti, che il provider veda solo i pacchetti DHCP oppure che il provider veda solo i pacchetti DHCP che specificano l'opzione DHCP Vendor Class Identifier (60) come "PXEClient".
-   La [**funzione PxeDhcpIsValid**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpisvalid) verifica che un pacchetto sia un pacchetto DHCP valido. I provider possono usare la funzione **PxeDhcpIsValid** per verificare se un pacchetto dal client è un pacchetto DHCP quando il set di filtri con la funzione [**PxeProviderSetAttribute**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) è impostato per ricevere tutti i pacchetti per determinare se un pacchetto specificato è un pacchetto DHCP valido.
-   La [**funzione PxeDhcpInitialize**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpinitialize) inizializza un pacchetto di risposta come pacchetto di risposta DHCP basato sulle informazioni contenute in un pacchetto ricevuto dal client. La [*funzione PxeProviderInitialize*](pxeproviderinitialize.md) accetta l'indirizzo di un pacchetto DHCP valido ricevuto dal client nel callback [*PxeProviderRecvRequest.*](pxeproviderrecvrequest.md) La **funzione PxeDhcpInitialize** accetta un puntatore a un pacchetto di risposta allocato con [**la funzione PxePacketAllocate.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate)
-   La [**funzione PxeDhcpGetOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue) recupera un valore di opzione da un pacchetto DHCP. La [**funzione PxeDhcpGetVendorOptionValue**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) recupera un valore di opzione dal campo Informazioni specifiche del fornitore (43) di un pacchetto DHCP.
-   Il provider può quindi popolare il pacchetto di risposta con informazioni e usare la [**funzione PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) per inviare il pacchetto di risposta al client. La [**funzione PxeDhcpAppendOption**](/windows/win32/api/WdsPxe/nf-wdspxe-pxedhcpappendoption) aggiunge un'opzione DHCP al pacchetto di risposta.
-   Un provider che risponde alle richieste client inviando un pacchetto deve allocare il pacchetto di risposta [**usando la funzione PxePacketAllocate.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketallocate) Il provider può quindi popolare il pacchetto di risposta con informazioni e usare la [**funzione PxeSendReply**](/windows/win32/api/WdsPxe/nf-wdspxe-pxesendreply) per inviare il pacchetto di risposta al client.
-   Quando la memoria allocata non è più necessaria, il provider deve rilasciarla usando la [**funzione PxePacketFree.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxepacketfree)

## <a name="enumerate-registered-providers"></a>Enumerare i provider registrati

-   Usare l'API per scrivere provider che enumerano e controllano altri provider registrati nell'elenco.
-   La [**funzione PxeGetServerInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxegetserverinfo) restituisce informazioni sul server PXE. La **funzione PxeGetServerInfo** restituisce un **valore BOOL** che indica se la traccia è abilitata per il server. **TRUE** indica che la traccia è abilitata.
-   La [**funzione PxeProviderEnumFirst**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) avvia un'enumerazione dei provider nell'elenco dei provider registrati. La **funzione PxeProviderEnumFirst** avvia l'enumerazione e restituisce l'indirizzo dell'handle da usare quando si chiama la [**funzione PxeProviderEnumNext.**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) La **funzione PxeProviderEnumNext** restituisce una [**struttura PXE \_ PROVIDER**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider) contenente le informazioni sul provider. La [**funzione PxeProviderFreeInfo**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo) libera la memoria allocata per la struttura **PXE \_ PROVIDER** dalla **funzione PxeProviderEnumNext.** La [**funzione PxeProviderEnumClose**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeproviderenumclose) chiude l'enumerazione dei provider nell'elenco dei provider registrati.

## <a name="handle-service-control-codes"></a>Gestire i codici di controllo del servizio

-   Quando viene ricevuto un messaggio di controllo del servizio, WDS chiama il callback [*PxeProviderServiceControl.*](pxeproviderservicecontrol.md)
-   Il provider può definire una funzione di callback [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) per gestire i messaggi di controllo del servizio.
-   Registrare il callback [*PxeProviderServiceControl*](pxeproviderservicecontrol.md) chiamando la funzione [**PxeRegisterCallback**](/windows/win32/api/WdsPxe/nf-wdspxe-pxeregistercallback) con **PXE \_ CALLBACK SERVICE \_ \_ CONTROL** durante l'elaborazione del callback [*PxeProviderInitialize.*](pxeproviderinitialize.md)

## <a name="add-trace-entries-to-pxe-log"></a>Aggiungere voci di traccia al log PXE

-   La [**funzione PxeTrace**](/windows/win32/api/WdsPxe/nf-wdspxe-pxetrace) aggiunge una voce di traccia al log PXE. WDSPXE fornisce funzionalità di traccia per aiutare gli amministratori nella risoluzione dei problemi. I provider possono registrare voci di traccia con livelli di gravità diversi. Gli amministratori possono configurare WDSPXE per registrare solo le voci per determinati livelli di gravità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API Windows Deployment Services](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Uso dell'API client di Servizi di distribuzione Windows](using-the-windows-deployment-services-client-api.md)
</dt> </dl>

 

 




