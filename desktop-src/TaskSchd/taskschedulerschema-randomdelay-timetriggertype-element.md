---
title: Elemento RandomDelay (timeTriggerType)
description: Contiene il tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. | Elemento RandomDelay (timeTriggerType)
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- Utilità di pianificazione elemento RandomDelay
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a28613cb236b6dc8a3ae77dce9452423a992a866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321751"
---
# <a name="randomdelay-timetriggertype-element"></a><span data-ttu-id="05374-105">Elemento RandomDelay (timeTriggerType)</span><span class="sxs-lookup"><span data-stu-id="05374-105">RandomDelay (timeTriggerType) Element</span></span>

<span data-ttu-id="05374-106">Contiene il tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="05374-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="05374-107">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="05374-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="05374-108">Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="05374-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="05374-109">L'elemento è definito dal tipo complesso [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="05374-109">The element is defined by the [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="05374-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="05374-110">Parent element</span></span>



| <span data-ttu-id="05374-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="05374-111">Element</span></span>                                                                                    | <span data-ttu-id="05374-112">Derivato da</span><span class="sxs-lookup"><span data-stu-id="05374-112">Derived from</span></span>                                                               | <span data-ttu-id="05374-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05374-113">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="05374-114">**TimeTrigger (triggerGroup)**</span><span class="sxs-lookup"><span data-stu-id="05374-114">**TimeTrigger (triggerGroup)**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md) | [<span data-ttu-id="05374-115">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="05374-115">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md) | <span data-ttu-id="05374-116">Specifica un trigger che avvia un'attività quando viene attivato il trigger.</span><span class="sxs-lookup"><span data-stu-id="05374-116">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="05374-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="05374-117">Remarks</span></span>

<span data-ttu-id="05374-118">Per lo sviluppo in C++, vedere [**la proprietà RandomDelay di ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).</span><span class="sxs-lookup"><span data-stu-id="05374-118">For C++ development, see [**RandomDelay Property of ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).</span></span>

<span data-ttu-id="05374-119">Per lo sviluppo di script, vedere [**TimeTrigger. RandomDelay**](timetrigger-randomdelay.md).</span><span class="sxs-lookup"><span data-stu-id="05374-119">For script development, see [**TimeTrigger.RandomDelay**](timetrigger-randomdelay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05374-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05374-120">Requirements</span></span>



| <span data-ttu-id="05374-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="05374-121">Requirement</span></span> | <span data-ttu-id="05374-122">Valore</span><span class="sxs-lookup"><span data-stu-id="05374-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05374-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05374-123">Minimum supported client</span></span><br/> | <span data-ttu-id="05374-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05374-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05374-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05374-125">Minimum supported server</span></span><br/> | <span data-ttu-id="05374-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05374-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





