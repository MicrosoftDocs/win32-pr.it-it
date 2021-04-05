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
# <a name="trigger-structures-for-task-scheduler-10"></a>Strutture trigger per Utilità di pianificazione 1,0

Utilità di pianificazione 1,0 USA diverse strutture per definire i criteri di un trigger.

> [!Note]  
> Per ulteriori informazioni sui trigger di Utilità di pianificazione 2,0, vedere [interfacce di trigger](trigger-interfaces.md).

 

## <a name="task-scheduler-10-structures"></a>Strutture di Utilità di pianificazione 1,0

Nella figura seguente viene illustrata la struttura del [**\_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . Dispone di tre membri obbligatori (**wBeginYear**, **wBeginMonth** e **wBeginDay**) che devono essere impostati quando si crea un nuovo trigger. Per passare alla pagina di riferimento per la struttura, fare clic sul nome della struttura nell'illustrazione.

![struttura del trigger di attività](images/tsktri1.png)

Tenere presente che il membro **TriggerType** utilizza l'enumerazione del [**\_ \_ tipo di trigger di attività**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) e che il membro del **tipo** utilizza una struttura di **\_ \_ Unione del trigger di attività** . L'enumerazione del **\_ \_ tipo di trigger di attività** viene utilizzata per specificare il tipo di trigger (tipi di trigger basati su eventi e ora). La struttura di [**\_ \_ Unione del tipo di trigger**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) viene utilizzata per combinare le strutture [**giornaliere**](/windows/desktop/api/Mstask/ns-mstask-daily), [**settimanali**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (giorno del mese) e [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (giorno della settimana) utilizzate per specificare quando verrà attivato un trigger basato sul tempo.

Se **TriggerType** specifica un trigger basato su una sola volta o un trigger basato su eventi, il membro del **tipo** viene ignorato. La struttura di [**\_ \_ Unione del tipo di trigger**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) viene utilizzata solo se il membro **TriggerType** specifica un trigger giornaliero, settimanale, giornaliero del mese o basato sul tempo della settimana.

Inoltre, l'impostazione del membro del **tipo** indica quale membro della struttura di [**\_ \_ Unione del tipo di trigger**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) viene utilizzato. Nella figura seguente viene illustrata la relazione tra i valori dell'enumerazione del [**\_ \_ tipo di trigger di attività**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) e i membri della struttura della **\_ \_ struttura del tipo di trigger** . Per passare alle pagine di riferimento per queste strutture, fare clic sul nome della struttura nella figura.

![relazione tra i valori di enumerazione del tipo di trigger attività e i membri della struttura della struttura del tipo di trigger](images/tsktri3.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trigger attività](task-triggers.md)
</dt> <dt>

[Tipi di trigger](trigger-types.md)
</dt> <dt>

[Interfacce trigger](trigger-interfaces.md)
</dt> </dl>

 

 




