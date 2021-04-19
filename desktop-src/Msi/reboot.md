---
description: La proprietà restart disattiva alcune richieste di riavvio del sistema.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Riavvia proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94b08a04f3e95d873f6fc233185ce623cafc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329248"
---
# <a name="reboot-property"></a><span data-ttu-id="ed960-103">Riavvia proprietà</span><span class="sxs-lookup"><span data-stu-id="ed960-103">REBOOT property</span></span>

<span data-ttu-id="ed960-104">La proprietà restart disattiva alcune richieste **di riavvio del** sistema.</span><span class="sxs-lookup"><span data-stu-id="ed960-104">The **REBOOT** property suppresses certain prompts for a restart of the system.</span></span> <span data-ttu-id="ed960-105">Un amministratore usa in genere questa proprietà con una serie di installazioni per installare più prodotti contemporaneamente con un solo riavvio alla fine.</span><span class="sxs-lookup"><span data-stu-id="ed960-105">An administrator typically uses this property with a series of installations to install several products at the same time with only one restart at the end.</span></span> <span data-ttu-id="ed960-106">Per ulteriori informazioni, vedere [riavvii del sistema](system-reboots.md).</span><span class="sxs-lookup"><span data-stu-id="ed960-106">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="ed960-107">Le azioni [ForceReboot](forcereboot-action.md) e [ScheduleReboot](schedulereboot-action.md) indicano al programma di installazione di richiedere all'utente di riavviare il sistema.</span><span class="sxs-lookup"><span data-stu-id="ed960-107">The [ForceReboot](forcereboot-action.md) and [ScheduleReboot](schedulereboot-action.md) actions inform the installer to prompt the user to restart the system.</span></span> <span data-ttu-id="ed960-108">Il programma di installazione può inoltre determinare che è necessario un riavvio se nella sequenza sono presenti azioni ForceReboot o ScheduleReboot.</span><span class="sxs-lookup"><span data-stu-id="ed960-108">The installer can also determine that a restart is necessary whether there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="ed960-109">Ad esempio, il programma di installazione richiede automaticamente un riavvio se è necessario sostituire i file in uso durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ed960-109">For example, the installer automatically prompts for a restart if it needs to replace any files in use during the installation.</span></span>

<span data-ttu-id="ed960-110">È possibile disattivare determinate richieste per i riavvii impostando la proprietà **reboot** come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="ed960-110">You can suppress certain prompts for restarts by setting the **REBOOT** property as follows.</span></span>



| <span data-ttu-id="ed960-111">Valore di riavvio</span><span class="sxs-lookup"><span data-stu-id="ed960-111">REBOOT value</span></span>   | <span data-ttu-id="ed960-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed960-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed960-113">Force</span><span class="sxs-lookup"><span data-stu-id="ed960-113">Force</span></span>          | <span data-ttu-id="ed960-114">Richiedere sempre un riavvio al termine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="ed960-114">Always prompt for a restart at the end of the installation.</span></span> <span data-ttu-id="ed960-115">L'interfaccia utente chiede sempre all'utente di scegliere di riavviare alla fine.</span><span class="sxs-lookup"><span data-stu-id="ed960-115">The UI always prompts the user with an option to restart at the end.</span></span> <span data-ttu-id="ed960-116">Se non è presente alcuna interfaccia utente e non si tratta di un' [installazione a più pacchetti](multiple-package-installations.md), il sistema viene riavviato automaticamente al termine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="ed960-116">If there is no user interface, and this is not a [multiple-package installation](multiple-package-installations.md), the system automatically restarts at the end of the installation.</span></span> <span data-ttu-id="ed960-117">Se si tratta di un'installazione con più pacchetti, non viene eseguito il riavvio automatico del sistema e il programma di installazione restituisce un errore di \_ \_ riavvio \_ necessario.</span><span class="sxs-lookup"><span data-stu-id="ed960-117">If this is a multiple-package installation, there is no automatic restart of the system and the installer returns ERROR\_SUCCESS\_REBOOT\_REQUIRED.</span></span> |
| <span data-ttu-id="ed960-118">Elimina</span><span class="sxs-lookup"><span data-stu-id="ed960-118">Suppress</span></span>       | <span data-ttu-id="ed960-119">Non visualizzare più la richiesta di riavvio al termine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="ed960-119">Suppress prompts for a restart at the end of the installation.</span></span> <span data-ttu-id="ed960-120">Il programma di installazione richiede all'utente l'opzione per il riavvio durante l'installazione ogni volta che viene rilevata l' [azione ForceReboot](forcereboot-action.md).</span><span class="sxs-lookup"><span data-stu-id="ed960-120">The installer still prompts the user with an option to restart during the installation whenever it encounters the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="ed960-121">Se non è presente alcuna interfaccia utente, il sistema viene riavviato automaticamente a ogni ForceReboot.</span><span class="sxs-lookup"><span data-stu-id="ed960-121">If there is no user interface, the system automatically restarts at each ForceReboot.</span></span> <span data-ttu-id="ed960-122">Il riavvio al termine dell'installazione, ad esempio causato da un tentativo di installazione di un file in uso, viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="ed960-122">Restarts at the end of the installation (for example, caused by an attempt to install a file in use) are suppressed.</span></span>                                    |
| <span data-ttu-id="ed960-123">ReallySuppress</span><span class="sxs-lookup"><span data-stu-id="ed960-123">ReallySuppress</span></span> | <span data-ttu-id="ed960-124">Elimina tutti i riavvii e riavvia i prompt avviati da ForceReboot durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ed960-124">Suppress all restarts and restart prompts initiated by ForceReboot during the installation.</span></span> <span data-ttu-id="ed960-125">Non visualizzare tutti i riavvii e riavviare i prompt alla fine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="ed960-125">Suppress all restarts and restart prompts at the end of the installation.</span></span> <span data-ttu-id="ed960-126">Sia la richiesta di riavvio che il riavvio vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="ed960-126">Both the restart prompt and the restart itself are suppressed.</span></span> <span data-ttu-id="ed960-127">Ad esempio, il riavvio alla fine dell'installazione, causato da un tentativo di installazione di un file in uso, viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="ed960-127">For example, restarts at the end of the installation, caused by an attempt to install a file in use, are suppressed.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="ed960-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed960-128">Remarks</span></span>

<span data-ttu-id="ed960-129">Il programma di installazione valuta solo il primo carattere della proprietà **reboot** .</span><span class="sxs-lookup"><span data-stu-id="ed960-129">The installer only evaluates the first character of the **REBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed960-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed960-130">Requirements</span></span>



| <span data-ttu-id="ed960-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed960-131">Requirement</span></span> | <span data-ttu-id="ed960-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ed960-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed960-133">Versione</span><span class="sxs-lookup"><span data-stu-id="ed960-133">Version</span></span><br/> | <span data-ttu-id="ed960-134">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ed960-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ed960-135">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed960-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ed960-136">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed960-136">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ed960-137">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ed960-137">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed960-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed960-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed960-139">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ed960-139">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="ed960-140">**Proprietà REBOOTPROMPT**</span><span class="sxs-lookup"><span data-stu-id="ed960-140">**REBOOTPROMPT Property**</span></span>](rebootprompt.md)
</dt> <dt>

[<span data-ttu-id="ed960-141">Riavvio del sistema</span><span class="sxs-lookup"><span data-stu-id="ed960-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




