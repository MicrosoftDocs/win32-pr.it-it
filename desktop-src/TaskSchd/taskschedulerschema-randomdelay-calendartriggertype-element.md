---
title: Elemento RandomDelay (calendarTriggerType)
description: Contiene il tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. | Elemento RandomDelay (calendarTriggerType)
ms.assetid: 497fab4e-ad63-43e6-a086-2d77b43662d9
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
ms.openlocfilehash: d71149bfeceeb6c17cafa27f56bb15bb184ead06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353381"
---
# <a name="randomdelay-calendartriggertype-element"></a><span data-ttu-id="9f37f-105">Elemento RandomDelay (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="9f37f-105">RandomDelay (calendarTriggerType) Element</span></span>

<span data-ttu-id="9f37f-106">Contiene il tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="9f37f-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="9f37f-107">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="9f37f-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="9f37f-108">Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="9f37f-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="9f37f-109">L'elemento **RandomDelay** è definito dal tipo complesso [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9f37f-109">The **RandomDelay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9f37f-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="9f37f-110">Parent element</span></span>



| <span data-ttu-id="9f37f-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="9f37f-111">Element</span></span>                                                                                            | <span data-ttu-id="9f37f-112">Derivato da</span><span class="sxs-lookup"><span data-stu-id="9f37f-112">Derived from</span></span>                                                                       | <span data-ttu-id="9f37f-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f37f-113">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f37f-114">**CalendarTrigger (triggerGroup)**</span><span class="sxs-lookup"><span data-stu-id="9f37f-114">**CalendarTrigger (triggerGroup)**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="9f37f-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="9f37f-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="9f37f-116">Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="9f37f-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="9f37f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f37f-117">Requirements</span></span>



| <span data-ttu-id="9f37f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f37f-118">Requirement</span></span> | <span data-ttu-id="9f37f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9f37f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9f37f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f37f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9f37f-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f37f-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9f37f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f37f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9f37f-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9f37f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





