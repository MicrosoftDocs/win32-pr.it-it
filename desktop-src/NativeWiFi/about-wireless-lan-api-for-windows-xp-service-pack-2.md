---
description: In Windows XP con Service Pack 2 (SP2) e Windows XP con Service Pack 3 (SP3) è supportato un subset delle funzionalità dell'API Wifi nativa.
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Supporto dell'API Wifi nativa in Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc284ed24a6aa6ddb266b410a6233c15e063bf909aa9c82f0afa3dc070c9289
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685311"
---
# <a name="native-wifi-api-support-on-windows-xp"></a>Supporto dell'API Wifi nativa in Windows XP

In Windows XP con Service Pack 2 (SP2) e Windows XP con Service Pack 3 (SP3) è supportato un subset delle funzionalità dell'API Wifi nativa. Questa funzionalità è inclusa in Windows XP con SP3 per impostazione predefinita. In Windows XP con SP2 questa funzionalità può essere aggiunta applicando un hotfix, noto come API LAN wireless per Windows XP con Service Pack 2 (SP2). Per altre informazioni o per scaricare l'hotfix, vedere "Developers cannot create wireless client programs that manage wireless profiles and connections over the Wireless Zero Configuration service in Microsoft Windows XP Service Pack 2 (SP2)" (Gli sviluppatori non possono creare programmi client wireless che gestiscono profili e connessioni wireless tramite il servizio Wireless Zero Configuration in Microsoft Windows XP Service Pack 2 (SP2)" nella guida e supporto tecnico Knowledge Base all'indirizzo [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .

A causa delle differenze di architettura sottostanti Windows XP, l'API Wi-Fi nativa in presenta alcune limitazioni. Ecco un elenco di limitazioni:

-   È possibile associare al massimo un SSID a un profilo.
-   Le reti dell'infrastruttura vengono sempre visualizzate prima delle reti ad hoc nell'elenco dei profili.
-   I nomi dei profili derivano dall'SSID e non possono essere impostati dall'utente su una stringa arbitraria.
-   I tipi PHY non sono supportati.
-   La memorizzazione nella cache della chiave master pairwise (PMK) non è supportata.
-   Le funzioni di estendibilità del fornitore di hardware indipendente (IHV) non sono supportate.
-   Le autorizzazioni del profilo non sono supportate.
-   Sono disponibili solo le notifiche \_ wlan notification \_ acm \_ connection complete e \_ wlan notification \_ \_ acm \_ disconnected notifications.
-   Le impostazioni di configurazione globali 802.1X ed EAPOL non sono supportate.

Le funzioni seguenti sono supportate da Windows XP con SP3 e dall'API LAN wireless per Windows XP con SP2:

-   [**CALLBACK DI NOTIFICA WLAN \_ \_**](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [**WlanAllocateMemory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [**WlanFreeMemory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [**WlanGetProfileList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [**WlanOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [**Interfaccia WlanSet**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [**WlanSetProfileEapXmlUserData**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [**WlanSetProfileList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [**WlanSetProfilePosition**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[Informazioni sul Wi-Fi nativo](about-native-wifi.md)
</dt> </dl>

 

 
