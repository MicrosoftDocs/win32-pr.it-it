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
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a><span data-ttu-id="c366b-103">Sicurezza di interfacce, metodi e proprietà nell'API WUA</span><span class="sxs-lookup"><span data-stu-id="c366b-103">Securing Interfaces, Methods, and Properties in the WUA API</span></span>

<span data-ttu-id="c366b-104">Alcune interfacce, metodi e proprietà di Windows Update Agent (WUA) sono accessibili solo ai chiamanti che appartengono ai gruppi di sicurezza di Windows seguenti:</span><span class="sxs-lookup"><span data-stu-id="c366b-104">Some interfaces, methods, and properties of Windows Update Agent (WUA) are accessible only to callers who belong to the following Windows security groups:</span></span>

-   <span data-ttu-id="c366b-105">Amministratore</span><span class="sxs-lookup"><span data-stu-id="c366b-105">Administrator</span></span>
-   <span data-ttu-id="c366b-106">User</span><span class="sxs-lookup"><span data-stu-id="c366b-106">User</span></span>
-   <span data-ttu-id="c366b-107">Utente esperto</span><span class="sxs-lookup"><span data-stu-id="c366b-107">Power User</span></span>

<span data-ttu-id="c366b-108">Quando WUA rileva che un chiamante non dispone dell'autorizzazione per accedere a un'interfaccia, a un metodo o a  una proprietà, \_ viene restituito HRESULT E AccessDenied.</span><span class="sxs-lookup"><span data-stu-id="c366b-108">When WUA detects that a caller does not have permission to access an interface, method, or property, the **HRESULT** E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="c366b-109">Le interfacce seguenti sono disponibili per i gruppi di sicurezza Administrator, User e Power User:</span><span class="sxs-lookup"><span data-stu-id="c366b-109">The following interfaces are available to the Administrator, User, and Power User security groups:</span></span>

