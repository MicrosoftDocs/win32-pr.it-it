---
title: Pianificare uno storyboard
description: Dopo la creazione, uno storyboard viene pianificato dal gestore dell'animazione.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- storyboard Windows animazione, pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013adc114fd09f518c34bc15ca2e7799381b6cee3dfeeedaf3b26fcae6d506e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008171"
---
# <a name="schedule-a-storyboard"></a>Pianificare uno storyboard

Dopo la creazione, uno storyboard viene pianificato dal gestore dell'animazione.

## <a name="overview"></a>Panoramica

Per impostazione predefinita, ogni storyboard viene avviato immediatamente quando viene pianificato. Ciò significa che quando uno storyboard inizia ad animare una o più variabili, può interrompere qualsiasi altro storyboard che anima le stesse variabili. Tuttavia, un'applicazione può specificare altri comportamenti determinando la priorità relativa tra gli storyboard.

Dopo la pianificazione, uno storyboard non può più essere modificato. Tuttavia, dopo che uno storyboard è stato rimosso dalla pianificazione, può essere pianificato per la riproduzione. Gli sviluppatori devono prestare attenzione quando si usano di nuovo gli storyboard, perché questa operazione deve essere eseguita solo quando non è possibile che lo stesso storyboard debba essere accodato a causa di un'azione dell'utente quando è già in riproduzione o in coda nella pianificazione.

## <a name="example-code"></a>Codice di esempio

Il codice di esempio seguente è tratto da MainWindow.cpp negli esempi di Windows Animation [application-driven Animation](application-driven-animation-sample.md) e [Timer-Driven Animation](timer-driven-animation-sample.md). Usa il [**metodo IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) per pianificare lo storyboard. Questo metodo richiede l'ora corrente come parametro.


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

Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [Creare uno storyboard e aggiungere transizioni](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[**IUIAnimationTimer::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[Panoramica dello storyboard](storyboard-construction.md)
</dt> </dl>

 

 




