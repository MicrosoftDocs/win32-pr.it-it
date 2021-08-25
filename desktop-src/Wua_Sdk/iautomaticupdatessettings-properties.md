---
description: L'interfaccia IAutomaticUpdatesSettings definisce le proprietà seguenti.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Proprietà IAutomaticUpdatesSettings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6995264aebed44e8cb21e3880268a1488157ed5085645e5232feaa94a8786eed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897151"
---
# <a name="iautomaticupdatessettings-properties"></a>Proprietà IAutomaticUpdatesSettings

[**L'interfaccia IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) definisce le proprietà seguenti.



| Proprietà                                                                                 | Descrizione                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**NotificationLevel**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | Ottiene e imposta la modalità di notifica degli utenti sugli eventi di aggiornamento automatico.                              |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | Ottiene un valore booleano che indica se le impostazioni di Aggiornamento automatico sono di sola lettura.         |
| [**Necessario**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | Ottiene un valore booleano che indica se Criteri di gruppo richiede il Aggiornamenti automatici servizio. |
| [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | Ottiene e imposta i giorni della settimana in cui Aggiornamenti automatici installa o disinstalla gli aggiornamenti.    |
| [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | Ottiene e imposta l'ora in cui Aggiornamenti automatici installa o disinstalla gli aggiornamenti.                |



 

> [!Note]  
> Windows 8, Windows 8.1, Windows Server 2012 e Windows Server 2012 R2 offrono solo supporto limitato per [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) e [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). Se il computer è stato configurato tramite Criteri di gruppo per usare un giorno e un'ora di installazione pianificata, le proprietà **ScheduledInstallationDay** e **ScheduledInstallationTime** restituiscono il giorno e l'ora pianificati. Se il computer non è stato configurato tramite Criteri di gruppo in questo modo, le proprietà **ScheduledInstallationDay** e **ScheduledInstallationTime** restituiscono valori predefiniti e non affidabili. Se si tenta di modificare il giorno e l'ora di installazione pianificata in questi sistemi operativi, **ScheduledInstallationDay** e **ScheduledInstallationTime** sembrano avere esito positivo, ma non hanno alcun effetto.

 

 

 



