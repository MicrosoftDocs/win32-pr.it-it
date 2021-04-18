---
description: È possibile utilizzare l'opzione di disinstallazione patch azione personalizzata per specificare che il programma di installazione esegue l'azione personalizzata solo quando viene disinstallata una patch.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Patch disinstallare azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90cfffbdb37f1f2fab046b794010a790e9a5212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306575"
---
# <a name="patch-uninstall-custom-actions"></a><span data-ttu-id="df594-103">Patch disinstallare azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="df594-103">Patch Uninstall Custom Actions</span></span>

<span data-ttu-id="df594-104">È possibile utilizzare l' [opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md) per specificare che il programma di installazione esegue l'azione personalizzata solo quando viene disinstallata una patch.</span><span class="sxs-lookup"><span data-stu-id="df594-104">You can use the [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) to specify that the installer run the custom action only when a patch is uninstalled.</span></span>

<span data-ttu-id="df594-105">**Windows Installer 4,5 e versioni successive:** È possibile utilizzare l' [opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md) per specificare che il programma di installazione esegue l'azione personalizzata solo quando viene disinstallata una patch.</span><span class="sxs-lookup"><span data-stu-id="df594-105">**Windows Installer 4.5 and later:** You can use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) to specify that the installer only run the custom action when a patch is uninstalled.</span></span>

<span data-ttu-id="df594-106">\*\*[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md): \* \*</span><span class="sxs-lookup"><span data-stu-id="df594-106">\*\*[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):  \*\*</span></span>

<span data-ttu-id="df594-107">L' [opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md) non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="df594-107">The [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) is not available.</span></span> <span data-ttu-id="df594-108">Non esiste alcun metodo per contrassegnare un' [azione personalizzata](custom-actions.md) all'interno di un pacchetto di patch da eseguire quando la patch viene disinstallata perché il programma di installazione non applica i pacchetti di patch da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="df594-108">There is no method for marking a [custom action](custom-actions.md) within a patch package to be run when the patch is uninstalled because the installer does not apply the patch packages being uninstalled.</span></span>

<span data-ttu-id="df594-109">Per eseguire un' [azione personalizzata](custom-actions.md) quando viene disinstallata una patch particolare, è necessario che l'azione personalizzata sia presente nell'applicazione originale o che si trovi in una patch per il prodotto che viene sempre applicato.</span><span class="sxs-lookup"><span data-stu-id="df594-109">To have a [custom action](custom-actions.md) run when a particular patch is uninstalled, the custom action must either be present in the original application or be in a patch for the product that is always applied.</span></span>

<span data-ttu-id="df594-110">Gli sviluppatori possono utilizzare la proprietà [**MsiPatchRemovalList**](msipatchremovallist.md) per creare un pacchetto di Windows Installer o una patch che esegue [azioni personalizzate](custom-actions.md) sulla rimozione di una patch.</span><span class="sxs-lookup"><span data-stu-id="df594-110">Developers can use the [**MsiPatchRemovalList**](msipatchremovallist.md) property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="df594-111">L'azione personalizzata può essere creata nel pacchetto di installazione originale, una patch che è già stata applicata al pacchetto o una patch che non è una [patch non installabile](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="df594-111">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="df594-112">L'azione personalizzata può essere condizionata nella proprietà **MsiPatchRemovalList** delle tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="df594-112">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="df594-113">Per ulteriori informazioni sulle azioni conditionalizing, vedere [utilizzo delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md) .</span><span class="sxs-lookup"><span data-stu-id="df594-113">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="df594-114">L'azione personalizzata può ottenere i GUID delle patch da rimuovere dal valore della proprietà [**MsiPatchRemovalList**](msipatchremovallist.md) .</span><span class="sxs-lookup"><span data-stu-id="df594-114">The custom action can obtain the GUIDs of patches being removed from the value of the [**MsiPatchRemovalList**](msipatchremovallist.md) property.</span></span> <span data-ttu-id="df594-115">L'azione personalizzata può determinare se lo stato di installazione della patch è applicato, obsoleto o sostituito chiamando il [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o la proprietà [**PatchProperty**](patch-patchproperty.md) dell' [oggetto patch](patch-object.md).</span><span class="sxs-lookup"><span data-stu-id="df594-115">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

<span data-ttu-id="df594-116">Se l'azione personalizzata richiede metadati speciali dalla patch, la patch deve contenere un'azione personalizzata che scrive i metadati in un percorso del registro di sistema o di file quando viene applicata la patch.</span><span class="sxs-lookup"><span data-stu-id="df594-116">If the custom action requires special metadata from the patch, the patch should contain a custom action that writes the metadata to a registry or file location when the patch is applied.</span></span> <span data-ttu-id="df594-117">L'azione personalizzata nell'applicazione originale o una patch che viene sempre applicata può ottenere le informazioni necessarie per rimuovere le modifiche apportate alla patch.</span><span class="sxs-lookup"><span data-stu-id="df594-117">The custom action in the original application or a patch that is always applied can obtain the information needed to remove the patch's changes.</span></span>

<span data-ttu-id="df594-118">Le patch che apportano modifiche difficili da annullare correttamente non devono essere contrassegnate come [patch non installabili](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="df594-118">Patches making changes that are difficult to undo correctly should not be marked as [uninstallable patches](uninstallable-patches.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df594-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="df594-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df594-120">Sequenza di patch</span><span class="sxs-lookup"><span data-stu-id="df594-120">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="df594-121">Rimozione di patch</span><span class="sxs-lookup"><span data-stu-id="df594-121">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="df594-122">Patch disinstallabili</span><span class="sxs-lookup"><span data-stu-id="df594-122">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="df594-123">Disinstallazione di patch</span><span class="sxs-lookup"><span data-stu-id="df594-123">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="df594-124">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="df594-124">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="df594-125">**MsiEnumapplicationsEx**</span><span class="sxs-lookup"><span data-stu-id="df594-125">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="df594-126">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="df594-126">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="df594-127">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="df594-127">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



