---
title: Tipo di file e modello di associazioni URI
description: Tipo di file e modello di associazioni URI
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78540a072405aade01a9f94503999ad105d2078
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047498"
---
# <a name="file-type-and-uri-associations-model"></a><span data-ttu-id="6eb56-103">Tipo di file e modello di associazioni URI</span><span class="sxs-lookup"><span data-stu-id="6eb56-103">File type and URI associations model</span></span>

## <a name="platforms"></a><span data-ttu-id="6eb56-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="6eb56-104">Platforms</span></span>

 <span data-ttu-id="6eb56-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="6eb56-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="6eb56-106">**Server** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6eb56-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="6eb56-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6eb56-107">Description</span></span>

<span data-ttu-id="6eb56-108">Il tipo di file e il modello di associazione URI sono stati modificati in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6eb56-108">The file type and URI association model has changed in Windows 8.</span></span> <span data-ttu-id="6eb56-109">Le app non sono più in grado di impostarsi a livello di codice come gestore predefinito per un tipo di file o un URI.</span><span class="sxs-lookup"><span data-stu-id="6eb56-109">Apps are no longer able to programmatically set themselves as the default handler for a file type or URI.</span></span> <span data-ttu-id="6eb56-110">Al contrario, ora l'utente controlla sempre il tipo di gestore predefinito per un tipo di file o uno schema URI.</span><span class="sxs-lookup"><span data-stu-id="6eb56-110">Instead, now the user always controls what the default handler is for a file type or URI scheme.</span></span>

## <a name="manifestation"></a><span data-ttu-id="6eb56-111">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="6eb56-111">Manifestation</span></span>

<span data-ttu-id="6eb56-112">Il modo in cui questa modifica viene presentata all'utente dipende dal modo in cui viene progettata l'app, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6eb56-112">How this change presents to the user depends upon how the app is designed, for example:</span></span>

-   <span data-ttu-id="6eb56-113">Molte app verificano se sono l'impostazione predefinita ogni volta che vengono eseguite e, in caso contrario, richiedono all'utente di impostarle come predefinite.</span><span class="sxs-lookup"><span data-stu-id="6eb56-113">Many apps check to see if they are the default every time they run and, if they are not, they prompt the user to set them as default.</span></span> <span data-ttu-id="6eb56-114">Tuttavia, poiché le app non possono più eseguire query in modo accurato per determinare quale app è il gestore predefinito per un tipo di file o uno schema URI, nessuna di queste operazioni funziona.</span><span class="sxs-lookup"><span data-stu-id="6eb56-114">However, because apps can no longer accurately query to determine which app is the default handler for a file type or URI scheme, neither of these operations works.</span></span>
-   <span data-ttu-id="6eb56-115">Molte app hanno una finestra di dialogo o un menu incorporato o nel programma di installazione che specifica i tipi di file per i quali l'app deve fungere da impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6eb56-115">Many apps have a dialog box or menu built in or in their installer that specifies the file types for which the app should serve as the default.</span></span> <span data-ttu-id="6eb56-116">Tuttavia, poiché le app non possono più essere impostate a livello di codice come gestore predefinito per un tipo di file o uno schema URI, questo non funziona più.</span><span class="sxs-lookup"><span data-stu-id="6eb56-116">However, because apps can no longer programmatically set themselves as the default handler for a file type or URI scheme, this no longer works.</span></span>

## <a name="mitigation"></a><span data-ttu-id="6eb56-117">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="6eb56-117">Mitigation</span></span>

<span data-ttu-id="6eb56-118">Sono disponibili diverse operazioni che gli utenti possono eseguire per gestire le modifiche:</span><span class="sxs-lookup"><span data-stu-id="6eb56-118">There are several things users can do to accommodate these changes:</span></span>

-   <span data-ttu-id="6eb56-119">Agli utenti viene richiesto di scegliere un'app predefinita per gestire i tipi di file, gli schemi URI o entrambi quando non ne è stato specificato uno.</span><span class="sxs-lookup"><span data-stu-id="6eb56-119">Users are prompted contextually to choose a default app to handle file types, URI schemes, or both when one has not been specified</span></span>
-   <span data-ttu-id="6eb56-120">Agli utenti viene offerta la possibilità di modificare il gestore predefinito dopo l'installazione di nuove app in grado di gestire un tipo di file o uno schema URI</span><span class="sxs-lookup"><span data-stu-id="6eb56-120">Users are offered the option to change their default handler after installing new apps that can handle a file type or URI scheme</span></span>
-   <span data-ttu-id="6eb56-121">Il pannello di controllo programmi predefiniti consente agli utenti di impostare le impostazioni predefinite per un'app o per un tipo di file, uno schema URI o entrambi. le app possono essere collegate al pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="6eb56-121">The default programs control panel allows users to set defaults for an app, or for a file type, URI scheme, or both; apps can link to the control panel</span></span>
-   <span data-ttu-id="6eb56-122">Le impostazioni predefinite possono essere modificate da Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="6eb56-122">Defaults can be changed from Windows Explorer</span></span>

## <a name="solution"></a><span data-ttu-id="6eb56-123">Soluzione</span><span class="sxs-lookup"><span data-stu-id="6eb56-123">Solution</span></span>

<span data-ttu-id="6eb56-124">In seguito a queste modifiche, viene fornita questa guida sull'API:</span><span class="sxs-lookup"><span data-stu-id="6eb56-124">As a result of these changes, this API guidance is provided:</span></span>

