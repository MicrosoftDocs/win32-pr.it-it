---
description: Il programma di installazione imposta il valore della proprietà MsiPatchRemovalList su un elenco di patch che vengono rimosse durante l'installazione.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: Proprietà MsiPatchRemovalList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2af522d9570297f2ff911b501bc543cf4b5971c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326267"
---
# <a name="msipatchremovallist-property"></a><span data-ttu-id="32937-103">Proprietà MsiPatchRemovalList</span><span class="sxs-lookup"><span data-stu-id="32937-103">MsiPatchRemovalList property</span></span>

<span data-ttu-id="32937-104">Il programma di installazione imposta il valore della proprietà **MsiPatchRemovalList** su un elenco di patch che vengono rimosse durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="32937-104">The installer sets the value of the **MsiPatchRemovalList** property to a list of patches that are being removed during the installation.</span></span> <span data-ttu-id="32937-105">Le patch sono rappresentate nell'elenco in base ai relativi GUID di codice della patch separati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="32937-105">The patches are represented in the list by their patch code GUIDs separated by semicolons.</span></span>

<span data-ttu-id="32937-106">Gli sviluppatori possono utilizzare la proprietà **MsiPatchRemovalList** per creare un pacchetto di Windows Installer o una patch che esegue [azioni personalizzate](custom-actions.md) sulla rimozione di una patch.</span><span class="sxs-lookup"><span data-stu-id="32937-106">Developers can use the **MsiPatchRemovalList** property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="32937-107">L'azione personalizzata può essere creata nel pacchetto di installazione originale, una patch che è già stata applicata al pacchetto o una patch che non è una [patch non installabile](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="32937-107">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="32937-108">L'azione personalizzata può essere condizionata nella proprietà **MsiPatchRemovalList** delle tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="32937-108">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="32937-109">Per ulteriori informazioni sulle azioni conditionalizing, vedere [utilizzo delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md) .</span><span class="sxs-lookup"><span data-stu-id="32937-109">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="32937-110">L'azione personalizzata può ottenere i GUID delle patch da rimuovere dal valore della proprietà **MsiPatchRemovalList** .</span><span class="sxs-lookup"><span data-stu-id="32937-110">The custom action can obtain the GUIDs of patches being removed from the value of the **MsiPatchRemovalList** property.</span></span> <span data-ttu-id="32937-111">L'azione personalizzata può determinare se lo stato di installazione della patch è applicato, obsoleto o sostituito chiamando la funzione [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o la proprietà [**PatchProperty**](patch-patchproperty.md) dell' [oggetto patch](patch-object.md).</span><span class="sxs-lookup"><span data-stu-id="32937-111">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) function or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="32937-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="32937-112">Remarks</span></span>

<span data-ttu-id="32937-113">Per ulteriori informazioni sulla rimozione di patch, vedere [rimozione di patch](removing-patches.md).</span><span class="sxs-lookup"><span data-stu-id="32937-113">For more information about removing patches, see [Removing Patches](removing-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32937-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32937-114">Requirements</span></span>



| <span data-ttu-id="32937-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="32937-115">Requirement</span></span> | <span data-ttu-id="32937-116">Valore</span><span class="sxs-lookup"><span data-stu-id="32937-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32937-117">Versione</span><span class="sxs-lookup"><span data-stu-id="32937-117">Version</span></span><br/> | <span data-ttu-id="32937-118">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="32937-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="32937-119">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="32937-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="32937-120">Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="32937-120">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="32937-121">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="32937-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32937-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32937-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32937-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="32937-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="32937-124">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="32937-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




