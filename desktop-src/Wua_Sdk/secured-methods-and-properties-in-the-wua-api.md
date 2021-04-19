---
description: Quando WUA rileva che un chiamante non dispone dell'autorizzazione per accedere a un'interfaccia, a un metodo o a una proprietà, \_ viene restituito HRESULT E AccessDenied.
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: Sicurezza di interfacce, metodi e proprietà nell'API WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307585"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a>Sicurezza di interfacce, metodi e proprietà nell'API WUA

Alcune interfacce, metodi e proprietà di Windows Update Agent (WUA) sono accessibili solo ai chiamanti che appartengono ai gruppi di sicurezza di Windows seguenti:

-   Amministratore
-   User
-   Utente esperto

Quando WUA rileva che un chiamante non dispone dell'autorizzazione per accedere a un'interfaccia, a un metodo o a  una proprietà, \_ viene restituito HRESULT E AccessDenied.

Le interfacce seguenti sono disponibili per i gruppi di sicurezza Administrator, User e Power User:

-   [**IAutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [**IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [**ISystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) e [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)

> [!Note]  
> Se le condizioni seguenti sono vere, la ricerca ha esito negativo:
>
> -   Un utente che non è un amministratore imposta la [**Proprietà UserLocale dell'interfaccia IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) sulle impostazioni locali che corrispondono a una lingua non installata nel computer.
> -   La ricerca usa un oggetto UpdateSearch creato dall'oggetto UpdateSession.

 

Le interfacce e i metodi di download seguenti sono disponibili per i gruppi Administrator e Power User:

-   [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [**IUpdate:: CopyFromCache**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IAutomaticUpdatesSettings2:: CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > Gli amministratori, gli utenti e gli utenti esperti possono chiamare [**IAutomaticUpdatesSettings2:: CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).

     

Le interfacce, i metodi e le proprietà di installazione seguenti sono disponibili per i gruppi di amministratori:

-   [**IAutomaticUpdates::P ause**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**IAutomaticUpdates:: Resume**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**IAutomaticUpdates::EnableService**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [**Proprietà Hidden di IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > Gli amministratori, gli utenti e gli utenti esperti possono recuperare i valori della [**Proprietà inhidden di IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden). Tuttavia, solo gli amministratori e gli utenti Power possono impostare i valori.

     

-   [**IUpdate:: AcceptEula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > Gli amministratori e gli utenti avanzati possono chiamare il [**Metodo AcceptEULA di IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).

     

-   [**IAutomaticUpdatesSettings:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [**Proprietà NotificationLevel di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > Gli amministratori, gli utenti e gli utenti esperti possono recuperare i valori della [**Proprietà NotificationLevel di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel). Tuttavia, solo gli amministratori possono impostare i valori.

     

-   [**Proprietà ScheduledInstallationDay di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > Gli amministratori, gli utenti e gli utenti esperti possono recuperare i valori della [**Proprietà ScheduledInstallationDay di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday). Tuttavia, solo gli amministratori possono impostare i valori.

     

-   [**Proprietà ScheduledInstallationTime di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > Gli amministratori, gli utenti e gli utenti esperti possono recuperare i valori della [**Proprietà ScheduledInstallationTime di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). Tuttavia, solo gli amministratori possono impostare i valori.

     

-   [**Proprietà IncludeRecommendedUpdates di IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > Gli amministratori, gli utenti e gli utenti esperti possono recuperare i valori della [**Proprietà IncludeRecommendedUpdates di IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates). Tuttavia, solo gli amministratori possono impostare i valori.

     

 

 



