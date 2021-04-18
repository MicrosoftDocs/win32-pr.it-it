---
description: Il programma di installazione imposta la proprietà OutOfDiskSpace su TRUE se un volume di destinazione dell'installazione corrente non dispone di spazio su disco sufficiente per gestire l'installazione.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: Proprietà OutOfDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327803"
---
# <a name="outofdiskspace-property"></a><span data-ttu-id="0a62b-103">Proprietà OutOfDiskSpace</span><span class="sxs-lookup"><span data-stu-id="0a62b-103">OutOfDiskSpace property</span></span>

<span data-ttu-id="0a62b-104">Il programma di installazione imposta la proprietà **OutOfDiskSpace** su true se un volume di destinazione dell'installazione corrente non dispone di spazio su disco sufficiente per gestire l'installazione.</span><span class="sxs-lookup"><span data-stu-id="0a62b-104">The installer sets the **OutOfDiskSpace** property to TRUE if any volume that is a target of the current installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="0a62b-105">Se lo spazio disponibile è sufficiente per tutti i volumi, il valore è FALSE.</span><span class="sxs-lookup"><span data-stu-id="0a62b-105">If all volumes have sufficient space, the value is FALSE.</span></span> <span data-ttu-id="0a62b-106">Azioni di risoluzione selezione utilizzare questo valore per annullare un'installazione e generare una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="0a62b-106">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

<span data-ttu-id="0a62b-107">Questa proprietà è valida in qualsiasi momento dopo l'esecuzione dell' [azione CostFinalize secondo](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="0a62b-107">This property is valid at any time after the [CostFinalize action](costfinalize-action.md) is executed.</span></span> <span data-ttu-id="0a62b-108">Lo stato della proprietà [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) viene aggiornato dinamicamente ogni volta che il costo di installazione totale viene ricalcolato (ad esempio, ogni volta che lo stato di installazione di qualsiasi funzionalità viene modificato tramite la finestra di dialogo di [selezione](selection-dialog.md) ).</span><span class="sxs-lookup"><span data-stu-id="0a62b-108">The [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection](selection-dialog.md) dialog).</span></span>

## <a name="remarks"></a><span data-ttu-id="0a62b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a62b-109">Remarks</span></span>

<span data-ttu-id="0a62b-110">Qualsiasi finestra di dialogo che si basa sulla proprietà **OutOfDiskSpace** per determinare se visualizzare una finestra di dialogo deve impostare il [bit di stile della finestra](trackdiskspace-dialog-style-bit.md) di dialogo TrackDiskSpace per la finestra di dialogo per aggiornare in modo dinamico lo spazio sui volumi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0a62b-110">Any dialog relying on the **OutOfDiskSpace** property to determine whether to bring up a dialog must set the [TrackDiskSpace Dialog Style Bit](trackdiskspace-dialog-style-bit.md) for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a62b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a62b-111">Requirements</span></span>



| <span data-ttu-id="0a62b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a62b-112">Requirement</span></span> | <span data-ttu-id="0a62b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="0a62b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a62b-114">Versione</span><span class="sxs-lookup"><span data-stu-id="0a62b-114">Version</span></span><br/> | <span data-ttu-id="0a62b-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0a62b-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0a62b-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0a62b-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0a62b-117">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0a62b-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="0a62b-118">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0a62b-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a62b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a62b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a62b-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0a62b-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




