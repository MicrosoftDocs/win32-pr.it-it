---
title: Strutture di trigger per Utilità di pianificazione 1.0
description: Utilità di pianificazione 1.0 usa diverse strutture per definire i criteri di un trigger.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a70688597f7684a6b6a0bedba90cb23d34135cd732aaed37cd74970867b3b02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002061"
---
# <a name="trigger-structures-for-task-scheduler-10"></a>Strutture di trigger per Utilità di pianificazione 1.0

Utilità di pianificazione 1.0 usa diverse strutture per definire i criteri di un trigger.

> [!Note]  
> Per altre informazioni sui trigger Utilità di pianificazione 2.0, vedere [Interfacce di trigger.](trigger-interfaces.md)

 

## <a name="task-scheduler-10-structures"></a>Utilità di pianificazione 1.0

Nella figura seguente viene illustrata [**la struttura \_ TASK TRIGGER.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) Ha tre membri obbligatori (**wBeginYear**, **wBeginMonth** e **wBeginDay**) che devono essere impostati durante la creazione di un nuovo trigger. Per passare alla pagina di riferimento per questa struttura, fare clic sul nome della struttura nell'illustrazione.

![struttura del trigger di attività](images/tsktri1.png)

Tenere presente che il **membro TriggerType** usa l'enumerazione [**TASK TRIGGER \_ \_ TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) e il **membro Type** usa una struttura TASK TRIGGER **\_ \_ UNION.** **L'enumerazione TASK \_ TRIGGER \_ TYPE** viene usata per specificare il tipo di trigger (tipi di trigger basati su eventi e tempo). La struttura [**TRIGGER \_ TYPE \_ UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) viene usata per combinare le strutture [**DAILY**](/windows/desktop/api/Mstask/ns-mstask-daily), [**WEEKLY**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (giorno del mese) e [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (giorno della settimana) usate per specificare quando verrà attivato un trigger basato sul tempo.

Se **TriggerType** specifica un trigger basato su una sola volta o un trigger basato su eventi, il **membro Type** viene ignorato. La [**struttura TRIGGER TYPE \_ \_ UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) viene usata solo se il membro **TriggerType** specifica un trigger basato sull'ora giornaliero, settimanale, giorno del mese o giorno della settimana mensile.

Inoltre, l'impostazione del **membro Type** indica quale membro della struttura TRIGGER [**TYPE \_ \_ UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) viene utilizzato. Nella figura seguente viene illustrata la relazione tra i valori [**dell'enumerazione TASK \_ TRIGGER \_ TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) e i membri della **struttura TRIGGER TYPE \_ \_ STRUCTURE.** Per passare alle pagine di riferimento per queste strutture, fare clic sul nome della struttura nell'illustrazione.

![relazione tra i valori di enumerazione del tipo di trigger di attività e i membri della struttura della struttura del tipo di trigger](images/tsktri3.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trigger di attività](task-triggers.md)
</dt> <dt>

[Tipi di trigger](trigger-types.md)
</dt> <dt>

[Interfacce di trigger](trigger-interfaces.md)
</dt> </dl>

 

 




