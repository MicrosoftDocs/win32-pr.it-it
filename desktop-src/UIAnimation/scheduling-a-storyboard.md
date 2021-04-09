---
title: Pianificare uno storyboard
description: Dopo la creazione di uno storyboard, questo viene pianificato dal gestore dell'animazione.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- Animazione di Windows storyboard, pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3feae253804d20711c9bbd8ed50895f43272a3f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044155"
---
# <a name="schedule-a-storyboard"></a>Pianificare uno storyboard

Dopo la creazione di uno storyboard, questo viene pianificato dal gestore dell'animazione.

## <a name="overview"></a>Panoramica

Per impostazione predefinita, ogni Storyboard viene avviato immediatamente quando viene pianificato. Ciò significa che quando uno storyboard inizia ad animare una o più variabili, può interrompere qualsiasi altro Storyboard che anima le stesse variabili. Tuttavia, un'applicazione può specificare altri comportamenti determinando la priorità relativa tra gli storyboard.

Una volta pianificato uno storyboard, non è più possibile modificarlo. Tuttavia, dopo che uno storyboard è stato rimosso dalla pianificazione, è possibile pianificarne nuovamente la riproduzione. Gli sviluppatori devono prestare attenzione quando riutilizza gli storyboard, in quanto questa operazione dovrebbe essere eseguita solo se non è possibile che lo stesso storyboard debba essere accodato a causa di un'azione dell'utente quando è già in esecuzione o in coda nella pianificazione.

## <a name="example-code"></a>Codice di esempio

Il codice di esempio seguente viene tratto da MainWindow. cpp nell'animazione Windows esempi di animazione basata su [applicazioni](application-driven-animation-sample.md) e [animazione basata su timer](timer-driven-animation-sample.md). Usa il metodo [**IUIAnimationStoryboard:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) per pianificare lo storyboard. Questo metodo richiede l'ora corrente come parametro.


```
// Get the current time and schedule the storyboard for play

UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    hr = pStoryboard->Schedule(
        secondsNow
    );
}
```



## <a name="previous-step"></a>Passaggio precedente

Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [creare uno storyboard e aggiungere transizioni](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAnimationStoryboard:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[**IUIAnimationTimer:: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[Panoramica dello storyboard](storyboard-construction.md)
</dt> </dl>

 

 




