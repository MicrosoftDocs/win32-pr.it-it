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
# <a name="schedule-a-storyboard"></a><span data-ttu-id="0c9be-104">Pianificare uno storyboard</span><span class="sxs-lookup"><span data-stu-id="0c9be-104">Schedule a Storyboard</span></span>

<span data-ttu-id="0c9be-105">Dopo la creazione di uno storyboard, questo viene pianificato dal gestore dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="0c9be-105">After a storyboard is created, it is scheduled by the animation manager.</span></span>

## <a name="overview"></a><span data-ttu-id="0c9be-106">Panoramica</span><span class="sxs-lookup"><span data-stu-id="0c9be-106">Overview</span></span>

<span data-ttu-id="0c9be-107">Per impostazione predefinita, ogni Storyboard viene avviato immediatamente quando viene pianificato.</span><span class="sxs-lookup"><span data-stu-id="0c9be-107">By default, each storyboard starts immediately when it is scheduled.</span></span> <span data-ttu-id="0c9be-108">Ciò significa che quando uno storyboard inizia ad animare una o più variabili, può interrompere qualsiasi altro Storyboard che anima le stesse variabili.</span><span class="sxs-lookup"><span data-stu-id="0c9be-108">This means that when a storyboard starts to animate one or more variables, it may interrupt any other storyboards animating those same variables.</span></span> <span data-ttu-id="0c9be-109">Tuttavia, un'applicazione può specificare altri comportamenti determinando la priorità relativa tra gli storyboard.</span><span class="sxs-lookup"><span data-stu-id="0c9be-109">However, an application may specify other behaviors by determining the relative priority between storyboards.</span></span>

<span data-ttu-id="0c9be-110">Una volta pianificato uno storyboard, non è più possibile modificarlo.</span><span class="sxs-lookup"><span data-stu-id="0c9be-110">After a storyboard has been scheduled, it can no longer be altered.</span></span> <span data-ttu-id="0c9be-111">Tuttavia, dopo che uno storyboard è stato rimosso dalla pianificazione, è possibile pianificarne nuovamente la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="0c9be-111">However, after a storyboard has been removed from the schedule, it can be scheduled for play again.</span></span> <span data-ttu-id="0c9be-112">Gli sviluppatori devono prestare attenzione quando riutilizza gli storyboard, in quanto questa operazione dovrebbe essere eseguita solo se non è possibile che lo stesso storyboard debba essere accodato a causa di un'azione dell'utente quando è già in esecuzione o in coda nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="0c9be-112">Developers should exercise caution when re-using storyboards, as this should only be done where there is no chance that the same storyboard might need to be queued due to a user action when it is already playing or queued in the schedule.</span></span>

## <a name="example-code"></a><span data-ttu-id="0c9be-113">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="0c9be-113">Example Code</span></span>

<span data-ttu-id="0c9be-114">Il codice di esempio seguente viene tratto da MainWindow. cpp nell'animazione Windows esempi di animazione basata su [applicazioni](application-driven-animation-sample.md) e [animazione basata su timer](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="0c9be-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="0c9be-115">Usa il metodo [**IUIAnimationStoryboard:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) per pianificare lo storyboard.</span><span class="sxs-lookup"><span data-stu-id="0c9be-115">It uses the [**IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) method to schedule the storyboard.</span></span> <span data-ttu-id="0c9be-116">Questo metodo richiede l'ora corrente come parametro.</span><span class="sxs-lookup"><span data-stu-id="0c9be-116">This method requires the current time as a parameter.</span></span>


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



## <a name="previous-step"></a><span data-ttu-id="0c9be-117">Passaggio precedente</span><span class="sxs-lookup"><span data-stu-id="0c9be-117">Previous Step</span></span>

<span data-ttu-id="0c9be-118">Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [creare uno storyboard e aggiungere transizioni](updating---timer-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="0c9be-118">Before starting this step, you should have completed this step: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c9be-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c9be-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c9be-120">**IUIAnimationStoryboard:: Schedule**</span><span class="sxs-lookup"><span data-stu-id="0c9be-120">**IUIAnimationStoryboard::Schedule**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[<span data-ttu-id="0c9be-121">**IUIAnimationTimer:: getTime**</span><span class="sxs-lookup"><span data-stu-id="0c9be-121">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="0c9be-122">Panoramica dello storyboard</span><span class="sxs-lookup"><span data-stu-id="0c9be-122">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




