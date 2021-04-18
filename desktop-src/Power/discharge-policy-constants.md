---
description: Nell'elenco seguente vengono descritte le costanti dei criteri di dismissione.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Costanti dei criteri di scaricamento (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 052d07a5fe538543b66ec8d48c940f63fe82a682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312057"
---
# <a name="discharge-policy-constants"></a><span data-ttu-id="01aa2-103">Costanti dei criteri di scaricamento</span><span class="sxs-lookup"><span data-stu-id="01aa2-103">Discharge Policy Constants</span></span>

<span data-ttu-id="01aa2-104">Nell'elenco seguente vengono descritte le costanti dei criteri di dismissione.</span><span class="sxs-lookup"><span data-stu-id="01aa2-104">The following list describes the discharge policy constants.</span></span>



| <span data-ttu-id="01aa2-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="01aa2-105">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="01aa2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01aa2-106">Description</span></span>                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <span data-ttu-id="01aa2-107"><dt>**Scarica \_ CRITERIO \_ critico**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="01aa2-107"><dt>**DISCHARGE\_POLICY\_CRITICAL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="01aa2-108">Quale delle impostazioni dei criteri di scaricamento della batteria (strutture a [**\_ \_ livello di energia del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) viene usato quando la batteria viene scaricata sotto la soglia critica.</span><span class="sxs-lookup"><span data-stu-id="01aa2-108">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the critical threshold.</span></span><br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <span data-ttu-id="01aa2-109"><dt>**Scarica \_ CRITERIO \_ basso**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="01aa2-109"><dt>**DISCHARGE\_POLICY\_LOW**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="01aa2-110">Quale delle impostazioni dei criteri di scaricamento della batteria (strutture a [**\_ \_ livello di energia del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) viene usato quando la batteria viene scaricata al di sotto della soglia inferiore.</span><span class="sxs-lookup"><span data-stu-id="01aa2-110">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the low threshold.</span></span><br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <span data-ttu-id="01aa2-111">Numero di <dt>**\_ \_Criteri di dismissione**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="01aa2-111"><dt>**NUM\_DISCHARGE\_POLICIES**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="01aa2-112">Numero di impostazioni dei criteri di scaricamento della batteria (strutture a [**\_ \_ livello di alimentazione del sistema**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) specificate.</span><span class="sxs-lookup"><span data-stu-id="01aa2-112">Number of battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) specified.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="01aa2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01aa2-113">Requirements</span></span>



| <span data-ttu-id="01aa2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="01aa2-114">Requirement</span></span> | <span data-ttu-id="01aa2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="01aa2-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01aa2-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01aa2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="01aa2-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="01aa2-117">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="01aa2-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01aa2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="01aa2-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01aa2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="01aa2-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01aa2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="01aa2-121"><dt>WinNT. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01aa2-121"><dt>WinNT.h (include Windows.h)</dt></span></span> </dl> |



 

 




