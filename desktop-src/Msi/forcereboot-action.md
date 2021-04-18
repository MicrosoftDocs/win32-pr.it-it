---
description: L'azione ForceReboot chiede all'utente di riavviare il sistema durante l'installazione.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: Azione ForceReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807bab474f1faacfbc7684797b7a0b7b74f354d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314272"
---
# <a name="forcereboot-action"></a><span data-ttu-id="b4542-103">Azione ForceReboot</span><span class="sxs-lookup"><span data-stu-id="b4542-103">ForceReboot Action</span></span>

<span data-ttu-id="b4542-104">L'azione ForceReboot chiede all'utente di riavviare il sistema durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="b4542-104">The ForceReboot action prompts the user for a restart of the system during the installation.</span></span> <span data-ttu-id="b4542-105">L'azione ForceReboot è diversa dall' [azione ScheduleReboot](schedulereboot-action.md) in quanto l'azione ScheduleReboot viene utilizzata per pianificare una richiesta di riavvio al termine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="b4542-105">The ForceReboot action is different from the [ScheduleReboot action](schedulereboot-action.md) in that the ScheduleReboot action is used to schedule a prompt to restart at the end of the installation.</span></span>

<span data-ttu-id="b4542-106">Se l'installazione ha un'interfaccia utente, il programma di installazione visualizza una finestra di dialogo in ogni azione ForceReboot che richiede all'utente di riavviare il sistema.</span><span class="sxs-lookup"><span data-stu-id="b4542-106">If the installation has a user interface, the installer displays a dialog box at each ForceReboot action which prompts the user to restart the system.</span></span> <span data-ttu-id="b4542-107">Prima di continuare con l'installazione, l'utente deve rispondere a questa richiesta.</span><span class="sxs-lookup"><span data-stu-id="b4542-107">The user must respond to this prompt before continuing with the installation.</span></span> <span data-ttu-id="b4542-108">Se l'installazione non ha un'interfaccia utente, il sistema viene riavviato automaticamente all'azione ForceReboot.</span><span class="sxs-lookup"><span data-stu-id="b4542-108">If the installation has no user interface, the system automatically restarts at the ForceReboot action.</span></span>

<span data-ttu-id="b4542-109">Se il programma di installazione determina che è necessario un riavvio, viene automaticamente richiesto all'utente di riavviare al termine dell'installazione, indipendentemente dal fatto che siano presenti azioni ForceReboot o ScheduleReboot nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="b4542-109">If the installer determines that a restart is necessary, it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="b4542-110">Ad esempio, il programma di installazione richiede automaticamente un riavvio se è necessario sostituire eventuali file utilizzati durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="b4542-110">For example, the installer automatically prompts for a restart if it needs to replace any files used during the installation.</span></span>

<span data-ttu-id="b4542-111">Non visualizzare alcune richieste di riavvio impostando la proprietà [**reboot**](reboot.md) .</span><span class="sxs-lookup"><span data-stu-id="b4542-111">Suppress certain restart prompts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="b4542-112">Se il Windows Installer rileva l'azione ForceReboot o [ScheduleReboot](schedulereboot-action.md) durante un'installazione con [più pacchetti](multiple-package-installations.md), il programma di installazione arresterà e eseguirà il rollback dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="b4542-112">If the Windows Installer encounters the ForceReboot or [ScheduleReboot](schedulereboot-action.md) action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="b4542-113">È possibile installare altri pacchetti che appartengono all'installazione con più pacchetti, che non contengono un'azione ForceReboot o ScheduleReboot.</span><span class="sxs-lookup"><span data-stu-id="b4542-113">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b4542-114">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="b4542-114">Sequence Restrictions</span></span>

<span data-ttu-id="b4542-115">Le azioni seguenti si verificano comunemente insieme come un gruppo nella sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="b4542-115">The following actions commonly occur together as a group in the action sequence.</span></span> <span data-ttu-id="b4542-116">È consigliabile che l'azione ForceReboot venga pianificata per essere eseguita dopo questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="b4542-116">It is recommended that the ForceReboot action be scheduled to come after this group.</span></span> <span data-ttu-id="b4542-117">Se l'azione ForceReboot è stata pianificata prima dell' [azione RegisterProduct](registerproduct-action.md), il programma di installazione richiede nuovamente l'origine del pacchetto di installazione dopo il riavvio.</span><span class="sxs-lookup"><span data-stu-id="b4542-117">If the ForceReboot action is scheduled before the [RegisterProduct action](registerproduct-action.md), the installer again requires the source of the installation package after the restart.</span></span> <span data-ttu-id="b4542-118">La sequenza preferita per ForceReboot si trova quindi immediatamente dopo questa sequenza di azioni.</span><span class="sxs-lookup"><span data-stu-id="b4542-118">Therefore, the preferred sequence for ForceReboot is immediately following this action sequence.</span></span>

