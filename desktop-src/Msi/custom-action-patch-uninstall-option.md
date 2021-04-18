---
description: Usare il flag di opzione seguente per specificare che il programma di installazione esegue l'azione personalizzata solo quando viene disinstallata una patch. Per impostare l'opzione, aggiungere il valore di questa tabella al valore nel campo ExtendedType della tabella CustomAction.
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: Opzione di disinstallazione patch azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108365876393733f7cc520ae565bb2c5ea7ff3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319022"
---
# <a name="custom-action-patch-uninstall-option"></a><span data-ttu-id="c63c4-104">Opzione di disinstallazione patch azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="c63c4-104">Custom Action Patch Uninstall Option</span></span>

<span data-ttu-id="c63c4-105">Usare il flag di opzione seguente per specificare che il programma di installazione esegue l'azione personalizzata solo quando viene disinstallata una patch.</span><span class="sxs-lookup"><span data-stu-id="c63c4-105">Use the following option flag to specify that the installer run the custom action only when a patch is being uninstalled.</span></span> <span data-ttu-id="c63c4-106">Per impostare l'opzione, aggiungere il valore di questa tabella al valore nel campo ExtendedType della [tabella CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="c63c4-106">To set the option, add the value in this table to the value in the ExtendedType field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="c63c4-107">**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="c63c4-107">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="c63c4-108">Questa opzione è disponibile a partire da Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="c63c4-108">This option is available beginning with Windows Installer 4.5.</span></span>



| <span data-ttu-id="c63c4-109">Costante</span><span class="sxs-lookup"><span data-stu-id="c63c4-109">Constant</span></span>                                | <span data-ttu-id="c63c4-110">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="c63c4-110">Hexadecimal</span></span> | <span data-ttu-id="c63c4-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="c63c4-111">Decimal</span></span> | <span data-ttu-id="c63c4-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c63c4-112">Description</span></span>                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| <span data-ttu-id="c63c4-113">**msidbCustomActionTypePatchUninstall**</span><span class="sxs-lookup"><span data-stu-id="c63c4-113">**msidbCustomActionTypePatchUninstall**</span></span> | <span data-ttu-id="c63c4-114">0x8000</span><span class="sxs-lookup"><span data-stu-id="c63c4-114">0x8000</span></span>      | <span data-ttu-id="c63c4-115">32768</span><span class="sxs-lookup"><span data-stu-id="c63c4-115">32768</span></span>   | <span data-ttu-id="c63c4-116">L'azione personalizzata viene eseguita solo quando è in corso la disinstallazione di una patch.</span><span class="sxs-lookup"><span data-stu-id="c63c4-116">The custom action runs only when a patch is being uninstalled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c63c4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c63c4-117">Remarks</span></span>

<span data-ttu-id="c63c4-118">Questo attributo può essere aggiunto a un'azione personalizzata mediante la relativa creazione nel pacchetto di Windows Installer (file con estensione msi).</span><span class="sxs-lookup"><span data-stu-id="c63c4-118">This attribute can be added to a custom action by authoring it in the Windows Installer package (.msi file).</span></span> <span data-ttu-id="c63c4-119">Una nuova azione personalizzata con questo attributo può essere aggiunta da una patch.</span><span class="sxs-lookup"><span data-stu-id="c63c4-119">A new custom action with this attribute can be added by a patch.</span></span> <span data-ttu-id="c63c4-120">Un'azione personalizzata con questo attributo può essere aggiornata da una patch.</span><span class="sxs-lookup"><span data-stu-id="c63c4-120">A custom action having this attribute can be updated by a patch.</span></span> <span data-ttu-id="c63c4-121">Questo attributo non può essere aggiunto o rimosso da una patch a un'azione personalizzata esistente.</span><span class="sxs-lookup"><span data-stu-id="c63c4-121">This attribute cannot be added or removed by a patch to an existing custom action.</span></span>

<span data-ttu-id="c63c4-122">Se una patch aggiunge o aggiorna un'azione personalizzata con questo attributo, Windows Installer esegue l'azione personalizzata nuova o aggiornata quando la patch viene disinstallata.</span><span class="sxs-lookup"><span data-stu-id="c63c4-122">If a patch adds or updates a custom action with this attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="c63c4-123">Windows Installer rende gli aggiornamenti all'interno della patch disinstallati disponibili per l'azione personalizzata di disinstallazione della patch.</span><span class="sxs-lookup"><span data-stu-id="c63c4-123">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="c63c4-124">La patch deve includere una [tabella *<PatchGUID>* MsiTransformView](msitransformview.md) per fornire queste informazioni Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c63c4-124">The patch must include a [MsiTransformView *<PatchGUID>*](msitransformview.md) table to provide this information to Windows Installer.</span></span>

<span data-ttu-id="c63c4-125">Quando si installa un pacchetto che contiene un'azione personalizzata con l'attributo **msidbCustomActionTypePatchUninstall** con una versione del programma di installazione precedente alla Windows Installer 4,0, il programma di installazione non chiama l'azione personalizzata quando la patch viene disinstallata.</span><span class="sxs-lookup"><span data-stu-id="c63c4-125">When a package that contains a custom action with the **msidbCustomActionTypePatchUninstall** attribute is installed using an installer version earlier than Windows Installer 4.0, the installer does not call the custom action when the patch is uninstalled.</span></span> <span data-ttu-id="c63c4-126">L'installazione può eseguire l'azione personalizzata durante l'installazione, il ripristino o l'aggiornamento del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c63c4-126">The install can run the custom action during the installation, repair, or update of the package.</span></span>

<span data-ttu-id="c63c4-127">Le azioni personalizzate con l'attributo **msidbCustomActionTypePatchUninstall** devono essere condizionate mediante la proprietà [**MSIPATCHREMOVE**](msipatchremove.md) per impedire l'esecuzione dell'azione personalizzata durante l'installazione, il ripristino o l'aggiornamento tramite un sistema con Windows Installer 4,0 o versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="c63c4-127">Custom actions with the **msidbCustomActionTypePatchUninstall** attribute should be conditioned using the [**MSIPATCHREMOVE**](msipatchremove.md) property to prevent the custom action from running when installing, repairing, or updating using a system with Windows Installer 4.0 or earlier.</span></span> <span data-ttu-id="c63c4-128">Quando si installa Windows Installer 4,5 e versioni successive, tutte le patch del sistema con azioni personalizzate contrassegnate con l'attributo **msidbCustomActionTypePatchUninstall** eseguono l'azione personalizzata durante la disinstallazione della patch.</span><span class="sxs-lookup"><span data-stu-id="c63c4-128">When Windows Installer 4.5 and later is installed, all the patches on the system having custom actions marked with the **msidbCustomActionTypePatchUninstall** attribute run the custom action during patch uninstallation.</span></span> <span data-ttu-id="c63c4-129">Se Windows Installer 4,5 o versione successiva viene rimossa dal sistema, le patch perdono la funzionalità di disinstallazione della patch dell'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="c63c4-129">If Windows Installer 4.5 or later is removed from the system, patches lose the custom action patch uninstall functionality.</span></span>

<span data-ttu-id="c63c4-130">Per informazioni sull'esecuzione di un'azione personalizzata durante la disinstallazione di una patch con una versione precedente alla Windows Installer 4,5, vedere [patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c63c4-130">For information about running a custom action during the uninstallation of a patch using a version earlier than Windows Installer 4.5, see [Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c63c4-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c63c4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c63c4-132">Opzioni di esecuzione In-Script azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="c63c4-132">Custom Action In-Script Execution Options</span></span>](custom-action-in-script-execution-options.md)
</dt> <dt>

[<span data-ttu-id="c63c4-133">Riferimento all'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="c63c4-133">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="c63c4-134">Informazioni sulle azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="c63c4-134">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="c63c4-135">Uso di azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="c63c4-135">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="c63c4-136">MsiTransformView *<PatchGUID>*</span><span class="sxs-lookup"><span data-stu-id="c63c4-136">MsiTransformView *<PatchGUID>*</span></span>](msitransformview.md)
</dt> </dl>

 

 



