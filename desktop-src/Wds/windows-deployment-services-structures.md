---
title: Windows Strutture dei servizi di distribuzione
description: Le strutture seguenti vengono usate con i servizi Windows distribuzione.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4315ccd3d9540334b00f43fda6522e3eae28be2d038cfdd56fcd129e9e0aed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760251"
---
# <a name="windows-deployment-services-structures"></a>Windows Strutture dei servizi di distribuzione

Le strutture seguenti vengono usate con i servizi Windows distribuzione.



| Struttura                                                                         | Descrizione                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**INDIRIZZO \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | Specifica l'indirizzo di rete per un pacchetto.                                                                        |
| [**PXE \_ DHCP \_ MESSAGE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | Questa struttura viene usata con l'API Windows Server PXE di Servizi di distribuzione.                                        |
| [**OPZIONE DHCP PXE \_ \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | Questa struttura viene usata con l'API Windows Server PXE di Servizi di distribuzione.                                        |
| [**PXE \_ PROVIDER**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | Descrive un provider.                                                                                              |
| [**CRED dell'interfaccia \_ della riga di comando DI \_ WDS**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | Contiene le credenziali utilizzate per autorizzare una sessione client.                                                           |
| [**RICHIESTA \_ TRANSPORTCLIENT WDS \_**](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | Usato dalla [**funzione WdsTransportClientStartSession.**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession)                     |
| [**TRANSPORTCLIENT \_ SESSION \_ INFO**](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | Usato dalla funzione di callback [*PFN \_ WdsTransportClientSessionStartEx.*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) |
| [**PARAMETRI \_ INIT TRANSPORTPROVIDER \_ \_ WDS**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | Usato dalla funzione di callback [**WdsTransportProviderInitialize.**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)            |
| [**IMPOSTAZIONI \_ TRANSPORTPROVIDER WDS \_**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | Usato dalla funzione di callback [**WdsTransportProviderInitialize.**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)            |



 

Gli elementi seguenti sono disponibili a partire da Windows 8 e Windows Server 2012.

| Struttura                                          | Descrizione                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [**OPZIONE DHCPV6 PXE \_ \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | Usato con l Windows API server PXE di Servizi di distribuzione. |
| [**PXE \_ DHCPV6 \_ MESSAGE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | Messaggio DHCPV6.                                         |



 

 

 




