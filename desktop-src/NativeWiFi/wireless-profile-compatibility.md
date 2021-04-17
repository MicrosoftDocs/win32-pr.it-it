---
description: A causa delle differenze di architettura sottostanti nel sistema operativo, Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2) supportano solo un subset degli elementi descritti nello \_ schema del profilo WLAN e il materiale di riferimento dello schema Onex.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Compatibilità del profilo wireless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e0eebfa627fb99d50490907108a2ddc7360202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529239"
---
# <a name="wireless-profile-compatibility"></a>Compatibilità del profilo wireless

A causa delle differenze di architettura sottostanti nel sistema operativo, Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2) supportano solo un subset degli elementi descritti [nello \_ schema del profilo WLAN](wlan-profileschema-schema.md) e il materiale di riferimento [dello schema Onex](onexschema-schema.md) .

Tutti i profili conformi ai requisiti di Windows XP con SP3 e dell'API LAN wireless per Windows XP con SP2 possono essere utilizzati anche in Windows Vista e Windows Server 2008.

## <a name="wlan_profile-support"></a>\_Supporto del profilo WLAN

Gli elementi del \_ profilo WLAN seguenti non sono supportati in Windows XP con SP3 o l'API LAN wireless per Windows XP con SP2:

-   connettività (IHV)
-   IHV (WLANProfile)
-   OUI (OUIHeader)
-   phyType (connettività)
-   PMKCacheMode (sicurezza)
-   PMKCacheSize (sicurezza)
-   PMKCacheTTL (sicurezza)
-   preAuthMode (sicurezza)
-   preAuthThrottle (sicurezza)
-   sicurezza (IHV)
-   tipo (OUIHeader)
-   useMSOneX (IHV)

La tabella seguente mostra \_ gli elementi del profilo WLAN con valori vincolati per Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:



| Elemento                                                                               | Vincolo                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**nome (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)             | L'elemento Name viene ignorato quando il profilo viene salvato nell'archivio profili. Il nome del profilo viene derivato automaticamente dall'SSID della rete. Per i profili di rete dell'infrastruttura, il nome del profilo è il SSID della rete. Per i profili di rete ad hoc, il nome del profilo è il SSID della rete ad hoc seguita da `-adhoc` . |
| [**protetto (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)       | Il valore di deve essere FALSE.                                                                                                                                                                                                                                                                                                                                      |
| [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md) | Limitato a un elemento [**SSID figlio (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) .                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a>Supporto di OneX

Solo l'elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) è supportato in Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2. Gli altri elementi OneX, se presenti in un profilo, verranno ignorati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API WiFi nativa](about-the-native-wifi-api.md)
</dt> <dt>

[Supporto per le API WiFi native in Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



