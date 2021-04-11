---
description: Le applicazioni possono adattare meglio il proprio comportamento allo stato di alimentazione corrente del computer registrandosi per gli eventi di alimentazione.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Registrazione per eventi di alimentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da084592414d1c58ab4ab43dd2b5c35f028552b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231527"
---
# <a name="registering-for-power-events"></a>Registrazione per eventi di alimentazione

Le applicazioni possono adattare meglio il proprio comportamento allo stato di alimentazione corrente del computer registrandosi per gli eventi di alimentazione. Un'applicazione deve registrarsi per ogni evento di modifica del risparmio di energia che può influisca sul comportamento.

Un'applicazione o un servizio utilizza la funzione [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) per eseguire la registrazione per le notifiche. Quando viene modificata l'impostazione di risparmio energia corrispondente, il sistema invia le notifiche come segue:

-   Un'applicazione riceve un [**messaggio WM \_ POWERBROADCAST**](wm-powerbroadcast.md) con un *wParam* di [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) e un *lParam* che punta a una struttura di [**\_ Impostazioni POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .
-   Un servizio riceve una chiamata alla funzione di callback [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) registrata chiamando la funzione [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) . Il parametro *lpEventData* inviato alla funzione di callback *HandlerEx* punta a una struttura di [**\_ impostazione POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .

Nella struttura [**delle \_ Impostazioni POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) il membro **PowerSetting** contiene il GUID che identifica la notifica e il membro **dati** contiene il nuovo valore dell'impostazione di risparmio energia.

Per un elenco dei GUID delle impostazioni di risparmio energia per le notifiche che risultano particolarmente utili per le applicazioni, vedere [**GUID delle impostazioni di risparmio energia**](power-setting-guids.md).

 

 
