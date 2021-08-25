---
description: Illustra l'uso di funzioni di gestione di rete wireless di base.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Esempio di API Wi-Fi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed28fadcd73eb4b3e632702078280ddba55d683c66decfdf03bc948182c52d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801061"
---
# <a name="native-wifi-api-sample"></a>Esempio di API Wi-Fi nativa

Un esempio di API Wi-Fi nativa che illustra l'uso di funzioni di gestione di rete wireless di base è incluso in Microsoft Windows Software Development Kit (SDK). La versione più recente di Windows SDK è disponibile [nell'Area download](https://developer.microsoft.com/windows/downloads).

Per impostazione predefinita, il codice sorgente di esempio Wi-Fi nativo viene installato nella directory seguente:

**C: \\ Programmi \\ Microsoft SDKs Windows \\ Esempi \\ <version number> \\ \\ NetDs \\ Wlan**

L'esempio di API Wi-Fi nativa si trova nella cartella seguente:

**Autoconfig**

L'esempio Wi-Fi nativo può essere compilato ed eseguito in Windows Vista e versioni successive, in Windows XP con Service Pack 3 (SP3) e nell'API LAN wireless per Windows XP con Service Pack 2 (SP2). Alcune funzionalità dell'esempio non sono supportate in Windows XP con SP3 e nell'API LAN wireless per Windows XP con SP2. Per un elenco delle funzioni supportate da Windows XP con SP3 e dall'API LAN wireless per Windows XP con SP2, vedere Supporto api Wifi native [in Windows XP.](about-wireless-lan-api-for-windows-xp-service-pack-2.md)

L'esempio Wi-Fi nativo illustra come eseguire le attività seguenti:

-   Enumerare le interfacce wireless. Vedere [**WlanEnumInterfaces.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   Ottenere le funzionalità di un'interfaccia. Vedere [**WlanGetInterfaceCapability.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability)

    **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2: ** Questa funzionalità non è supportata.

-   Eseguire query su un'interfaccia. Vedere [**WlanQueryInterface.**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   Impostare i parametri per un'interfaccia di rete. Vedere [**WlanSetInterface.**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface) Questa funzione può essere usata per attivare e disattivare la radio wireless (e quindi abilitare o disabilitare la connettività di rete wireless).
-   Cercare le reti wireless disponibili. Vedere [**WlanScan.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   Ottenere l'elenco delle reti wireless disponibili o visibili. Vedere [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).
-   Ottenere, salvare o eliminare un profilo. Vedere [**WlanGetProfile,**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)e [**WlanDeleteProfile.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   Connessione o disconnettersi da una rete wireless. Vedere [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) e [**WlanDisconnect.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Wi-Fi nativo](using-native-wifi.md)
</dt> <dt>

[Windows Vista Wireless SDK Forum](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

[Risoluzione dei Windows connessioni wireless di Vista 802.11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))
</dt> </dl>

 

 
