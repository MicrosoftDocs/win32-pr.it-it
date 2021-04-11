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
# <a name="registering-for-power-events"></a><span data-ttu-id="6ca62-103">Registrazione per eventi di alimentazione</span><span class="sxs-lookup"><span data-stu-id="6ca62-103">Registering for Power Events</span></span>

<span data-ttu-id="6ca62-104">Le applicazioni possono adattare meglio il proprio comportamento allo stato di alimentazione corrente del computer registrandosi per gli eventi di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="6ca62-104">Applications can better adapt their behavior to the current power state of the computer by registering for power events.</span></span> <span data-ttu-id="6ca62-105">Un'applicazione deve registrarsi per ogni evento di modifica del risparmio di energia che può influisca sul comportamento.</span><span class="sxs-lookup"><span data-stu-id="6ca62-105">An application should register for each power change event that might impact its behavior.</span></span>

<span data-ttu-id="6ca62-106">Un'applicazione o un servizio utilizza la funzione [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) per eseguire la registrazione per le notifiche.</span><span class="sxs-lookup"><span data-stu-id="6ca62-106">An application or service uses the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function to register for notifications.</span></span> <span data-ttu-id="6ca62-107">Quando viene modificata l'impostazione di risparmio energia corrispondente, il sistema invia le notifiche come segue:</span><span class="sxs-lookup"><span data-stu-id="6ca62-107">When the corresponding power setting changes, the system sends notifications as follows:</span></span>

-   <span data-ttu-id="6ca62-108">Un'applicazione riceve un [**messaggio WM \_ POWERBROADCAST**](wm-powerbroadcast.md) con un *wParam* di [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) e un *lParam* che punta a una struttura di [**\_ Impostazioni POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="6ca62-108">An application receives a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message with a *wParam* of [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) and an *lParam* that points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>
-   <span data-ttu-id="6ca62-109">Un servizio riceve una chiamata alla funzione di callback [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) registrata chiamando la funzione [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) .</span><span class="sxs-lookup"><span data-stu-id="6ca62-109">A service receives a call to the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) callback function it registered by calling the [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function.</span></span> <span data-ttu-id="6ca62-110">Il parametro *lpEventData* inviato alla funzione di callback *HandlerEx* punta a una struttura di [**\_ impostazione POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="6ca62-110">The *lpEventData* parameter sent to the *HandlerEx* callback function points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

<span data-ttu-id="6ca62-111">Nella struttura [**delle \_ Impostazioni POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) il membro **PowerSetting** contiene il GUID che identifica la notifica e il membro **dati** contiene il nuovo valore dell'impostazione di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="6ca62-111">In the [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure, the **PowerSetting** member contains the GUID that identifies the notification and the **Data** member contains the new value of the power setting.</span></span>

<span data-ttu-id="6ca62-112">Per un elenco dei GUID delle impostazioni di risparmio energia per le notifiche che risultano particolarmente utili per le applicazioni, vedere [**GUID delle impostazioni di risparmio energia**](power-setting-guids.md).</span><span class="sxs-lookup"><span data-stu-id="6ca62-112">For a list of power setting GUIDs for notifications that are most useful to applications, see [**Power Setting GUIDs**](power-setting-guids.md).</span></span>

 

 
