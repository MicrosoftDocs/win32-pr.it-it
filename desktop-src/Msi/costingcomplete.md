---
description: La proprietà CostingComplete indica se il programma di installazione ha completato il costo dello spazio su disco.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Proprietà CostingComplete
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326773"
---
# <a name="costingcomplete-property"></a><span data-ttu-id="e0eef-103">Proprietà CostingComplete</span><span class="sxs-lookup"><span data-stu-id="e0eef-103">CostingComplete property</span></span>

<span data-ttu-id="e0eef-104">La proprietà **CostingComplete** indica se il programma di installazione ha completato il costo dello spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="e0eef-104">The **CostingComplete** property indicates whether the installer has completed disk space costing.</span></span> <span data-ttu-id="e0eef-105">Questa proprietà può essere utilizzata per creare una finestra di dialogo attivata se i costi non sono stati completati.</span><span class="sxs-lookup"><span data-stu-id="e0eef-105">This property can be used to author a dialog box triggered if costing has not been completed.</span></span> <span data-ttu-id="e0eef-106">La proprietà viene impostata in modo dinamico durante il costo dello spazio su disco e viene impostata su 1 non appena il costo è completo.</span><span class="sxs-lookup"><span data-stu-id="e0eef-106">The property is set dynamically during disk space costing and is set to 1 as soon as the costing is complete.</span></span> <span data-ttu-id="e0eef-107">Questa proprietà viene inizializzata su 0 dall' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e0eef-107">This property is initialized to 0 by the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e0eef-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0eef-108">Remarks</span></span>

<span data-ttu-id="e0eef-109">Per un esempio di come creare un'attesa.</span><span class="sxs-lookup"><span data-stu-id="e0eef-109">For an example of how to author a "Please wait .</span></span> <span data-ttu-id="e0eef-110">.</span><span class="sxs-lookup"><span data-stu-id="e0eef-110">.</span></span> <span data-ttu-id="e0eef-111">.</span><span class="sxs-lookup"><span data-stu-id="e0eef-111">.</span></span> <span data-ttu-id="e0eef-112">"la finestra di dialogo visualizzata durante i costi di spazio su disco, vedere la sezione [creazione di un condizionale" attendere... " MessageBox](authoring-a-conditional-please-wait-------message-box.md).</span><span class="sxs-lookup"><span data-stu-id="e0eef-112">" dialog box that pops up during disk space costing, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0eef-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0eef-113">Requirements</span></span>



| <span data-ttu-id="e0eef-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0eef-114">Requirement</span></span> | <span data-ttu-id="e0eef-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e0eef-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0eef-116">Versione</span><span class="sxs-lookup"><span data-stu-id="e0eef-116">Version</span></span><br/> | <span data-ttu-id="e0eef-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e0eef-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e0eef-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e0eef-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e0eef-119">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0eef-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e0eef-120">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e0eef-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0eef-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0eef-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0eef-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e0eef-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




