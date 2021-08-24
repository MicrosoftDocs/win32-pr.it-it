---
description: Le applicazioni possono adattare meglio il comportamento allo stato di alimentazione corrente del computer registrando gli eventi di risparmio energia.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Registrazione per gli eventi di risparmio energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c360905800ad3fdce047e16a0244cd3dbf1ca312f18154f0be0c36b75e546d5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143324"
---
# <a name="registering-for-power-events"></a>Registrazione per gli eventi di risparmio energia

Le applicazioni possono adattare meglio il comportamento allo stato di alimentazione corrente del computer registrando gli eventi di risparmio energia. Un'applicazione deve registrarsi per ogni evento di modifica dell'alimentazione che potrebbe influire sul comportamento.

Un'applicazione o un servizio usa la [**funzione RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) per la registrazione per le notifiche. Quando viene modificata l'impostazione di risparmio energia corrispondente, il sistema invia le notifiche come segue:

-   Un'applicazione riceve un messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) con *wParam* [di PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) e *un lParam* che punta a una [**struttura POWERBROADCAST \_ SETTING.**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
-   Un servizio riceve una chiamata alla funzione di callback [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) registrata chiamando la [**funzione RegisterServiceCtrlHandlerEx.**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) Il *parametro lpEventData* inviato alla funzione di callback *HandlerEx* punta a una [**struttura SETTING DI POWERBROADCAST. \_**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)

Nella struttura [**POWERBROADCAST \_ SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) il membro **Di PowerSetting** contiene il GUID che identifica la notifica e il membro **dati** contiene il nuovo valore dell'impostazione di risparmio energia.

Per un elenco dei GUID delle impostazioni di risparmio energia per le notifiche più utili per le applicazioni, vedere [**GUID delle impostazioni di risparmio energia.**](power-setting-guids.md)

 

 
