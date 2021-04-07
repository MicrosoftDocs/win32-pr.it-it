---
description: Questo attributo specifica se i file di backup di rollback sono inclusi nei costi visualizzati dal controllo VolumeCostList.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: Attributo di controllo ControlShowRollbackCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7947777a356933ab74051163b6b9b023736dbb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883941"
---
# <a name="controlshowrollbackcost-control-attribute"></a><span data-ttu-id="180ae-103">Attributo di controllo ControlShowRollbackCost</span><span class="sxs-lookup"><span data-stu-id="180ae-103">ControlShowRollbackCost Control Attribute</span></span>

<span data-ttu-id="180ae-104">Questo attributo specifica se i file di backup di rollback sono inclusi nei costi visualizzati dal [controllo VolumeCostList](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="180ae-104">This attribute specifies whether or not the rollback backup files are included in the costs displayed by the [VolumeCostList control](volumecostlist-control.md).</span></span>

<span data-ttu-id="180ae-105">Se questo bit è impostato e la proprietà [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, i file di backup di rollback sono inclusi nel costo visualizzato dal [controllo VolumeCostList](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="180ae-105">If this bit is set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

<span data-ttu-id="180ae-106">Se questo bit non è impostato e la proprietà [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, i file di backup di rollback non sono inclusi nei costi visualizzati dal [controllo VolumeCostList](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="180ae-106">If this bit is not set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are not included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="180ae-107">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="180ae-107">Valid Controls</span></span>

[<span data-ttu-id="180ae-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="180ae-108">VolumeCostList</span></span>](volumecostlist-control.md)

## <a name="value"></a><span data-ttu-id="180ae-109">Valore</span><span class="sxs-lookup"><span data-stu-id="180ae-109">Value</span></span>



| <span data-ttu-id="180ae-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="180ae-110">Decimal</span></span> | <span data-ttu-id="180ae-111">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="180ae-111">Hexadecimal</span></span> | <span data-ttu-id="180ae-112">Costante</span><span class="sxs-lookup"><span data-stu-id="180ae-112">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="180ae-113">4194304</span><span class="sxs-lookup"><span data-stu-id="180ae-113">4194304</span></span> | <span data-ttu-id="180ae-114">0x00400000</span><span class="sxs-lookup"><span data-stu-id="180ae-114">0x00400000</span></span>  | <span data-ttu-id="180ae-115">**msidbControlShowRollbackCost**</span><span class="sxs-lookup"><span data-stu-id="180ae-115">**msidbControlShowRollbackCost**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="180ae-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="180ae-116">Remarks</span></span>

<span data-ttu-id="180ae-117">Questo attributo di controllo viene ignorato se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D o F.</span><span class="sxs-lookup"><span data-stu-id="180ae-117">This control attribute is ignored if [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D or F.</span></span>

<span data-ttu-id="180ae-118">Se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, viene incluso il costo del rollback, ovvero i file di backup.</span><span class="sxs-lookup"><span data-stu-id="180ae-118">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, the cost of the rollback, backup files is included.</span></span>

<span data-ttu-id="180ae-119">Se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D o la proprietà [**DisableRollback**](-disablerollback.md) = 1, il costo del rollback non include i file di backup.</span><span class="sxs-lookup"><span data-stu-id="180ae-119">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D, or [**DISABLEROLLBACK**](-disablerollback.md) property = 1, the cost of the rollback, backup files is not included.</span></span>

 

 



