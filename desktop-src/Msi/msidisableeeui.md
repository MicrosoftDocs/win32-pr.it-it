---
description: Per disabilitare l'interfaccia utente incorporata per l'installazione definita nella tabella MsiEmbeddedUI, impostare la proprietà MSIDISABLEEEUI su 1 nella riga di comando.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: Proprietà MSIDISABLEEEUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d89ce43f649d406e4ae086db236375c02c43e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329344"
---
# <a name="msidisableeeui-property"></a><span data-ttu-id="4eb00-103">Proprietà MSIDISABLEEEUI</span><span class="sxs-lookup"><span data-stu-id="4eb00-103">MSIDISABLEEEUI property</span></span>

<span data-ttu-id="4eb00-104">Per disabilitare l'interfaccia utente incorporata per l'installazione definita nella [tabella MsiEmbeddedUI](msiembeddedui-table.md), impostare la proprietà MSIDISABLEEEUI su 1 nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4eb00-104">To disable the embedded user interface for the installation defined in the [MsiEmbeddedUI table](msiembeddedui-table.md), set the MSIDISABLEEEUI property to 1 on the command line.</span></span>

<span data-ttu-id="4eb00-105">**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="4eb00-105">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="4eb00-106">Le versioni precedenti a Windows Installer 4,5 ignorano la proprietà MSIDISABLEEEUI.</span><span class="sxs-lookup"><span data-stu-id="4eb00-106">Versions earlier than Windows Installer 4.5 ignore the MSIDISABLEEEUI Property.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb00-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="4eb00-107">Remarks</span></span>

<span data-ttu-id="4eb00-108">In un'installazione a più pacchetti, un pacchetto figlio deve in genere usare l'interfaccia utente del pacchetto padre e non inizializzare la propria interfaccia utente incorporata.</span><span class="sxs-lookup"><span data-stu-id="4eb00-108">In a multiple-package installation, a child package should typically use the user interface of the parent package and not initialize its own embedded UI.</span></span> <span data-ttu-id="4eb00-109">Se la proprietà MSIDISABLEEEUI non è impostata nel pacchetto padre, per impostazione predefinita il pacchetto figlio utilizza l'interfaccia utente incorporata del pacchetto padre e ignora la proprietà MSIDISABLEEEUI all'interno del pacchetto figlio.</span><span class="sxs-lookup"><span data-stu-id="4eb00-109">If the MSIDISABLEEEUI property is not set inside the parent package, the child package uses the embedded UI of the parent package by default and ignores the MSIDISABLEEEUI property within the child package.</span></span>

<span data-ttu-id="4eb00-110">La proprietà MSIDISABLEEEUI Disabilita l'interfaccia utente incorporata per un singolo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4eb00-110">The MSIDISABLEEEUI property disables the embedded user interface for a single package.</span></span> <span data-ttu-id="4eb00-111">È possibile utilizzare il criterio [MsiDisableEmbeddedUI](msidisableembeddedui.md) per disabilitare le interfacce utente incorporate per tutti i pacchetti nel computer.</span><span class="sxs-lookup"><span data-stu-id="4eb00-111">You can use the [MsiDisableEmbeddedUI](msidisableembeddedui.md) policy to disable embedded user interfaces for all packages on the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb00-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4eb00-112">Requirements</span></span>



| <span data-ttu-id="4eb00-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eb00-113">Requirement</span></span> | <span data-ttu-id="4eb00-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4eb00-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb00-115">Versione</span><span class="sxs-lookup"><span data-stu-id="4eb00-115">Version</span></span><br/> | <span data-ttu-id="4eb00-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4eb00-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4eb00-117">Windows Installer 4,5 in Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4eb00-117">Windows Installer 4.5 on Windows Server 2008, Windows Vista, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="4eb00-118">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4eb00-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4eb00-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4eb00-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb00-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4eb00-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




