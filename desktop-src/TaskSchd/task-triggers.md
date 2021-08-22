---
title: Trigger di attività
description: Un trigger è un set di criteri che, se soddisfatti, avvia l'esecuzione di un'attività.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- creazione di trigger Utilità di pianificazione
- trigger Utilità di pianificazione
- trigger Utilità di pianificazione , descritto
- trigger Utilità di pianificazione , basati sul tempo
- trigger Utilità di pianificazione , basati su eventi
- trigger basati su eventi Utilità di pianificazione
- Trigger basati sul tempo Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0060511556615c638eb8385a757e9c44147720b659bb11bfe4f0849e4499ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002299"
---
# <a name="task-triggers"></a>Trigger di attività

Un trigger è un set di criteri che, se soddisfatti, avvia l'esecuzione di un'attività. Utilità di pianificazione fornisce trigger basati sul tempo e basati su eventi che possono avviare un'attività in diversi modi. Una determinata attività può essere avviata da uno o più trigger. Un'attività può avere un massimo di 48 trigger.

## <a name="time-based-triggers"></a>Trigger basati sul tempo

I trigger basati sul tempo avviano le attività in orari specificati. Ciò include l'avvio dell'attività una sola volta a un'ora specifica o l'avvio dell'attività più volte in una pianificazione giornaliera, settimanale, mensile o mensile del giorno della settimana.

## <a name="event-based-triggers"></a>Trigger basati su eventi

I trigger basati su eventi avviano un'attività in risposta a determinati eventi di sistema. Ad esempio, i trigger basati su eventi possono essere impostati per avviare un'attività all'avvio del sistema, quando un utente accede al computer locale o quando il sistema diventa inattivo.

## <a name="multiple-triggers"></a>Più trigger

Ogni attività può essere avviata da uno o più trigger, consentendo l'avvio dell'attività in diversi modi. Tuttavia, più trigger vengono implementati in modo diverso in Utilità di pianificazione 1.0 e Utilità di pianificazione 2.0.

In Utilità di pianificazione 2.0, ogni trigger è definito da un'API trigger separata associata all'attività tramite la raccolta di trigger.

In Utilità di pianificazione 1.0, più trigger possono essere definiti come una pianificazione, un set di orari in cui l'attività viene avviata. In questo caso, la pianificazione è il set di orari (specificato dall'unione di tutti i trigger associati all'elemento di lavoro) in cui verrà eseguito un elemento di lavoro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ripetizione di un'attività](repeating-a-task.md)
</dt> <dt>

[Tipi di trigger](trigger-types.md)
</dt> <dt>

[Interfacce di trigger](trigger-interfaces.md)
</dt> <dt>

[Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md)
</dt> </dl>

 

 




