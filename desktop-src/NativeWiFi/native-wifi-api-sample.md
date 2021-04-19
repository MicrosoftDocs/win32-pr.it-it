---
description: Viene illustrato l'utilizzo delle funzioni di gestione di rete wireless di base.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Esempio di API WiFi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac72000363fcb91f013c3f55d4686335c0a59e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311689"
---
# <a name="native-wifi-api-sample"></a>Esempio di API WiFi nativa

Con Microsoft Windows Software Development Kit (SDK) è incluso un esempio di API Wi-Fi nativo che illustra l'uso delle funzioni di gestione di rete wireless di base. La versione più recente del Windows SDK è disponibile nell' [area download](https://developer.microsoft.com/windows/downloads).

Per impostazione predefinita, il codice sorgente di esempio di WiFi nativo viene installato nella directory seguente:

**C: \\ programmi \\ Microsoft SDK \\ Windows \\ <version number> \\ Samples \\ NetDs \\ WLAN**

L'esempio di API WiFi nativa si trova nella cartella seguente:

**AutoConfig**

Questo esempio può essere compilato ed eseguito in Windows Vista e versioni successive, Windows XP con Service Pack 3 (SP3) e l'API LAN wireless per Windows XP con Service Pack 2 (SP2). Alcune funzionalità dell'esempio non sono supportate in Windows XP con SP3 e nell'API LAN wireless per Windows XP con SP2. Per un elenco delle funzioni supportate da Windows XP con SP3 e dall'API LAN wireless per Windows XP con SP2, vedere [supporto per le API WiFi native in Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).

Nell'esempio di connessione Wi-Fi nativa viene illustrato come eseguire le attività seguenti:

-   Enumerare le interfacce wireless. Vedere [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).
-   Ottenere le funzionalità di un'interfaccia. Vedere [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).

    * * Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2: * * questa funzionalità non è supportata.

-   Eseguire una query su un'interfaccia. Vedere [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).
-   Impostare i parametri per un'interfaccia di rete. Vedere [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface). Questa funzione può essere utilizzata per attivare e disattivare la radio wireless (e quindi abilitare o disabilitare la connettività di rete wireless).
-   Ricercare le reti wireless disponibili. Vedere [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).
-   Ottiene l'elenco delle reti wireless disponibili o visibili. Vedere [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).
-   Ottenere, salvare o eliminare un profilo. Vedere [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)e [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).
-   Connettersi o disconnettersi da una rete wireless. Vedere [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) e [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del WiFi nativo](using-native-wifi.md)
</dt> <dt>

[Forum su Windows Vista Wireless SDK](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

[Risoluzione dei problemi relativi alle connessioni wireless di Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))
</dt> </dl>

 

 
