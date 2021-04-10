---
description: L'interfaccia IAutomaticUpdatesSettings definisce le proprietà seguenti.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Proprietà di IAutomaticUpdatesSettings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2463fdc69fc93960ee45c0003a65894eaaf7399
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966744"
---
# <a name="iautomaticupdatessettings-properties"></a><span data-ttu-id="b640c-103">Proprietà di IAutomaticUpdatesSettings</span><span class="sxs-lookup"><span data-stu-id="b640c-103">IAutomaticUpdatesSettings Properties</span></span>

<span data-ttu-id="b640c-104">L'interfaccia [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="b640c-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following properties.</span></span>



| <span data-ttu-id="b640c-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b640c-105">Property</span></span>                                                                                 | <span data-ttu-id="b640c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b640c-106">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b640c-107">**NotificationLevel**</span><span class="sxs-lookup"><span data-stu-id="b640c-107">**NotificationLevel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | <span data-ttu-id="b640c-108">Ottiene e imposta il modo in cui gli utenti ricevono notifiche sugli eventi di aggiornamento automatici.</span><span class="sxs-lookup"><span data-stu-id="b640c-108">Gets and sets how users are notified about Automatic Update events.</span></span>                              |
| [<span data-ttu-id="b640c-109">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="b640c-109">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | <span data-ttu-id="b640c-110">Ottiene un valore booleano che indica se le impostazioni di aggiornamento automatico sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b640c-110">Gets a Boolean value that indicates whether the Automatic Update settings are read-only.</span></span>         |
| [<span data-ttu-id="b640c-111">**Necessario**</span><span class="sxs-lookup"><span data-stu-id="b640c-111">**Required**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | <span data-ttu-id="b640c-112">Ottiene un valore booleano che indica se Criteri di gruppo richiede il servizio di Aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="b640c-112">Gets a Boolean value that indicates whether Group Policy requires the Automatic Updates service.</span></span> |
| [<span data-ttu-id="b640c-113">**ScheduledInstallationDay**</span><span class="sxs-lookup"><span data-stu-id="b640c-113">**ScheduledInstallationDay**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | <span data-ttu-id="b640c-114">Ottiene e imposta i giorni della settimana in cui Aggiornamenti automatici installa o disinstalla gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="b640c-114">Gets and sets the days of the week on which Automatic Updates installs or uninstalls updates.</span></span>    |
| [<span data-ttu-id="b640c-115">**ScheduledInstallationTime**</span><span class="sxs-lookup"><span data-stu-id="b640c-115">**ScheduledInstallationTime**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | <span data-ttu-id="b640c-116">Ottiene e imposta l'ora in cui Aggiornamenti automatici installa o disinstalla gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="b640c-116">Gets and sets the time at which Automatic Updates installs or uninstalls updates.</span></span>                |



 

> [!Note]  
> <span data-ttu-id="b640c-117">Windows 8, Windows 8.1, Windows Server 2012 e Windows Server 2012 R2 offrono solo un supporto limitato per [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) e [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span><span class="sxs-lookup"><span data-stu-id="b640c-117">Windows 8, Windows 8.1, Windows Server 2012, and Windows Server 2012 R2 provide only limited support for [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) and [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="b640c-118">Se il computer è stato configurato tramite Criteri di gruppo per utilizzare una data e un'ora di installazione pianificate, le proprietà **ScheduledInstallationDay** e **ScheduledInstallationTime** restituiscono il giorno e l'ora pianificati.</span><span class="sxs-lookup"><span data-stu-id="b640c-118">If the computer has been configured through Group Policy to use a scheduled installation day and time, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return this scheduled day and time.</span></span> <span data-ttu-id="b640c-119">Se il computer non è stato configurato tramite Criteri di gruppo in questo modo, le proprietà **ScheduledInstallationDay** e **ScheduledInstallationTime** restituiscono valori predefiniti e non affidabili.</span><span class="sxs-lookup"><span data-stu-id="b640c-119">If the computer hasn't been configured through Group Policy in this way, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return default and unreliable values.</span></span> <span data-ttu-id="b640c-120">Se si tenta di modificare il giorno e l'ora di installazione pianificata in questi sistemi operativi, **ScheduledInstallationDay** e **ScheduledInstallationTime** sembrano avere esito positivo, ma non hanno alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="b640c-120">If you try to modify the scheduled installation day and time on these operating systems, **ScheduledInstallationDay** and **ScheduledInstallationTime** appear to succeed but have no effect.</span></span>

 

 

 



