---
description: Un subset della funzionalità API WiFi nativa è supportato in Windows XP con Service Pack 2 (SP2) e Windows XP con Service Pack 3 (SP3).
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Supporto per le API WiFi native in Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346011"
---
# <a name="native-wifi-api-support-on-windows-xp"></a>Supporto per le API WiFi native in Windows XP

Un subset della funzionalità API WiFi nativa è supportato in Windows XP con Service Pack 2 (SP2) e Windows XP con Service Pack 3 (SP3). Questa funzionalità è inclusa in Windows XP con SP3 per impostazione predefinita. In Windows XP con SP2 è possibile aggiungere questa funzionalità applicando un hotfix, noto come API LAN wireless per Windows XP con Service Pack 2 (SP2). Per ulteriori informazioni o per scaricare l'hotfix, vedere "gli sviluppatori non possono creare programmi client wireless che gestiscono profili e connessioni wireless tramite il servizio Wireless Zero Configuration in Microsoft Windows XP Service Pack 2 (SP2)" nella guida e supporto tecnico all'indirizzo [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .

A causa delle differenze di architettura sottostanti in Windows XP, l'API WiFi nativa di presenta alcune limitazioni. Di seguito è riportato un elenco di limitazioni:

-   Al massimo un SSID può essere associato a un profilo.
-   Le reti dell'infrastruttura vengono sempre visualizzate prima delle reti ad hoc nell'elenco dei profili.
-   I nomi dei profili derivano dall'SSID e non possono essere impostati dall'utente su una stringa arbitraria.
-   I tipi PHY non sono supportati.
-   La memorizzazione nella cache Pairwise Master Key (PMK) non è supportata.
-   Le funzioni di estensibilità del fornitore di hardware indipendente (IHV) non sono supportate.
-   Le autorizzazioni del profilo non sono supportate.
-   \_Sono disponibili solo la \_ connessione ACM per le notifiche \_ di WLAN \_ e le notifiche di notifica di rete WLAN \_ \_ ACM \_ disconnesse.
-   Le impostazioni di configurazione globali 802.1 X e avvio EAPOL non sono supportate.

Le funzioni seguenti sono supportate da Windows XP con SP3 e dall'API LAN wireless per Windows XP con SP2:

-   [**\_callback notifiche \_ WLAN**](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
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
-   [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
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

 

 
