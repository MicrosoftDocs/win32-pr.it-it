---
description: In alcuni casi, un utente che non è un amministratore di sistema può solo ignorare un elenco approvato di proprietà pubbliche con restrizioni Windows Installer.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Proprietà pubbliche limitate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315893"
---
# <a name="restricted-public-properties"></a><span data-ttu-id="670e1-103">Proprietà pubbliche limitate</span><span class="sxs-lookup"><span data-stu-id="670e1-103">Restricted Public Properties</span></span>

<span data-ttu-id="670e1-104">Nel caso di un'installazione gestita, l'autore del pacchetto potrebbe dover limitare le [proprietà pubbliche](public-properties.md) che vengono passate al lato server e possono essere modificate da un utente che non è un amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="670e1-104">In the case of a managed installation, the package author may need to limit which [public properties](public-properties.md) are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="670e1-105">Alcune restrizioni sono in genere necessarie per mantenere un ambiente protetto quando l'installazione richiede che il programma di installazione utilizzi privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="670e1-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span> <span data-ttu-id="670e1-106">Se vengono soddisfatte tutte le condizioni seguenti, un utente che non è un amministratore di sistema può solo eseguire l'override di un elenco approvato di proprietà pubbliche limitate:</span><span class="sxs-lookup"><span data-stu-id="670e1-106">If all of the following conditions are met, a user that is not a system administrator can only override an approved list of restricted public properties:</span></span>

-   <span data-ttu-id="670e1-107">Il sistema è Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="670e1-107">The system is Windows 2000.</span></span>
-   <span data-ttu-id="670e1-108">L'utente non è un amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="670e1-108">The user is not a system administrator.</span></span>
-   <span data-ttu-id="670e1-109">È in corso l'installazione dell'applicazione o del prodotto con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="670e1-109">The application or product is being installed with elevated privileges.</span></span>

<span data-ttu-id="670e1-110">Se tutte le condizioni precedenti sono vere, il programma di installazione viene impostato sul seguente elenco di proprietà pubbliche con restrizioni che possono essere modificate da qualsiasi utente:</span><span class="sxs-lookup"><span data-stu-id="670e1-110">If all of the above conditions are true, the installer defaults to the following list of restricted public properties that can be changed by any user:</span></span>

