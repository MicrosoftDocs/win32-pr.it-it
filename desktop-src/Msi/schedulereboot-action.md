---
description: Inserire l'azione ScheduleReboot nella sequenza di azione per richiedere all'utente il riavvio del sistema alla fine dell'installazione. Usare l'azione ForceReboot per richiedere un riavvio durante l'installazione.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Azione ScheduleReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881841"
---
# <a name="schedulereboot-action"></a><span data-ttu-id="3acac-104">Azione ScheduleReboot</span><span class="sxs-lookup"><span data-stu-id="3acac-104">ScheduleReboot Action</span></span>

<span data-ttu-id="3acac-105">Inserire l'azione ScheduleReboot nella sequenza di azione per richiedere all'utente il riavvio del sistema alla fine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="3acac-105">Insert the ScheduleReboot action into the action sequence to prompt the user for a restart of the system at the end of the installation.</span></span> <span data-ttu-id="3acac-106">Usare l' [azione ForceReboot](forcereboot-action.md) per richiedere un riavvio durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="3acac-106">Use the [ForceReboot action](forcereboot-action.md) to prompt for a restart during installation.</span></span>

<span data-ttu-id="3acac-107">Se l'installazione ha un'interfaccia utente, il programma di installazione visualizza una finestra di messaggio e un pulsante alla fine dell'installazione che chiede se l'utente vuole riavviare il sistema.</span><span class="sxs-lookup"><span data-stu-id="3acac-107">If the installation has a user interface, the installer displays a message box and button at the end of installation asking whether the user wants to restart the system.</span></span> <span data-ttu-id="3acac-108">Prima di completare l'installazione, l'utente deve rispondere a questa richiesta.</span><span class="sxs-lookup"><span data-stu-id="3acac-108">The user must respond to this prompt before completing installation.</span></span> <span data-ttu-id="3acac-109">Se l'installazione non ha un'interfaccia utente, il sistema viene riavviato automaticamente alla fine.</span><span class="sxs-lookup"><span data-stu-id="3acac-109">If the installation has no user interface, the system automatically restarts at the end.</span></span>

<span data-ttu-id="3acac-110">Se il programma di installazione determina che è necessario un riavvio, viene automaticamente richiesto all'utente di riavviare al termine dell'installazione, indipendentemente dal fatto che siano presenti azioni ForceReboot o ScheduleReboot nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="3acac-110">If the installer determines that a restart is necessary it automatically prompts the user to restart at the end of the installation, whether or not there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="3acac-111">Ad esempio, il programma di installazione richiede automaticamente un riavvio se è necessario sostituire i file in uso durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="3acac-111">For example, the installer automatically prompts for a restart if it needs to replace any files that are in use during installation.</span></span>

<span data-ttu-id="3acac-112">È possibile disattivare determinate richieste di [**riavvio**](reboot.md) impostando la proprietà restart.</span><span class="sxs-lookup"><span data-stu-id="3acac-112">You can suppress certain prompts for restarts by setting the [**REBOOT**](reboot.md) property.</span></span>

<span data-ttu-id="3acac-113">Se il Windows Installer rileva l'azione [ForceReboot](forcereboot-action.md) o ScheduleReboot durante un'installazione con [più pacchetti](multiple-package-installations.md), il programma di installazione arresterà e eseguirà il rollback dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="3acac-113">If the Windows Installer encounters the [ForceReboot](forcereboot-action.md) or ScheduleReboot action during a [multiple-package installation](multiple-package-installations.md), the installer will stop and roll back the installation.</span></span> <span data-ttu-id="3acac-114">È possibile installare altri pacchetti che appartengono all'installazione con più pacchetti, che non contengono un'azione ForceReboot o ScheduleReboot.</span><span class="sxs-lookup"><span data-stu-id="3acac-114">Other packages belonging to the multiple-package installation, that do not contain a ForceReboot or ScheduleReboot action, can be installed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3acac-115">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="3acac-115">Sequence Restrictions</span></span>

<span data-ttu-id="3acac-116">Non esistono restrizioni di sequenza.</span><span class="sxs-lookup"><span data-stu-id="3acac-116">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3acac-117">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="3acac-117">ActionData Messages</span></span>

<span data-ttu-id="3acac-118">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="3acac-118">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="3acac-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3acac-119">Remarks</span></span>

<span data-ttu-id="3acac-120">Ad esempio, questa azione può essere usata per forzare il programma di installazione a richiedere un riavvio dopo l'installazione dei driver che richiedono un riavvio.</span><span class="sxs-lookup"><span data-stu-id="3acac-120">For example, this action can be used to force the installer to prompt for a restart after installing drivers that require a restart.</span></span> <span data-ttu-id="3acac-121">Se il programma di installazione tenta di sostituire i file in uso, viene automaticamente richiesto di riavviare l'utente anche se ScheduleReboot non è stato usato.</span><span class="sxs-lookup"><span data-stu-id="3acac-121">If the installer attempts to replace files that are in use, it automatically prompts the user to restart even if ScheduleReboot has not been used.</span></span>

<span data-ttu-id="3acac-122">L'azione ScheduleReboot viene in genere posizionata alla fine della sequenza, ma può essere inserita in qualsiasi punto della sequenza.</span><span class="sxs-lookup"><span data-stu-id="3acac-122">The ScheduleReboot action is typically placed at the end of the sequence, but it can be inserted at any point in the sequence.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3acac-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3acac-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3acac-124">Riavvio del sistema</span><span class="sxs-lookup"><span data-stu-id="3acac-124">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 