-   [<span data-ttu-id="b4542-119">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="b4542-119">RegisterProduct</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="b4542-120">RegisterUser</span><span class="sxs-lookup"><span data-stu-id="b4542-120">RegisterUser</span></span>](registeruser-action.md)
-   [<span data-ttu-id="b4542-121">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="b4542-121">PublishProduct</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="b4542-122">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="b4542-122">PublishFeatures</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="b4542-123">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="b4542-123">CreateShortcuts</span></span>](createshortcuts-action.md)
-   [<span data-ttu-id="b4542-124">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="b4542-124">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)
-   [<span data-ttu-id="b4542-125">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="b4542-125">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="b4542-126">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="b4542-126">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="b4542-127">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="b4542-127">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="b4542-128">L'azione ForceReboot deve essere compresa tra [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) nella sequenza di azione della [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b4542-128">The ForceReboot action must come between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the action sequence of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b4542-129">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="b4542-129">ActionData Messages</span></span>

<span data-ttu-id="b4542-130">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="b4542-130">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4542-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4542-131">Remarks</span></span>

<span data-ttu-id="b4542-132">L'azione ForceReboot deve sempre essere utilizzata con un'istruzione condizionale in modo che il programma di installazione avvii un riavvio solo quando necessario.</span><span class="sxs-lookup"><span data-stu-id="b4542-132">The ForceReboot action must always be used with a conditional statement such that the installer triggers a restart only when necessary.</span></span> <span data-ttu-id="b4542-133">Ad esempio, è possibile che sia necessario un riavvio solo se viene sostituito un particolare file o se è installato un particolare componente.</span><span class="sxs-lookup"><span data-stu-id="b4542-133">For example, a restart may only be required if a particular file is replaced or a particular component is installed.</span></span> <span data-ttu-id="b4542-134">Ogni installazione del prodotto è univoca ed è possibile che sia necessaria un'azione personalizzata per determinare se è necessario un riavvio.</span><span class="sxs-lookup"><span data-stu-id="b4542-134">Each product installation is unique and a custom action may be required to determine whether a restart is needed.</span></span> <span data-ttu-id="b4542-135">La condizione sull'azione ForceReboot USA in genere la proprietà [**AFTERREBOOT**](afterreboot.md) .</span><span class="sxs-lookup"><span data-stu-id="b4542-135">The condition on the ForceReboot action commonly makes use of the [**AFTERREBOOT**](afterreboot.md) property.</span></span>

<span data-ttu-id="b4542-136">ForceReboot esegue le operazioni di sistema generate da qualsiasi azione precedente prima di richiedere un riavvio o un riavvio.</span><span class="sxs-lookup"><span data-stu-id="b4542-136">ForceReboot runs system operations generated by any previous actions before prompting for a restart or restarting.</span></span> <span data-ttu-id="b4542-137">Ad esempio, le operazioni di sistema generate da [InstallFiles](installfiles-action.md) e [WriteRegistryValori consente](writeregistryvalues-action.md) vengono eseguite prima di un riavvio.</span><span class="sxs-lookup"><span data-stu-id="b4542-137">For example, the system operations generated by [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) are run before a restart.</span></span>

<span data-ttu-id="b4542-138">L'azione ForceReboot scrive una chiave del registro di sistema che determina l'avvio del programma di installazione dopo il riavvio.</span><span class="sxs-lookup"><span data-stu-id="b4542-138">The ForceReboot action writes a registry key that causes the installer to start after restarting.</span></span> <span data-ttu-id="b4542-139">Il percorso di questa chiave è **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**.</span><span class="sxs-lookup"><span data-stu-id="b4542-139">The location of this key is **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\RunOnce**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4542-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b4542-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4542-141">Riavvio del sistema</span><span class="sxs-lookup"><span data-stu-id="b4542-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 



