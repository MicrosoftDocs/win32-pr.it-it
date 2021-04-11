---
title: Trigger attività
description: Un trigger è un set di criteri che, se soddisfatti, avvia l'esecuzione di un'attività.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- creazione di trigger Utilità di pianificazione
- trigger Utilità di pianificazione
- trigger Utilità di pianificazione, descritti
- trigger Utilità di pianificazione, basato sul tempo
- trigger Utilità di pianificazione, basati su eventi
- trigger basati su eventi Utilità di pianificazione
- trigger basati sul tempo Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465dfa015be19ff220a77d3c85f0cbb223c4899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221074"
---
# <a name="task-triggers"></a>Trigger attività

Un trigger è un set di criteri che, se soddisfatti, avvia l'esecuzione di un'attività. Utilità di pianificazione fornisce trigger basati sul tempo e basati su eventi che possono avviare un'attività in diversi modi. Una determinata attività può essere avviata da uno o più trigger. Un'attività può avere un massimo di 48 trigger.

## <a name="time-based-triggers"></a>Trigger basati sul tempo

I trigger basati sul tempo avviano le attività a intervalli specificati. Questo include l'avvio dell'attività una volta a un'ora specifica o l'avvio più volte dell'attività in base a una pianificazione giornaliera, settimanale, mensile o mensile del giorno della settimana.

## <a name="event-based-triggers"></a>Trigger basati su eventi

I trigger basati su eventi avviano un'attività in risposta a determinati eventi di sistema. È ad esempio possibile impostare trigger basati su eventi per avviare un'attività all'avvio del sistema, quando un utente accede al computer locale o quando il sistema diventa inattivo.

## <a name="multiple-triggers"></a>Più trigger

Ogni attività può essere avviata da uno o più trigger, consentendo l'avvio dell'attività in diversi modi. Tuttavia, più trigger sono implementati in modo diverso in Utilità di pianificazione 1,0 e Utilità di pianificazione 2,0.

In Utilità di pianificazione 2,0 ogni trigger è definito da un'API trigger separata associata all'attività tramite la raccolta di trigger.

In Utilità di pianificazione 1,0, più trigger possono essere considerati come una pianificazione, un set di volte in cui l'attività viene avviata. In questo caso, la pianificazione è il set di volte (specificato dall'Unione di tutti i trigger associati all'elemento di lavoro) in cui verrà eseguito un elemento di lavoro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ripetizione di un'attività](repeating-a-task.md)
</dt> <dt>

[Tipi di trigger](trigger-types.md)
</dt> <dt>

[Interfacce trigger](trigger-interfaces.md)
</dt> <dt>

[Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md)
</dt> </dl>

 

 




