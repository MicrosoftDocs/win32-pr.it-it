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
# <a name="iautomaticupdatessettings-properties"></a>Proprietà di IAutomaticUpdatesSettings

L'interfaccia [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) definisce le proprietà seguenti.



| Proprietà                                                                                 | Descrizione                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**NotificationLevel**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | Ottiene e imposta il modo in cui gli utenti ricevono notifiche sugli eventi di aggiornamento automatici.                              |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | Ottiene un valore booleano che indica se le impostazioni di aggiornamento automatico sono di sola lettura.         |
| [**Necessario**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | Ottiene un valore booleano che indica se Criteri di gruppo richiede il servizio di Aggiornamenti automatici. |
| [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | Ottiene e imposta i giorni della settimana in cui Aggiornamenti automatici installa o disinstalla gli aggiornamenti.    |
| [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | Ottiene e imposta l'ora in cui Aggiornamenti automatici installa o disinstalla gli aggiornamenti.                |



 

> [!Note]  
> Windows 8, Windows 8.1, Windows Server 2012 e Windows Server 2012 R2 offrono solo un supporto limitato per [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) e [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). Se il computer è stato configurato tramite Criteri di gruppo per utilizzare una data e un'ora di installazione pianificate, le proprietà **ScheduledInstallationDay** e **ScheduledInstallationTime** restituiscono il giorno e l'ora pianificati. Se il computer non è stato configurato tramite Criteri di gruppo in questo modo, le proprietà **ScheduledInstallationDay** e **ScheduledInstallationTime** restituiscono valori predefiniti e non affidabili. Se si tenta di modificare il giorno e l'ora di installazione pianificata in questi sistemi operativi, **ScheduledInstallationDay** e **ScheduledInstallationTime** sembrano avere esito positivo, ma non hanno alcun effetto.

 

 

 



