---
description: Il programma di installazione imposta la proprietà OutOfNoRbDiskSpace su true se un volume di destinazione dell'installazione non dispone di spazio su disco sufficiente per gestire l'installazione.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Proprietà OutOfNoRbDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330473"
---
# <a name="outofnorbdiskspace-property"></a><span data-ttu-id="4b5b6-103">Proprietà OutOfNoRbDiskSpace</span><span class="sxs-lookup"><span data-stu-id="4b5b6-103">OutOfNoRbDiskSpace property</span></span>

<span data-ttu-id="4b5b6-104">Il programma di installazione imposta la proprietà **OutOfNoRbDiskSpace** su true se un volume di destinazione dell'installazione non dispone di spazio su disco sufficiente per gestire l'installazione.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-104">The installer sets the **OutOfNoRbDiskSpace** property to True if any volume that is a target of the installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="4b5b6-105">In questo caso, la proprietà **OutOfNoRbDiskSpace** è impostata su true anche se il rollback è stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-105">In this case, the **OutOfNoRbDiskSpace** property is set to True even if rollback has been disabled.</span></span> <span data-ttu-id="4b5b6-106">Se lo spazio disponibile è sufficiente per tutti i volumi, il valore è false.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-106">If all volumes have sufficient space, the value is False.</span></span>

<span data-ttu-id="4b5b6-107">Uno sviluppatore di un pacchetto di installazione può gestire la situazione in cui la proprietà [**OutOfDiskSpace**](outofdiskspace.md) è true e la proprietà **OutOfNoRbDiskSpace** è false creando un'interfaccia utente che presenta all'utente l'opzione per disabilitare il rollback e continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-107">A developer of an installation package can handle the situation when the [**OutOfDiskSpace**](outofdiskspace.md) property is True and the **OutOfNoRbDiskSpace** property is False by authoring a user interface that presents the user with an option to disable rollback and continue the installation.</span></span> <span data-ttu-id="4b5b6-108">Per informazioni sulla visualizzazione condizionale di una finestra di dialogo, vedere [Panoramica di ControlEvent](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4b5b6-108">For information about conditionally displaying a dialog box, see [ControlEvent Overview](controlevent-overview.md).</span></span> <span data-ttu-id="4b5b6-109">Per informazioni sulla disabilitazione del rollback, vedere [EnableRollback ControlEvent](enablerollback-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="4b5b6-109">For information about disabling rollback, see [EnableRollback ControlEvent](enablerollback-controlevent.md).</span></span>

<span data-ttu-id="4b5b6-110">La proprietà **OutOfNoRbDiskSpace** è valida in qualsiasi momento dopo l'esecuzione dell' [azione CostFinalize secondo](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="4b5b6-110">The **OutOfNoRbDiskSpace** property is valid at any time after the [CostFinalize action](costfinalize-action.md) has been executed.</span></span> <span data-ttu-id="4b5b6-111">Lo stato della proprietà **OutOfNoRbDiskSpace** viene aggiornato dinamicamente ogni volta che il costo di installazione totale viene ricalcolato (ad esempio, ogni volta che lo stato di installazione di qualsiasi funzionalità viene modificato tramite la [finestra di dialogo di selezione](selection-dialog.md)).</span><span class="sxs-lookup"><span data-stu-id="4b5b6-111">The **OutOfNoRbDiskSpace** property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection dialog](selection-dialog.md)).</span></span> <span data-ttu-id="4b5b6-112">Azioni di risoluzione selezione utilizzare questo valore per annullare un'installazione e generare una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-112">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b5b6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b5b6-113">Requirements</span></span>



| <span data-ttu-id="4b5b6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b5b6-114">Requirement</span></span> | <span data-ttu-id="4b5b6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4b5b6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b5b6-116">Versione</span><span class="sxs-lookup"><span data-stu-id="4b5b6-116">Version</span></span><br/> | <span data-ttu-id="4b5b6-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4b5b6-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4b5b6-119">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4b5b6-120">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4b5b6-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4b5b6-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b5b6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b5b6-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b5b6-122">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="4b5b6-123">Panoramica di ControlEvent</span><span class="sxs-lookup"><span data-stu-id="4b5b6-123">ControlEvent Overview</span></span>](controlevent-overview.md)
</dt> <dt>

[<span data-ttu-id="4b5b6-124">**Proprietà OutOfDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="4b5b6-124">**OutOfDiskSpace property**</span></span>](outofdiskspace.md)
</dt> <dt>

[<span data-ttu-id="4b5b6-125">ControlEvent EnableRollback</span><span class="sxs-lookup"><span data-stu-id="4b5b6-125">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)
</dt> <dt>

[<span data-ttu-id="4b5b6-126">Azione CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="4b5b6-126">CostFinalize action</span></span>](costfinalize-action.md)
</dt> <dt>

[<span data-ttu-id="4b5b6-127">Finestra di dialogo di selezione</span><span class="sxs-lookup"><span data-stu-id="4b5b6-127">Selection dialog</span></span>](selection-dialog.md)
</dt> </dl>

 

 




