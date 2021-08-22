---
description: Novità di Native WiFi
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Novità di Native WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a9430fa2c1645d574f8b4ab851a8cf5ce1407139cfe63a6aabeb3ebfd57abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064861"
---
# <a name="whats-new-in-native-wifi"></a>Novità di Native WiFi

## <a name="windows-10-version-2004"></a>Windows 10, versione 2004

Vedere [Effettuare il provisioning Wi-Fi profilo di rete tramite un sito Web.](prov-wifi-profile-via-website.md)

## <a name="windows-10"></a>Windows 10

Il supporto per Hotspot 2.0 è stato aggiunto allo [ \_ schema del profilo WLAN](wlan-profileschema-schema.md). Hotspot 2.0 consente la connessione automatica ai servizi Wi-Fi usando credenziali esistenti e l'appartenenza alle reti dei provider di servizi. I provider di servizi specificano come vengono effettuate le connessioni usando i nuovi elementi dello schema per descrivere le reti da usare e come eseguire l'autenticazione. Per informazioni [**dettagliate, vedere la**](wlan-profileschema-hotspot2-element.md) documentazione dell'elemento Hotspot2.

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 e Windows Server 2012

Le funzionalità seguenti sono state aggiunte alle API Wi-Fi native in Windows 8 e Windows Server 2012.

Funzionalità Wi-Fi Direct basata sullo sviluppo della specifica tecnica Wi-Fi Peer-to-Peer v1.1 di Wi-Fi Alliance (vedere Le specifiche pubblicate di [Wi-Fi Alliance).](https://www.wi-fi.org/) L'obiettivo della specifica tecnica peer-to-peer di Wi-Fi è quello di fornire una soluzione per la connettività da dispositivo a dispositivo di Wi-Fi senza la necessità di un punto di accesso wireless (AP wireless) per configurare la connessione o l'uso del meccanismo adhoc (IBSS) Wi-Fi esistente.

Le funzioni seguenti supportano la Wi-Fi Direct.

-   [**CALLBACK DI APERTURA \_ \_ SESSIONE WFD \_ \_ COMPLETATO**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

Le funzionalità seguenti sono state aggiunte alle API Wifi native in Windows 7 e Windows Server 2008 R2.

La rete wireless ospitata consente a una singola scheda wireless fisica di connettersi come client a un punto di accesso hardware (AP), mentre allo stesso tempo funge da punto di accesso software che consente ad altri dispositivi che supportano wireless di connettersi a esso.

Le funzioni seguenti supportano la funzionalità Rete ospitata wireless.

-   [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

Le nuove strutture seguenti che funzionano con la rete ospitata wireless.

-   [**IMPOSTAZIONI DI \_ CONNESSIONE DI \_ RETE OSPITATA \_ \_ WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [**MODIFICA DELLO STATO \_ DEL PEER DI DATI DI RETE \_ \_ OSPITATA \_ \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [**STATO DEL \_ PEER DI RETE OSPITATO \_ \_ \_ WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [**STATO RADIO \_ RETE \_ OSPITATA \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [**IMPOSTAZIONI DI \_ SICUREZZA DELLA RETE \_ OSPITATA \_ \_ WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [**MODIFICA DELLO \_ STATO DELLA RETE \_ OSPITATA \_ \_ WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [**STATO RETE \_ OSPITATA \_ \_ WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

Le nuove enumerazioni seguenti che funzionano con la rete ospitata wireless.

-   [**CODICE DI \_ NOTIFICA DELLA RETE \_ OSPITATA \_ \_ WLAN**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [**CODICE OPERATIVO \_ DELLA RETE \_ OSPITATA \_ WLAN**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [**STATO DI \_ AUTENTICAZIONE PEER DI RETE \_ \_ OSPITATA \_ \_ WLAN**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [**MOTIVO DELLA \_ RETE OSPITATA \_ \_ WLAN**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [**STATO DELLA \_ RETE OSPITATA \_ \_ WLAN**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla rete wireless ospitata](about-the-wireless-hosted-network.md)
</dt> <dt>

[Uso di Rete ospitata wireless e Condivisione connessione Internet](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



