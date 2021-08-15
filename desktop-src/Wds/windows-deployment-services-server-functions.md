---
title: Windows Funzioni server di Servizi di distribuzione
description: Le funzioni seguenti vengono usate con l Windows API server PXE di Servizi di distribuzione.
ms.assetid: b6089ff9-4d74-4f5d-957f-4a741c09f4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cc99f01dc88fce91beafe51a65f8e8ddccfdf08c4361fb194a7e60451a5aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330605"
---
# <a name="windows-deployment-services-server-functions"></a>Windows Funzioni server di Servizi di distribuzione

Le funzioni seguenti vengono usate con l Windows API server PXE di Servizi di distribuzione.



| Funzione                                                           | Descrizione                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone)                       | Restituisce i risultati asincroni della richiesta del client.                                                                                |
| [**PxeDhcpAppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoption)                 | Aggiunge un'opzione DHCP al pacchetto di risposta.                                                                                     |
| [**PxeDhcpAppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoptionraw)           | Aggiunge un'opzione DHCP al pacchetto di risposta.                                                                                     |
| [**PxeDhcpGetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue)             | Recupera un valore di opzione da un pacchetto DHCP.                                                                                  |
| [**PxeDhcpGetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) | Recupera il valore di un'opzione dal campo Informazioni specifiche del fornitore (43) di un pacchetto DHCP.                                    |
| [**PxeDhcpInitialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpinitialize)                     | Inizializza un pacchetto di risposta come pacchetto di risposta DHCP.                                                                          |
| [**PxeDhcpIsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpisvalid)                           | Convalida che un pacchetto è un pacchetto DHCP.                                                                                      |
| [**PxeGetServerInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfo)                       | Restituisce informazioni sul server PXE.                                                                                      |
| [**PxePacketAllocate**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                     | Alloca un pacchetto da inviare con [**la funzione PxeSendReply.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                                          |
| [**PxePacketFree**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketfree)                             | Libera un pacchetto allocato dalla [**funzione PxePacketAllocate.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                                       |
| [**PxeProviderEnumClose**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumclose)               | Chiude l'enumerazione dei provider aperti dalla [**funzione PxeProviderEnumFirst.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               |
| [**PxeProviderEnumFirst**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               | Avvia un'enumerazione di provider registrati.                                                                                 |
| [**PxeProviderEnumNext**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                 | Enumera i provider registrati.                                                                                               |
| [**PxeProviderFreeInfo**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo)                 | Libera la memoria allocata dalla [**funzione PxeProviderEnumNext.**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                                     |
| [*PxeProviderInitialize*](pxeproviderinitialize.md)               | Esportazione da una libreria a collegamento dinamico (DLL) del provider che inizializza il provider e lo prepara alla ricezione delle richieste client. |
| [**PxeProviderQueryIndex**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex)             | Restituisce l'indice del provider specificato nell'elenco dei provider registrati.                                               |
| [*PxeProviderRecvRequest*](pxeproviderrecvrequest.md)             | Chiamato quando viene ricevuta una richiesta da un client.                                                                               |
| [**PxeProviderRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderregister)                 | Registra un provider con il sistema.                                                                                          |
| [*PxeProviderServiceControl*](pxeproviderservicecontrol.md)       | Chiamato quando un codice di controllo del servizio viene ricevuto dal servizio Servizi di distribuzione Windows.                                                             |
| [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)         | Specifica gli attributi per il provider.                                                                                         |
| [*PxeProviderShutdown*](pxeprovidershutdown.md)                   | Chiamato per arrestare il provider.                                                                                               |
| [**PxeProviderUnRegister**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderunregister)             | Rimuove un provider dall'elenco di provider registrati.                                                                      |
| [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)                 | Registra le funzioni di callback per eventi di notifica diversi.                                                                |
| [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                               | Invia un pacchetto a una richiesta client.                                                                                            |
| [**PxeTrace**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxetrace)                                       | Aggiunge una voce di traccia al log PXE.                                                                                             |



 

Gli elementi seguenti sono disponibili a partire da Windows 8 e Windows Server 2012.

| Funzione                                                               | Descrizione                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**PxeDhcpv6AppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoption)                 | Aggiunge un'opzione DHCPv6 al pacchetto di risposta.                                                  |
| [**PxeDhcpv6AppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoptionraw)           | Aggiunge un'opzione DHCPv6 al pacchetto di risposta.                                                  |
| [**PxeDhcpv6GetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getoptionvalue)             | Recupera un valore di opzione da un pacchetto DHCPv6.                                               |
| [**PxeDhcpv6GetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getvendoroptionvalue) | Recupera i valori delle opzioni dal campo OPTION \_ VENDOR \_ OPTS (17) di un pacchetto DHCPv6.          |
| [**PxeDhcpv6Initialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6initialize)                     | Inizializza un pacchetto di risposta come pacchetto di risposta DHCPv6.                                       |
| [**PxeDhcpv6IsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6isvalid)                           | Convalida che un pacchetto è un pacchetto DHCPv6 valido.                                             |
| [**PxeGetServerInfoEx**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfoex)                       | Restituisce informazioni sul server PXE.                                                     |
| [**PxeDhcpv6ParseRelayForw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6parserelayforw)             | Consente a un provider di analizzare i messaggi RELAY-FORW e i relativi messaggi OPTION \_ RELAY \_ MSG annidati. |
| [**PxeDhcpv6CreateRelayRepl**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6createrelayrepl)           | Genera un messaggio RELAY-REPL.                                                               |



 

 

 




