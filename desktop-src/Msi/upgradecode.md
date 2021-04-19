---
description: La proprietà UpgradeCode è un GUID che rappresenta un set correlato di prodotti. UpgradeCode viene utilizzato nella tabella di aggiornamento per cercare le versioni correlate del prodotto già installato. Questa proprietà viene utilizzata dall'azione RegisterProduct.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: Proprietà UpgradeCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328147"
---
# <a name="upgradecode-property"></a><span data-ttu-id="078fd-104">Proprietà UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="078fd-104">UpgradeCode property</span></span>

<span data-ttu-id="078fd-105">La proprietà **UpgradeCode** è un GUID che rappresenta un set correlato di prodotti.</span><span class="sxs-lookup"><span data-stu-id="078fd-105">The **UpgradeCode** property is a GUID representing a related set of products.</span></span> <span data-ttu-id="078fd-106">**UpgradeCode** viene utilizzato nella tabella di [aggiornamento](upgrade-table.md) per cercare le versioni correlate del prodotto già installato.</span><span class="sxs-lookup"><span data-stu-id="078fd-106">The **UpgradeCode** is used in the [Upgrade Table](upgrade-table.md) to search for related versions of the product that are already installed.</span></span>

<span data-ttu-id="078fd-107">Questa proprietà viene utilizzata dall' [azione RegisterProduct](registerproduct-action.md).</span><span class="sxs-lookup"><span data-stu-id="078fd-107">This property is used by the [RegisterProduct action](registerproduct-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="078fd-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="078fd-108">Remarks</span></span>

<span data-ttu-id="078fd-109">Si consiglia vivamente agli autori dei pacchetti di installazione di specificare un **UpgradeCode** per la propria applicazione.</span><span class="sxs-lookup"><span data-stu-id="078fd-109">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span>

## <a name="requirements"></a><span data-ttu-id="078fd-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="078fd-110">Requirements</span></span>



| <span data-ttu-id="078fd-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="078fd-111">Requirement</span></span> | <span data-ttu-id="078fd-112">Valore</span><span class="sxs-lookup"><span data-stu-id="078fd-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="078fd-113">Versione</span><span class="sxs-lookup"><span data-stu-id="078fd-113">Version</span></span><br/> | <span data-ttu-id="078fd-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="078fd-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="078fd-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="078fd-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="078fd-116">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="078fd-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="078fd-117">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="078fd-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="078fd-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="078fd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="078fd-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="078fd-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="078fd-120">Applicazione di patch e aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="078fd-120">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="078fd-121">Preparazione di un'applicazione per aggiornamenti principali futuri</span><span class="sxs-lookup"><span data-stu-id="078fd-121">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




