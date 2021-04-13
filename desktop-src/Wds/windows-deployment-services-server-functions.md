---
title: Funzioni server di servizi di distribuzione Windows
description: Le funzioni seguenti vengono utilizzate con l'API del server PXE di servizi di distribuzione Windows.
ms.assetid: b6089ff9-4d74-4f5d-957f-4a741c09f4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3852ecfd3e51d6375ca8d566f78d019e733808ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396674"
---
# <a name="windows-deployment-services-server-functions"></a>Funzioni server di servizi di distribuzione Windows

Le funzioni seguenti vengono utilizzate con l'API del server PXE di servizi di distribuzione Windows.



| Funzione                                                           | Descrizione                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone)                       | Restituisce i risultati asincroni della richiesta del client.                                                                                |
| [**PxeDhcpAppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoption)                 | Accoda un'opzione DHCP al pacchetto di risposta.                                                                                     |
| [**PxeDhcpAppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoptionraw)           | Accoda un'opzione DHCP al pacchetto di risposta.                                                                                     |
| [**PxeDhcpGetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue)             | Recupera un valore di opzione da un pacchetto DHCP.                                                                                  |
| [**PxeDhcpGetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) | Recupera un valore di opzione dal campo informazioni specifiche del fornitore (43) di un pacchetto DHCP.                                    |
| [**PxeDhcpInitialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpinitialize)                     | Inizializza un pacchetto di risposta come pacchetto di risposta DHCP.                                                                          |
| [**PxeDhcpIsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpisvalid)                           | Verifica che un pacchetto sia un pacchetto DHCP.                                                                                      |
| [**PxeGetServerInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfo)                       | Restituisce informazioni sul server PXE.                                                                                      |
| [**PxePacketAllocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                     | Alloca un pacchetto da inviare con la funzione [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) .                                          |
| [**PxePacketFree**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketfree)                             | Libera un pacchetto allocato dalla funzione [**PxePacketAllocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate) .                                       |
| [**PxeProviderEnumClose**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumclose)               | Chiude l'enumerazione dei provider aperti dalla funzione [**PxeProviderEnumFirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) .               |
| [**PxeProviderEnumFirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               | Avvia un'enumerazione di provider registrati.                                                                                 |
| [**PxeProviderEnumNext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                 | Enumera i provider registrati.                                                                                               |
| [**PxeProviderFreeInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo)                 | Libera la memoria allocata dalla funzione [**PxeProviderEnumNext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) .                                     |
| [*PxeProviderInitialize*](pxeproviderinitialize.md)               | Un'esportazione da una libreria di collegamento dinamico (DLL) del provider che inizializza il provider e prepara la ricezione delle richieste client. |
| [**PxeProviderQueryIndex**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex)             | Restituisce l'indice del provider specificato nell'elenco dei provider registrati.                                               |
| [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md)             | Chiamato quando viene ricevuta una richiesta da un client.                                                                               |
| [**PxeProviderRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderregister)                 | Registra un provider con il sistema.                                                                                          |
| [*PxeProviderServiceControl*](pxeproviderservicecontrol.md)       | Chiamato quando il servizio WDS riceve un codice di controllo del servizio.                                                             |
| [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)         | Specifica gli attributi per il provider.                                                                                         |
| [*PxeProviderShutdown*](pxeprovidershutdown.md)                   | Chiamato per arrestare il provider.                                                                                               |
| [**PxeProviderUnRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderunregister)             | Rimuove un provider dall'elenco di provider registrati.                                                                      |
| [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)                 | Registra le funzioni di callback per eventi di notifica diversi.                                                                |
| [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                               | Invia un pacchetto a una richiesta client.                                                                                            |
| [**PxeTrace**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxetrace)                                       | Aggiunge una voce di traccia al log PXE.                                                                                             |



 

Il codice seguente è disponibile a partire da Windows 8 e Windows Server 2012.

| Funzione                                                               | Descrizione                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**PxeDhcpv6AppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoption)                 | Accoda un'opzione DHCPv6 al pacchetto di risposta.                                                  |
| [**PxeDhcpv6AppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoptionraw)           | Accoda un'opzione DHCPv6 al pacchetto di risposta.                                                  |
| [**PxeDhcpv6GetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getoptionvalue)             | Recupera un valore di opzione da un pacchetto DHCPv6.                                               |
| [**PxeDhcpv6GetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getvendoroptionvalue) | Recupera i valori delle opzioni dal \_ campo option vendor \_ (17) di un pacchetto DHCPv6.          |
| [**PxeDhcpv6Initialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6initialize)                     | Inizializza un pacchetto di risposta come pacchetto di risposta DHCPv6.                                       |
| [**PxeDhcpv6IsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6isvalid)                           | Verifica che un pacchetto sia un pacchetto DHCPv6 valido.                                             |
| [**PxeGetServerInfoEx**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfoex)                       | Restituisce informazioni sul server PXE.                                                     |
| [**PxeDhcpv6ParseRelayForw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6parserelayforw)             | Consente a un provider di analizzare i messaggi FORW e i messaggi di inoltro delle opzioni annidate \_ \_ . |
| [**PxeDhcpv6CreateRelayRepl**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6createrelayrepl)           | Genera un messaggio di inoltro REPL.                                                               |



 

 

 




