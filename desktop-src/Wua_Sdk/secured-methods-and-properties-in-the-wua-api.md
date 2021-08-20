---
description: Quando WUA rileva che un chiamante non dispone dell'autorizzazione per accedere a un'interfaccia, a un metodo o a una proprietà, viene restituito HRESULT E \_ ACCESSDENIED.
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: Protezione di interfacce, metodi e proprietà nell'API WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53ad374734e596cf6e419e7ed426a90719328fc012d0750a6f3b1d27b8e8f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106192"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a>Protezione di interfacce, metodi e proprietà nell'API WUA

Alcune interfacce, metodi e proprietà di Windows Update Agent (WUA) sono accessibili solo ai chiamanti che appartengono ai gruppi di sicurezza Windows seguenti:

-   Amministratore
-   Utente
-   Utente esperto

Quando WUA rileva che un chiamante non dispone dell'autorizzazione per accedere a un'interfaccia, a un metodo o a una proprietà, viene restituito **HRESULT** E \_ ACCESSDENIED.

Le interfacce seguenti sono disponibili per i gruppi di sicurezza Administrator, User e Power User:

-   [**IAutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [**IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [**ISystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) e [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)

> [!Note]  
> Se le condizioni seguenti sono vere, una ricerca ha esito negativo:
>
> -   Un utente che non è un amministratore imposta la [**proprietà UserLocale dell'interfaccia IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) su impostazioni locali che corrispondono a una lingua non installata nel computer.
> -   La ricerca usa un oggetto UpdateSearch creato dall'oggetto UpdateSession.

 

Le interfacce e i metodi di download seguenti sono disponibili per i gruppi Administrator e Power User:

-   [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [**IUpdate::CopyFromCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IAutomaticUpdatesSettings2::CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > Amministratori, utenti e utenti esperti possono chiamare [**IAutomaticUpdatesSettings2::CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).

     

Le interfacce, i metodi e le proprietà di installazione seguenti sono disponibili per i gruppi Administrator:

-   [**IAutomaticUpdates::P ause**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**IAutomaticUpdates::Resume**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**IAutomaticUpdates::EnableService**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [**Proprietà IsHidden di IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > Amministratori, utenti e utenti esperti possono recuperare i valori della proprietà [**IsHidden di IUpdate.**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) Tuttavia, solo gli amministratori e gli utenti esperti possono impostare i valori.

     

-   [**IUpdate::AcceptEula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > Gli amministratori e gli utenti esperti possono chiamare [**il metodo AcceptEula di IUpdate.**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)

     

-   [**IAutomaticUpdatesSettings::Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [**Proprietà NotificationLevel di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > Amministratori, utenti e utenti esperti possono recuperare i valori della [**proprietà NotificationLevel di IAutomaticUpdatesSettings.**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel) Tuttavia, solo gli amministratori possono impostare i valori.

     

-   [**Proprietà ScheduledInstallationDay di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > Amministratori, utenti e utenti esperti possono recuperare i valori della [**proprietà ScheduledInstallationDay di IAutomaticUpdatesSettings.**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) Tuttavia, solo gli amministratori possono impostare i valori.

     

-   [**Proprietà ScheduledInstallationTime di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > Amministratori, utenti e utenti esperti possono recuperare i valori della [**proprietà ScheduledInstallationTime di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). Tuttavia, solo gli amministratori possono impostare i valori.

     

-   [**Proprietà IncludeRecommendedUpdates di IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > Amministratori, utenti e utenti esperti possono recuperare i valori della [**proprietà IncludeRecommendedUpdates di IAutomaticUpdatesSettings2.**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates) Tuttavia, solo gli amministratori possono impostare i valori.

     

 

 



