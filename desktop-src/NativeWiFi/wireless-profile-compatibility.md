---
description: A causa delle differenze di architettura sottostanti nel sistema operativo, Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2) supportano solo un subset degli elementi descritti nel materiale di riferimento Schema e OneX Schema del profilo \_ WLAN.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Compatibilità dei profili wireless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36db0ecea6f85341d904603c99308ec10e79cee20d7567160cd3beee3b13c35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684571"
---
# <a name="wireless-profile-compatibility"></a>Compatibilità dei profili wireless

A causa delle differenze di architettura sottostanti nel sistema operativo, Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2) supportano solo un subset degli elementi descritti nel materiale di riferimento dello schema del profilo [WLAN \_ ](wlan-profileschema-schema.md) e [dello schema OneX.](onexschema-schema.md)

Tutti i profili conformi Windows XP con SP3 e l'API LAN wireless per i requisiti di Windows XP con SP2 possono essere usati anche in Windows Vista e Windows Server 2008.

## <a name="wlan_profile-support"></a>Supporto del profilo \_ WLAN

Gli elementi del profilo WLAN seguenti non sono supportati in Windows XP con SP3 o \_ NELL'API LAN wireless per Windows XP con SP2:

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
-   type (OUIHeader)
-   useMSOneX (IHV)

La tabella seguente illustra gli elementi del profilo WLAN con valori vincolati per Windows XP con SP3 e \_ l'API LAN wireless per Windows XP con SP2:



| Elemento                                                                               | Vincolo                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**name (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)             | L'elemento name viene ignorato quando il profilo viene salvato nell'archivio profili. Il nome del profilo viene derivato automaticamente dall'SSID della rete. Per i profili di rete dell'infrastruttura, il nome del profilo è l'SSID della rete. Per i profili di rete ad hoc, il nome del profilo è il SSID della rete ad hoc seguito da `-adhoc` . |
| [**protected (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)       | Deve avere valore FALSE.                                                                                                                                                                                                                                                                                                                                      |
| [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md) | Limitato a un elemento [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) figlio.                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a>Supporto OneX

Solo [**l'elemento EAPConfig**](onexschema-eapconfig-onex-element.md) è supportato in Windows XP con SP3 e nell'API LAN wireless per Windows XP con SP2. Gli altri elementi OneX, se presenti in un profilo, verranno ignorati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API Wi-Fi nativa](about-the-native-wifi-api.md)
</dt> <dt>

[Supporto dell'API WiFi nativa in Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



