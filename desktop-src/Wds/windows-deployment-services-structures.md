---
title: Strutture di servizi di distribuzione Windows
description: Con servizi di distribuzione Windows vengono utilizzate le strutture seguenti.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20f5b369a2bbb5d68bd77dce1751e09fed2e6b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045212"
---
# <a name="windows-deployment-services-structures"></a>Strutture di servizi di distribuzione Windows

Con servizi di distribuzione Windows vengono utilizzate le strutture seguenti.



| Struttura                                                                         | Descrizione                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**\_Indirizzo PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | Specifica l'indirizzo di rete per un pacchetto.                                                                        |
| [**\_messaggio DHCP \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | Questa struttura viene utilizzata con l'API del server PXE di servizi di distribuzione Windows.                                        |
| [**PXE \_ ( \_ opzione DHCP)**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | Questa struttura viene utilizzata con l'API del server PXE di servizi di distribuzione Windows.                                        |
| [**\_provider PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | Descrive un provider.                                                                                              |
| [**\_cred dell'interfaccia della riga di comando WDS \_**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | Contiene le credenziali utilizzate per autorizzare una sessione client.                                                           |
| [**\_richiesta TRANSPORTCLIENT di WDS \_**](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | Usato dalla funzione [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) .                     |
| [**\_informazioni sulla sessione TRANSPORTCLIENT \_**](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | Usato dalla funzione di callback [*\_ WdsTransportClientSessionStartEx di PFN*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) . |
| [**\_ \_ parametri init di WDS TRANSPORTPROVIDER \_**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | Usato dalla funzione di callback [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .            |
| [**\_Impostazioni TRANSPORTPROVIDER \_ WDS**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | Usato dalla funzione di callback [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .            |



 

Il codice seguente è disponibile a partire da Windows 8 e Windows Server 2012.

| Struttura                                          | Descrizione                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [**PXE \_ ( \_ opzione DHCPV6)**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | Utilizzato con l'API del server PXE di servizi di distribuzione Windows. |
| [**\_Messaggio DHCPV6 \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | Messaggio DHCPV6.                                         |



 

 

 