-   <span data-ttu-id="6eb56-125">La funzionalità di alcune chiamate al metodo all'interno dell'API [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) è cambiata e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="6eb56-125">The functionality of some method calls within the [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) API has changed, and should no longer be used.</span></span>

    -   <span data-ttu-id="6eb56-126">**Non chiamare** [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) per determinare se un'app è l'impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="6eb56-126">**Do not** call [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault)/[QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) to determine if an app is the default</span></span>
    -   <span data-ttu-id="6eb56-127">**Non** chiamare [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) per determinare quale applicazione (se presente) è l'impostazione predefinita corrente</span><span class="sxs-lookup"><span data-stu-id="6eb56-127">**Do not** call [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) to determine which app (if any) is the current default</span></span>
    -   <span data-ttu-id="6eb56-128">**Non chiamare** [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) per impostare l'app predefinita</span><span class="sxs-lookup"><span data-stu-id="6eb56-128">**Do not** call [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault)/[SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) to set the default app</span></span>

-   <span data-ttu-id="6eb56-129">Il materiale sussidiario in futuro è:</span><span class="sxs-lookup"><span data-stu-id="6eb56-129">The guidance going forward is:</span></span>

    -   <span data-ttu-id="6eb56-130">**Non eseguire una query per** vedere quale app è il gestore predefinito per i tipi di file o gli schemi URI</span><span class="sxs-lookup"><span data-stu-id="6eb56-130">**Do not** query to see which app is the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="6eb56-131">**Non** tentare di monitorare le modifiche nel gestore predefinito per i tipi di file o gli schemi URI</span><span class="sxs-lookup"><span data-stu-id="6eb56-131">**Do not** attempt to monitor changes in the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="6eb56-132">**Non** tentare di impostare un'app come gestore predefinito per i tipi di file o gli schemi URI</span><span class="sxs-lookup"><span data-stu-id="6eb56-132">**Do not** attempt to set an app as the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="6eb56-133">**Non** tentare di gestire i valori predefiniti per i tipi di file o gli schemi URI dall'interno di un'app</span><span class="sxs-lookup"><span data-stu-id="6eb56-133">**Do not** attempt to manage defaults for file types or URI schemes from within an app</span></span>

    -   <span data-ttu-id="6eb56-134">**Eseguire** l'integrazione con il pannello di controllo [Imposta programmi predefiniti](../shell/default-programs.md) se si vuole consentire agli utenti dell'app di accedere all'interfaccia utente di gestione predefinita (l'interfaccia utente di gestione all'interno dell'app non è più supportata)</span><span class="sxs-lookup"><span data-stu-id="6eb56-134">**Do** integrate with the [Set Default Programs](../shell/default-programs.md) control panel if you want to allow users of your app to access the default management UI (the management UI within the app is no longer supported)</span></span>

        -   <span data-ttu-id="6eb56-135">La chiamata a [IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) consente all'utente di accedere alla pagina del pannello di controllo '[Imposta programmi predefiniti](../shell/default-programs.md)' per l'app specificata</span><span class="sxs-lookup"><span data-stu-id="6eb56-135">Calling [IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) allows the user to access the ‘[Set Default Programs](../shell/default-programs.md)’ control panel page for the specified app</span></span>

## <a name="tests"></a><span data-ttu-id="6eb56-136">Test</span><span class="sxs-lookup"><span data-stu-id="6eb56-136">Tests</span></span>

-   <span data-ttu-id="6eb56-137">Eseguire un test per verificare che le app vengano registrate correttamente nel pannello di controllo Imposta programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="6eb56-137">Test to verify that apps register properly in Set Default Programs control panel</span></span>
-   <span data-ttu-id="6eb56-138">Eseguire un test per verificare che le app vengano registrate correttamente per essere visualizzate nell'elenco OpenWith per i tipi di file, gli schemi URI o entrambi, che si registrano per gestire</span><span class="sxs-lookup"><span data-stu-id="6eb56-138">Test to verify that apps register properly to appear in the OpenWith list for the file types, URI schemes, or both, that they register to handle</span></span>
-   <span data-ttu-id="6eb56-139">Eseguire un test per verificare che le nuove notifiche dell'app vengano visualizzate dopo l'installazione dell'app e che l'utente richiami un tipo di file, uno schema URI o entrambi, che l'app sia stata registrata per gestire</span><span class="sxs-lookup"><span data-stu-id="6eb56-139">Test to verify that new app notifications appear after your app is installed and the user invokes a file type, URI scheme, or both, that your app has registered to handle</span></span>

## <a name="resources"></a><span data-ttu-id="6eb56-140">Risorse</span><span class="sxs-lookup"><span data-stu-id="6eb56-140">Resources</span></span>

-   <span data-ttu-id="6eb56-141">[Procedure consigliate per il tipo di file e le associazioni URI nelle applicazioni desktop di Windows 8](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6eb56-141">[Best Practices for File Type and URI Associations in Windows 8 Desktop Apps](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span></span>
-   [<span data-ttu-id="6eb56-142">Associazioni del tipo di file e presentazione della conferenza di compilazione AutoPlay</span><span class="sxs-lookup"><span data-stu-id="6eb56-142">File Type Associations and AutoPlay Build Conference Presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 