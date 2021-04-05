---
title: Interfacce storyboard
description: In questa sezione sono contenute le specifiche di riferimento per le interfacce di Windows Animation Manager che supportano gli storyboard.
ms.assetid: 372D6348-3DF2-48EB-B495-BAD4E5DAAAD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fba60c480ef4c316731da6eefbe5334616a72b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046932"
---
# <a name="storyboard-interfaces"></a><span data-ttu-id="b318c-103">Interfacce storyboard</span><span class="sxs-lookup"><span data-stu-id="b318c-103">Storyboard Interfaces</span></span>

<span data-ttu-id="b318c-104">In questa sezione sono contenute le specifiche di riferimento per le interfacce di Windows Animation Manager che supportano gli storyboard.</span><span class="sxs-lookup"><span data-stu-id="b318c-104">This section contains the reference specifications for the Windows Animation Manager interfaces that support storyboards.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b318c-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b318c-105">In this section</span></span>



| <span data-ttu-id="b318c-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="b318c-106">Topic</span></span>                                                                                                 | <span data-ttu-id="b318c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b318c-107">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b318c-108">**IUIAnimationStoryboard**</span><span class="sxs-lookup"><span data-stu-id="b318c-108">**IUIAnimationStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)<br/>                                   | <span data-ttu-id="b318c-109">Definisce uno storyboard che contiene un gruppo di transizioni sincronizzate l'una rispetto all'altra.</span><span class="sxs-lookup"><span data-stu-id="b318c-109">Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.</span></span><br/> |
| [<span data-ttu-id="b318c-110">**IUIAnimationStoryboard2**</span><span class="sxs-lookup"><span data-stu-id="b318c-110">**IUIAnimationStoryboard2**</span></span>](/windows/win32/api/uianimation/nn-uianimation-iuianimationstoryboard2)<br/>                                 | <span data-ttu-id="b318c-111">Definisce uno storyboard che contiene un gruppo di transizioni sincronizzate l'una rispetto all'altra.</span><span class="sxs-lookup"><span data-stu-id="b318c-111">Defines a storyboard, which contains a group of transitions that are synchronized relative to one another.</span></span><br/> |
| [<span data-ttu-id="b318c-112">**IUIAnimationStoryboardEventHandler**</span><span class="sxs-lookup"><span data-stu-id="b318c-112">**IUIAnimationStoryboardEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboardeventhandler)<br/>           | <span data-ttu-id="b318c-113">Definisce i metodi per la gestione degli eventi di stato e di aggiornamento per uno storyboard.</span><span class="sxs-lookup"><span data-stu-id="b318c-113">Defines methods for handling status and update events for a storyboard.</span></span><br/>                                    |
| [<span data-ttu-id="b318c-114">**IUIAnimationStoryboardEventHandler2**</span><span class="sxs-lookup"><span data-stu-id="b318c-114">**IUIAnimationStoryboardEventHandler2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboardeventhandler2)<br/>         | <span data-ttu-id="b318c-115">Definisce i metodi per la gestione degli eventi Storyboard.</span><span class="sxs-lookup"><span data-stu-id="b318c-115">Defines methods for handling storyboard events.</span></span> <br/>                                                           |
| [<span data-ttu-id="b318c-116">**IUIAnimationLoopIterationChangeHandler2**</span><span class="sxs-lookup"><span data-stu-id="b318c-116">**IUIAnimationLoopIterationChangeHandler2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationloopiterationchangehandler2)<br/> | <span data-ttu-id="b318c-117">Definisce un metodo per la gestione degli eventi di iterazione del ciclo storyboard.</span><span class="sxs-lookup"><span data-stu-id="b318c-117">Defines a method for handling storyboard loop iteration events.</span></span><br/>                                            |
| [<span data-ttu-id="b318c-118">**IUIAnimationPriorityComparison**</span><span class="sxs-lookup"><span data-stu-id="b318c-118">**IUIAnimationPriorityComparison**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)<br/>                   | <span data-ttu-id="b318c-119">Definisce un metodo per il confronto di priorità usato dal gestore animazione per risolvere i conflitti di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="b318c-119">Defines a method for priority comparison that the animation manager uses to resolve scheduling conflicts.</span></span><br/>  |
| [<span data-ttu-id="b318c-120">**IUIAnimationPriorityComparison2**</span><span class="sxs-lookup"><span data-stu-id="b318c-120">**IUIAnimationPriorityComparison2**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison2)<br/>                 | <span data-ttu-id="b318c-121">Definisce un metodo che risolve i conflitti di pianificazione tramite il confronto di priorità.</span><span class="sxs-lookup"><span data-stu-id="b318c-121">Defines a method that resolves scheduling conflicts through priority comparison.</span></span><br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="b318c-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b318c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b318c-123">Interfacce</span><span class="sxs-lookup"><span data-stu-id="b318c-123">Interfaces</span></span>](windows-animation-reference.md)
</dt> </dl>

 