-   [<span data-ttu-id="670e1-111">**AZIONE**</span><span class="sxs-lookup"><span data-stu-id="670e1-111">**ACTION**</span></span>](action.md)
-   [<span data-ttu-id="670e1-112">**AFTERREBOOT**</span><span class="sxs-lookup"><span data-stu-id="670e1-112">**AFTERREBOOT**</span></span>](afterreboot.md)
-   [<span data-ttu-id="670e1-113">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="670e1-113">**ALLUSERS**</span></span>](allusers.md)
-   [<span data-ttu-id="670e1-114">**EXECUTEACTION**</span><span class="sxs-lookup"><span data-stu-id="670e1-114">**EXECUTEACTION**</span></span>](executeaction.md)
-   [<span data-ttu-id="670e1-115">**EXECUTEMODE**</span><span class="sxs-lookup"><span data-stu-id="670e1-115">**EXECUTEMODE**</span></span>](executemode.md)
-   [<span data-ttu-id="670e1-116">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="670e1-116">**FILEADDDEFAULT**</span></span>](fileadddefault.md)
-   [<span data-ttu-id="670e1-117">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="670e1-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="670e1-118">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="670e1-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="670e1-119">**INSTALLLEVEL**</span><span class="sxs-lookup"><span data-stu-id="670e1-119">**INSTALLLEVEL**</span></span>](installlevel.md)
-   [<span data-ttu-id="670e1-120">**LIMITUI**</span><span class="sxs-lookup"><span data-stu-id="670e1-120">**LIMITUI**</span></span>](limitui.md)
-   [<span data-ttu-id="670e1-121">**LOGACTION**</span><span class="sxs-lookup"><span data-stu-id="670e1-121">**LOGACTION**</span></span>](logaction.md)
-   [<span data-ttu-id="670e1-122">**NoCompanyName**</span><span class="sxs-lookup"><span data-stu-id="670e1-122">**NOCOMPANYNAME**</span></span>](nocompanyname.md)
-   [<span data-ttu-id="670e1-123">**NOUSERNAME**</span><span class="sxs-lookup"><span data-stu-id="670e1-123">**NOUSERNAME**</span></span>](nousername.md)
-   [<span data-ttu-id="670e1-124">**MSIENFORCEUPGRADECOMPONENTRULES**</span><span class="sxs-lookup"><span data-stu-id="670e1-124">**MSIENFORCEUPGRADECOMPONENTRULES**</span></span>](msienforceupgradecomponentrules.md)
-   [<span data-ttu-id="670e1-125">**MSIINSTANCEGUID**</span><span class="sxs-lookup"><span data-stu-id="670e1-125">**MSIINSTANCEGUID**</span></span>](msiinstanceguid.md)
-   [<span data-ttu-id="670e1-126">**MSINEWINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="670e1-126">**MSINEWINSTANCE**</span></span>](msinewinstance.md)
-   [<span data-ttu-id="670e1-127">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="670e1-127">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
-   [<span data-ttu-id="670e1-128">**PATCH**</span><span class="sxs-lookup"><span data-stu-id="670e1-128">**PATCH**</span></span>](patch.md)
-   [<span data-ttu-id="670e1-129">**PRIMARYFOLDER**</span><span class="sxs-lookup"><span data-stu-id="670e1-129">**PRIMARYFOLDER**</span></span>](primaryfolder.md)
-   [<span data-ttu-id="670e1-130">**PROMPTROLLBACKCOST**</span><span class="sxs-lookup"><span data-stu-id="670e1-130">**PROMPTROLLBACKCOST**</span></span>](promptrollbackcost.md)
-   [<span data-ttu-id="670e1-131">**RIAVVIO**</span><span class="sxs-lookup"><span data-stu-id="670e1-131">**REBOOT**</span></span>](reboot.md)
-   [<span data-ttu-id="670e1-132">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="670e1-132">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="670e1-133">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="670e1-133">**REINSTALLMODE**</span></span>](reinstallmode.md)
-   [<span data-ttu-id="670e1-134">**RIPRENDERE**</span><span class="sxs-lookup"><span data-stu-id="670e1-134">**RESUME**</span></span>](resume.md)
-   [<span data-ttu-id="670e1-135">**SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="670e1-135">**SEQUENCE**</span></span>](sequence.md)
-   [<span data-ttu-id="670e1-136">**SHORTFILENAMES**</span><span class="sxs-lookup"><span data-stu-id="670e1-136">**SHORTFILENAMES**</span></span>](shortfilenames.md)
-   [<span data-ttu-id="670e1-137">**TRASFORMA**</span><span class="sxs-lookup"><span data-stu-id="670e1-137">**TRANSFORMS**</span></span>](transforms.md)
-   [<span data-ttu-id="670e1-138">**TRANSFORMSATSOURCE**</span><span class="sxs-lookup"><span data-stu-id="670e1-138">**TRANSFORMSATSOURCE**</span></span>](transformsatsource.md)

<span data-ttu-id="670e1-139">L'autore di un pacchetto di installazione può estendere questo elenco predefinito per includere proprietà pubbliche aggiuntive tramite la proprietà [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="670e1-139">The author of an installation package can extend this default list to include additional public properties by using the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="670e1-140">Se si imposta la proprietà [**EnableUserControl**](-enableusercontrol.md) o il [criterio di sistema](system-policy.md) [EnableUserControl](enableusercontrol.md), l'elenco viene esteso a tutte le proprietà pubbliche.</span><span class="sxs-lookup"><span data-stu-id="670e1-140">Setting the [**EnableUserControl**](-enableusercontrol.md) property or the [EnableUserControl](enableusercontrol.md)[system policy](system-policy.md) extends the list to all public properties.</span></span> <span data-ttu-id="670e1-141">Tutti gli utenti possono quindi modificare qualsiasi proprietà pubblica.</span><span class="sxs-lookup"><span data-stu-id="670e1-141">All users can then change any public property.</span></span>

<span data-ttu-id="670e1-142">Il programma di installazione imposta la proprietà [**RestrictedUserControl**](restrictedusercontrol.md) ogni volta che l'elenco di proprietà pubbliche passato al server da utenti non amministratori è limitato.</span><span class="sxs-lookup"><span data-stu-id="670e1-142">The installer sets the [**RestrictedUserControl**](restrictedusercontrol.md) property whenever the list of public properties passed to the server by non-administrator users is restricted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="670e1-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="670e1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="670e1-144">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="670e1-144">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



