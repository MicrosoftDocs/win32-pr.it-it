---
description: Novità di Native WiFi
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Novità di Native WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126627f4cf6431fbac2bf4d1f6ec58561bfd8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309441"
---
# <a name="whats-new-in-native-wifi"></a>Novità di Native WiFi

## <a name="windows-10-version-2004"></a>Windows 10, versione 2004

Vedere effettuare il [provisioning di un profilo di Wi-Fi tramite un sito Web](prov-wifi-profile-via-website.md).

## <a name="windows-10"></a>Windows 10

È stato aggiunto il supporto per Hotspot 2,0 allo [ \_ schema del profilo WLAN](wlan-profileschema-schema.md). Hotspot 2,0 consente la connessione automatica ai servizi Wi-Fi pubblici usando le credenziali esistenti e l'appartenenza alle reti del provider di servizi. I provider di servizi specificano il modo in cui vengono stabilite le connessioni usando i nuovi elementi dello schema per descrivere le reti da usare e come eseguire l'autenticazione. Per informazioni dettagliate, vedere la documentazione dell'elemento [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 e Windows Server 2012

Le funzionalità seguenti sono state aggiunte alle API native di Wi-Fi in Windows 8 e Windows Server 2012.

Una Wi-Fi funzionalità diretta basata sullo sviluppo di Wi-Fi specifiche tecniche peer-to-Peer v 1.1 da Wi-Fi Alliance (vedere le [specifiche pubblicate in Wi-Fi Alliance](https://www.wi-fi.org/)). L'obiettivo della specifica tecnica peer-to-peer Wi-Fi è fornire una soluzione per Wi-Fi la connettività da dispositivo a dispositivo senza che sia necessario un punto di accesso wireless (AP wireless) per configurare la connessione o l'utilizzo del meccanismo di Wi-Fi ad hoc (IBSS) esistente.

Le funzioni seguenti supportano la funzionalità Wi-Fi Direct.

-   [**\_ \_ callback completo della sessione di apertura della \_ direttiva GMA \_**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 e Windows Server 2008 R2

Le funzionalità seguenti sono state aggiunte alle API native di Wi-Fi in Windows 7 e Windows Server 2008 R2.

La rete wireless ospitata consente a una singola scheda di rete fisica di connettersi come client a un punto di accesso hardware (AP), mentre allo stesso tempo funge da AP software che consente ad altri dispositivi con supporto wireless di connettersi.

Le funzioni seguenti supportano la funzionalità rete ospitata senza fili.

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

Le nuove strutture seguenti funzionano con la rete wireless ospitata.

-   [**\_impostazioni di \_ connessione di rete ospitata da \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [**\_ \_ \_ \_ \_ modifica stato peer di dati rete ospitata WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [**\_ \_ stato peer di rete OSPITAta WLAN \_ \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [**\_ \_ \_ stato radio rete ospitata WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [**\_impostazioni di \_ sicurezza della rete ospitata da \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [**\_ \_ \_ modifica dello stato della rete ospitata WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [**\_stato rete ospitata WLAN \_ \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

Le seguenti nuove enumerazioni che funzionano con la rete wireless ospitata.

-   [**\_codice di \_ notifica della rete ospitata da \_ WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [**\_ \_ codice operativo rete OSPITAta WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [**\_ \_ \_ \_ stato autenticazione peer rete ospitata WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [**\_motivo rete ospitata WLAN \_ \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [**\_stato rete ospitata WLAN \_ \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla rete wireless ospitata](about-the-wireless-hosted-network.md)
</dt> <dt>

[Uso della rete ospitata wireless e della condivisione della connessione Internet](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