-   [<span data-ttu-id="c366b-110">**IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="c366b-110">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="c366b-111">**IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="c366b-111">**IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [<span data-ttu-id="c366b-112">**IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="c366b-112">**IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [<span data-ttu-id="c366b-113">**ISystemInformation**</span><span class="sxs-lookup"><span data-stu-id="c366b-113">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [<span data-ttu-id="c366b-114">**IUpdateSearcher**</span><span class="sxs-lookup"><span data-stu-id="c366b-114">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   <span data-ttu-id="c366b-115">[**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) e [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span><span class="sxs-lookup"><span data-stu-id="c366b-115">[**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) and [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span></span>

> [!Note]  
> <span data-ttu-id="c366b-116">Se le condizioni seguenti sono vere, la ricerca ha esito negativo:</span><span class="sxs-lookup"><span data-stu-id="c366b-116">If the following conditions are true, a search fails:</span></span>
>
> -   <span data-ttu-id="c366b-117">Un utente che non è un amministratore imposta la [**Proprietà UserLocale dell'interfaccia IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) sulle impostazioni locali che corrispondono a una lingua non installata nel computer.</span><span class="sxs-lookup"><span data-stu-id="c366b-117">A user who is not an administrator sets the [**UserLocale property of the IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) interface to a locale that corresponds to a language that is not installed on the computer.</span></span>
> -   <span data-ttu-id="c366b-118">La ricerca usa un oggetto UpdateSearch creato dall'oggetto UpdateSession.</span><span class="sxs-lookup"><span data-stu-id="c366b-118">The search uses an UpdateSearch object created from the UpdateSession object.</span></span>

 

<span data-ttu-id="c366b-119">Le interfacce e i metodi di download seguenti sono disponibili per i gruppi Administrator e Power User:</span><span class="sxs-lookup"><span data-stu-id="c366b-119">The following download interfaces and methods are available to the Administrator and Power User groups:</span></span>

-   [<span data-ttu-id="c366b-120">**IUpdateDownloader**</span><span class="sxs-lookup"><span data-stu-id="c366b-120">**IUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [<span data-ttu-id="c366b-121">**IUpdate:: CopyFromCache**</span><span class="sxs-lookup"><span data-stu-id="c366b-121">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="c366b-122">**IAutomaticUpdatesSettings2:: CheckPermission**</span><span class="sxs-lookup"><span data-stu-id="c366b-122">**IAutomaticUpdatesSettings2::CheckPermission**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > <span data-ttu-id="c366b-123">Gli amministratori, gli utenti e gli utenti esperti possono chiamare [**IAutomaticUpdatesSettings2:: CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).</span><span class="sxs-lookup"><span data-stu-id="c366b-123">Administrators, users, and power users can call [**IAutomaticUpdatesSettings2::CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).</span></span>

     

<span data-ttu-id="c366b-124">Le interfacce, i metodi e le proprietà di installazione seguenti sono disponibili per i gruppi di amministratori:</span><span class="sxs-lookup"><span data-stu-id="c366b-124">The following installation interfaces, methods, and properties are available to the Administrator groups:</span></span>

-   [<span data-ttu-id="c366b-125">**IAutomaticUpdates::P ause**</span><span class="sxs-lookup"><span data-stu-id="c366b-125">**IAutomaticUpdates::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="c366b-126">**IAutomaticUpdates:: Resume**</span><span class="sxs-lookup"><span data-stu-id="c366b-126">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="c366b-127">**IAutomaticUpdates::EnableService**</span><span class="sxs-lookup"><span data-stu-id="c366b-127">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="c366b-128">**IUpdateInstaller**</span><span class="sxs-lookup"><span data-stu-id="c366b-128">**IUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [<span data-ttu-id="c366b-129">**Proprietà Hidden di IUpdate**</span><span class="sxs-lookup"><span data-stu-id="c366b-129">**IsHidden Property of IUpdate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > <span data-ttu-id="c366b-130">Gli amministratori, gli utenti e gli utenti esperti possono recuperare i valori della [**Proprietà inhidden di IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden).</span><span class="sxs-lookup"><span data-stu-id="c366b-130">Administrators, users, and power users can retrieve the values of the [**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden).</span></span> <span data-ttu-id="c366b-131">Tuttavia, solo gli amministratori e gli utenti Power possono impostare i valori.</span><span class="sxs-lookup"><span data-stu-id="c366b-131">However, only administrators and power users can set the values.</span></span>

     

-   [<span data-ttu-id="c366b-132">**IUpdate:: AcceptEula**</span><span class="sxs-lookup"><span data-stu-id="c366b-132">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > <span data-ttu-id="c366b-133">Gli amministratori e gli utenti avanzati possono chiamare il [**Metodo AcceptEULA di IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).</span><span class="sxs-lookup"><span data-stu-id="c366b-133">Administrators and power users can call the [**AcceptEula method of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).</span></span>

     

-   [<span data-ttu-id="c366b-134">**IAutomaticUpdatesSettings:: Save**</span><span class="sxs-lookup"><span data-stu-id="c366b-134">**IAutomaticUpdatesSettings::Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [<span data-ttu-id="c366b-135">**Proprietà NotificationLevel di IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="c366b-135">**NotificationLevel Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > <span data-ttu-id="c366b-136">Gli amministratori, gli utenti e gli utenti esperti possono recuperare i valori della [**Proprietà NotificationLevel di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel).</span><span class="sxs-lookup"><span data-stu-id="c366b-136">Administrators, users, and power users can retrieve the values of the [**NotificationLevel Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel).</span></span> <span data-ttu-id="c366b-137">Tuttavia, solo gli amministratori possono impostare i valori.</span><span class="sxs-lookup"><span data-stu-id="c366b-137">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="c366b-138">**Proprietà ScheduledInstallationDay di IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="c366b-138">**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > <span data-ttu-id="c366b-139">Gli amministratori, gli utenti e gli utenti esperti possono recuperare i valori della [**Proprietà ScheduledInstallationDay di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday).</span><span class="sxs-lookup"><span data-stu-id="c366b-139">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday).</span></span> <span data-ttu-id="c366b-140">Tuttavia, solo gli amministratori possono impostare i valori.</span><span class="sxs-lookup"><span data-stu-id="c366b-140">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="c366b-141">**Proprietà ScheduledInstallationTime di IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="c366b-141">**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > <span data-ttu-id="c366b-142">Gli amministratori, gli utenti e gli utenti esperti possono recuperare i valori della [**Proprietà ScheduledInstallationTime di IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span><span class="sxs-lookup"><span data-stu-id="c366b-142">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="c366b-143">Tuttavia, solo gli amministratori possono impostare i valori.</span><span class="sxs-lookup"><span data-stu-id="c366b-143">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="c366b-144">**Proprietà IncludeRecommendedUpdates di IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="c366b-144">**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > <span data-ttu-id="c366b-145">Gli amministratori, gli utenti e gli utenti esperti possono recuperare i valori della [**Proprietà IncludeRecommendedUpdates di IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates).</span><span class="sxs-lookup"><span data-stu-id="c366b-145">Administrators, users, and power users can retrieve the values of the [**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates).</span></span> <span data-ttu-id="c366b-146">Tuttavia, solo gli amministratori possono impostare i valori.</span><span class="sxs-lookup"><span data-stu-id="c366b-146">However, only administrators can set the values.</span></span>

     

 

 



