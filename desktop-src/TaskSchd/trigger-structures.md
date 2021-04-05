---
title: Strutture trigger per Utilità di pianificazione 1,0
description: Utilità di pianificazione 1,0 USA diverse strutture per definire i criteri di un trigger.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a03f28f85782d87ee3349582929babe6f907e8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044846"
---
# <a name="trigger-structures-for-task-scheduler-10"></a><span data-ttu-id="3c0d8-103">Strutture trigger per Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="3c0d8-103">Trigger Structures for Task Scheduler 1.0</span></span>

<span data-ttu-id="3c0d8-104">Utilità di pianificazione 1,0 USA diverse strutture per definire i criteri di un trigger.</span><span class="sxs-lookup"><span data-stu-id="3c0d8-104">Task Scheduler 1.0 uses several structures to define the criteria of a trigger.</span></span>

> [!Note]  
> <span data-ttu-id="3c0d8-105">Per ulteriori informazioni sui trigger di Utilità di pianificazione 2,0, vedere [interfacce di trigger](trigger-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="3c0d8-105">For more information about Task Scheduler 2.0 triggers, see [Trigger Interfaces](trigger-interfaces.md).</span></span>

 

## <a name="task-scheduler-10-structures"></a><span data-ttu-id="3c0d8-106">Strutture di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="3c0d8-106">Task Scheduler 1.0 Structures</span></span>

<span data-ttu-id="3c0d8-107">Nella figura seguente viene illustrata la struttura del [**\_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="3c0d8-107">The following illustration shows the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="3c0d8-108">Dispone di tre membri obbligatori (**wBeginYear**, **wBeginMonth** e **wBeginDay**) che devono essere impostati quando si crea un nuovo trigger.</span><span class="sxs-lookup"><span data-stu-id="3c0d8-108">It has three required members (**wBeginYear**, **wBeginMonth**, and **wBeginDay**) that must be set when creating a new trigger.</span></span> <span data-ttu-id="3c0d8-109">Per passare alla pagina di riferimento per la struttura, fare clic sul nome della struttura nell'illustrazione.</span><span class="sxs-lookup"><span data-stu-id="3c0d8-109">(To jump to the reference page for this structure, click the structure name in the illustration.)</span></span>

![struttura del trigger di attività](images/tsktri1.png)

<span data-ttu-id="3c0d8-111">Tenere presente che il membro **TriggerType** utilizza l'enumerazione del [**\_ \_ tipo di trigger di attività**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) e che il membro del **tipo** utilizza una struttura di **\_ \_ Unione del trigger di attività** .</span><span class="sxs-lookup"><span data-stu-id="3c0d8-111">Be aware that the **TriggerType** member uses the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the **Type** member uses a **TASK\_TRIGGER\_UNION** structure.</span></span> <span data-ttu-id="3c0d8-112">L'enumerazione del **\_ \_ tipo di trigger di attività** viene utilizzata per specificare il tipo di trigger (tipi di trigger basati su eventi e ora).</span><span class="sxs-lookup"><span data-stu-id="3c0d8-112">The **TASK\_TRIGGER\_TYPE** enumeration is used to specify the type of trigger (event and time-based trigger types).</span></span> <span data-ttu-id="3c0d8-113">La struttura di [**\_ \_ Unione del tipo di trigger**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) viene utilizzata per combinare le strutture [**giornaliere**](/windows/desktop/api/Mstask/ns-mstask-daily), [**settimanali**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (giorno del mese) e [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (giorno della settimana) utilizzate per specificare quando verrà attivato un trigger basato sul tempo.</span><span class="sxs-lookup"><span data-stu-id="3c0d8-113">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used to combine the [**DAILY**](/windows/desktop/api/Mstask/ns-mstask-daily), [**WEEKLY**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (day of month), and [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (day of week) structures that are used to specify when a time-based trigger will fire.</span></span>

<span data-ttu-id="3c0d8-114">Se **TriggerType** specifica un trigger basato su una sola volta o un trigger basato su eventi, il membro del **tipo** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3c0d8-114">If **TriggerType** specifies a one-time time-based trigger or an event-based trigger, the **Type** member is ignored.</span></span> <span data-ttu-id="3c0d8-115">La struttura di [**\_ \_ Unione del tipo di trigger**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) viene utilizzata solo se il membro **TriggerType** specifica un trigger giornaliero, settimanale, giornaliero del mese o basato sul tempo della settimana.</span><span class="sxs-lookup"><span data-stu-id="3c0d8-115">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used only if the **TriggerType** member specifies a daily, weekly, day-of-month, or monthly day-of-week time-based trigger.</span></span>

<span data-ttu-id="3c0d8-116">Inoltre, l'impostazione del membro del **tipo** indica quale membro della struttura di [**\_ \_ Unione del tipo di trigger**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="3c0d8-116">In addition, the setting of the **Type** member indicates which member of the [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used.</span></span> <span data-ttu-id="3c0d8-117">Nella figura seguente viene illustrata la relazione tra i valori dell'enumerazione del [**\_ \_ tipo di trigger di attività**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) e i membri della struttura della **\_ \_ struttura del tipo di trigger** .</span><span class="sxs-lookup"><span data-stu-id="3c0d8-117">The following illustration shows the relationship between the values of the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the members of the **TRIGGER\_TYPE\_STRUCTURE** structure.</span></span> <span data-ttu-id="3c0d8-118">Per passare alle pagine di riferimento per queste strutture, fare clic sul nome della struttura nella figura.</span><span class="sxs-lookup"><span data-stu-id="3c0d8-118">(To jump to the reference pages for these structures click the structure name in the illustration.)</span></span>

![relazione tra i valori di enumerazione del tipo di trigger attività e i membri della struttura della struttura del tipo di trigger](images/tsktri3.png)

## <a name="related-topics"></a><span data-ttu-id="3c0d8-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c0d8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c0d8-121">Trigger attività</span><span class="sxs-lookup"><span data-stu-id="3c0d8-121">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="3c0d8-122">Tipi di trigger</span><span class="sxs-lookup"><span data-stu-id="3c0d8-122">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="3c0d8-123">Interfacce trigger</span><span class="sxs-lookup"><span data-stu-id="3c0d8-123">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> </dl>

 

 




