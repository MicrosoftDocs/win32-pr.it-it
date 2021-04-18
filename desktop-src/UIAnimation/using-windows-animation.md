---
title: Attività di animazione Windows
description: Negli argomenti contenuti in questa sezione vengono descritte le attività di base necessarie per le applicazioni che utilizzano Windows Animation Manager.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Animazione Windows Animation Windows, attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2007e53a738494e9b143b3aa8a6cf83290acb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298705"
---
# <a name="windows-animation-tasks"></a><span data-ttu-id="d34f8-104">Attività di animazione Windows</span><span class="sxs-lookup"><span data-stu-id="d34f8-104">Windows Animation Tasks</span></span>

<span data-ttu-id="d34f8-105">Negli argomenti contenuti in questa sezione vengono descritte le attività di base necessarie per le applicazioni che utilizzano Windows Animation Manager.</span><span class="sxs-lookup"><span data-stu-id="d34f8-105">The topics contained in this section describe the basic tasks required of applications that use Windows Animation Manager.</span></span>

<span data-ttu-id="d34f8-106">Queste attività, in ordine, includono:</span><span class="sxs-lookup"><span data-stu-id="d34f8-106">These tasks, in order, include:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d34f8-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="d34f8-107">In this section</span></span>



| <span data-ttu-id="d34f8-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="d34f8-108">Topic</span></span>                                                                                                | <span data-ttu-id="d34f8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d34f8-109">Description</span></span>                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d34f8-110">Creare gli oggetti animazione principali</span><span class="sxs-lookup"><span data-stu-id="d34f8-110">Create the Main Animation Objects</span></span>](adding-animation-to-an-application.md)<br/>               | <span data-ttu-id="d34f8-111">Per utilizzare l'animazione Windows nell'applicazione, il primo passaggio consiste nel creare un piccolo set di oggetti animazione principali.</span><span class="sxs-lookup"><span data-stu-id="d34f8-111">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="d34f8-112">Creare variabili di animazione</span><span class="sxs-lookup"><span data-stu-id="d34f8-112">Create Animation Variables</span></span>](create-animation-variables.md)<br/>                              | <span data-ttu-id="d34f8-113">Un'applicazione deve creare una variabile di animazione per ogni caratteristica visiva che deve essere animata usando l'animazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="d34f8-113">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="d34f8-114">Aggiornare gestione animazioni e creare frame</span><span class="sxs-lookup"><span data-stu-id="d34f8-114">Update the Animation Manager and Draw Frames</span></span>](introducing-windows-animation-manager.md)<br/> | <span data-ttu-id="d34f8-115">Ogni volta che un'applicazione pianifica uno storyboard, l'applicazione deve fornire l'ora corrente al gestore dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="d34f8-115">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="d34f8-116">L'ora corrente è necessaria anche quando si indica al gestore delle animazioni di aggiornare lo stato e impostare tutte le variabili di animazione sui valori interpolati appropriati.</span><span class="sxs-lookup"><span data-stu-id="d34f8-116">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span><br/> |
| [<span data-ttu-id="d34f8-117">Leggere i valori delle variabili di animazione</span><span class="sxs-lookup"><span data-stu-id="d34f8-117">Read the Animation Variable Values</span></span>](updating---application-driven-animation.md)<br/>         | <span data-ttu-id="d34f8-118">Ogni volta che l'applicazione disegna, deve leggere i valori correnti delle variabili di animazione che rappresentano le caratteristiche visive da animare.</span><span class="sxs-lookup"><span data-stu-id="d34f8-118">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="d34f8-119">Creare uno storyboard e aggiungere transizioni</span><span class="sxs-lookup"><span data-stu-id="d34f8-119">Create a Storyboard and Add Transitions</span></span>](updating---timer-driven-animation.md)<br/>          | <span data-ttu-id="d34f8-120">Per creare un'animazione, un'applicazione deve costruire uno storyboard.</span><span class="sxs-lookup"><span data-stu-id="d34f8-120">To create an animation, an application must construct a storyboard.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="d34f8-121">Pianificare uno storyboard</span><span class="sxs-lookup"><span data-stu-id="d34f8-121">Schedule a Storyboard</span></span>](scheduling-a-storyboard.md)<br/>                                      | <span data-ttu-id="d34f8-122">Dopo la creazione di uno storyboard, questo viene pianificato dal gestore dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="d34f8-122">After a storyboard is created, it is scheduled by the animation manager.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="d34f8-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d34f8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d34f8-124">Cenni preliminari sull'animazione Windows</span><span class="sxs-lookup"><span data-stu-id="d34f8-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="d34f8-125">Informazioni di riferimento sull'animazione Windows</span><span class="sxs-lookup"><span data-stu-id="d34f8-125">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> <dt>

[<span data-ttu-id="d34f8-126">Esempi di animazioni Windows</span><span class="sxs-lookup"><span data-stu-id="d34f8-126">Windows Animation Samples</span></span>](windows-animation-samples.md)
</dt> </dl>

 

 





