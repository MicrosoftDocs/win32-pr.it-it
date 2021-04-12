---
title: Creare uno storyboard e aggiungere transizioni
description: Per creare un'animazione, un'applicazione deve costruire uno storyboard.
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- storyboard animazione Windows, creazione
- Animazione di Windows storyboard, aggiunta di transizioni
- transizioni animazione Windows, creazione
- esegue la transizione dell'animazione di Windows, aggiungendo allo storyboard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee85aac4db11371c9a1e4a2aa254421d217cfd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331647"
---
# <a name="create-a-storyboard-and-add-transitions"></a><span data-ttu-id="d066f-107">Creare uno storyboard e aggiungere transizioni</span><span class="sxs-lookup"><span data-stu-id="d066f-107">Create a Storyboard and Add Transitions</span></span>

<span data-ttu-id="d066f-108">Per creare un'animazione, un'applicazione deve costruire uno storyboard.</span><span class="sxs-lookup"><span data-stu-id="d066f-108">To create an animation, an application must construct a storyboard.</span></span>

## <a name="overview"></a><span data-ttu-id="d066f-109">Panoramica</span><span class="sxs-lookup"><span data-stu-id="d066f-109">Overview</span></span>

<span data-ttu-id="d066f-110">I passaggi generali per la creazione di uno storyboard sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d066f-110">The general steps for constructing a storyboard are as follows:</span></span>

1.  <span data-ttu-id="d066f-111">Creare uno storyboard</span><span class="sxs-lookup"><span data-stu-id="d066f-111">Create a storyboard</span></span>
2.  <span data-ttu-id="d066f-112">Creare una o più transizioni</span><span class="sxs-lookup"><span data-stu-id="d066f-112">Create one or more transitions</span></span>
3.  <span data-ttu-id="d066f-113">Aggiungere le transizioni allo storyboard, specificando quali variabili vengono animate</span><span class="sxs-lookup"><span data-stu-id="d066f-113">Add the transitions to the storyboard, specifying which variables they animate</span></span>

<span data-ttu-id="d066f-114">È possibile creare uno storyboard vuoto usando Gestione animazioni.</span><span class="sxs-lookup"><span data-stu-id="d066f-114">An empty storyboard can be created using the animation manager.</span></span> <span data-ttu-id="d066f-115">L'applicazione deve popolare ogni Storyboard con transizioni.</span><span class="sxs-lookup"><span data-stu-id="d066f-115">The application must populate each storyboard with transitions.</span></span> <span data-ttu-id="d066f-116">Ogni transizione specifica il modo in cui una singola variabile di animazione viene modificata in un intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="d066f-116">Each transition specifies how a single animation variable changes over a given time interval.</span></span> <span data-ttu-id="d066f-117">È possibile creare transizioni usando il componente della libreria di transizione incluso nell'animazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="d066f-117">Transitions can be created using the transition library component included in Windows Animation.</span></span> <span data-ttu-id="d066f-118">In alternativa, un'applicazione può creare le proprie transizioni personalizzate o usare una libreria di transizione da terze parti.</span><span class="sxs-lookup"><span data-stu-id="d066f-118">Alternately, an application can create its own custom transitions or use a transition library from a third party.</span></span> <span data-ttu-id="d066f-119">Quando l'applicazione aggiunge una transizione a uno storyboard, specifica quale variabile di animazione verrà animata dalla transizione.</span><span class="sxs-lookup"><span data-stu-id="d066f-119">When the application adds a transition to a storyboard, it specifies which animation variable the transition will animate.</span></span>

<span data-ttu-id="d066f-120">Uno storyboard può includere transizioni su una o più variabili di animazione.</span><span class="sxs-lookup"><span data-stu-id="d066f-120">A storyboard may include transitions on one or more animation variables.</span></span> <span data-ttu-id="d066f-121">Storyboard più complessi possono usare i fotogrammi chiave per sincronizzare l'inizio o la fine delle transizioni o per specificare parti dello storyboard che devono essere ripetute (un numero fisso di volte o a tempo indefinito).</span><span class="sxs-lookup"><span data-stu-id="d066f-121">More complex storyboards can use keyframes to synchronize the starts or ends of transitions, or to specify portions of the storyboard that should repeat (a fixed number of times or indefinitely).</span></span>

## <a name="example-code"></a><span data-ttu-id="d066f-122">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="d066f-122">Example Code</span></span>

<span data-ttu-id="d066f-123">Il codice di esempio seguente viene tratto da MainWindow. cpp nell' [animazione basata sul timer](timer-driven-animation-sample.md)di esempio di Windows Animation; vedere il metodo CMainWindow:: ChangeColor.</span><span class="sxs-lookup"><span data-stu-id="d066f-123">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::ChangeColor method.</span></span> <span data-ttu-id="d066f-124">Questo esempio crea lo storyboard (passaggio 1) usando il metodo [**IUIAnimationManager:: CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) , crea le transizioni (passaggio 2) usando il metodo [**IUIAnimationTransitionLibrary:: CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) e aggiunge le transizioni allo storyboard (passaggio 3) usando il metodo [**IUIAnimationStoryboard:: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) .</span><span class="sxs-lookup"><span data-stu-id="d066f-124">This example creates the storyboard (step 1) using the [**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) method, creates the transitions (step 2) using the [**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) method, and adds the transitions to the storyboard (step 3) using the [**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) method.</span></span>


```C++
const UI_ANIMATION_SECONDS DURATION = 0.5;
const DOUBLE ACCELERATION_RATIO = 0.5;
const DOUBLE DECELERATION_RATIO = 0.5;

// Create a storyboard

IUIAnimationStoryboard *pStoryboard = NULL;
HRESULT hr = m_pAnimationManager->CreateStoryboard(
    &pStoryboard
    );
if (SUCCEEDED(hr))
{
    // Create transitions for the RGB animation variables

    IUIAnimationTransition *pTransitionRed;
    hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
        DURATION,
        red,
        ACCELERATION_RATIO,
        DECELERATION_RATIO,
        &pTransitionRed
        );
    if (SUCCEEDED(hr))
    {
        IUIAnimationTransition *pTransitionGreen;
        hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
            DURATION,
            green,
            ACCELERATION_RATIO,
            DECELERATION_RATIO,
            &pTransitionGreen
            );
        if (SUCCEEDED(hr))
        {
            IUIAnimationTransition *pTransitionBlue;
            hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
                DURATION,
                blue,
                ACCELERATION_RATIO,
                DECELERATION_RATIO,
                &pTransitionBlue
                );
            if (SUCCEEDED(hr))
            {
                // Add transitions to the storyboard

                hr = pStoryboard->AddTransition(
                    m_pAnimationVariableRed,
                    pTransitionRed
                    );
                if (SUCCEEDED(hr))
                {
                    hr = pStoryboard->AddTransition(
                        m_pAnimationVariableGreen,
                        pTransitionGreen
                        );
                    if (SUCCEEDED(hr))
                    {
                        hr = pStoryboard->AddTransition(
                            m_pAnimationVariableBlue,
                            pTransitionBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            // Get the current time and schedule the storyboard for play

                            ...

}
```



## <a name="previous-step"></a><span data-ttu-id="d066f-125">Passaggio precedente</span><span class="sxs-lookup"><span data-stu-id="d066f-125">Previous Step</span></span>

<span data-ttu-id="d066f-126">Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [leggere i valori della variabile di animazione](updating---application-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="d066f-126">Before starting this step, you should have completed this step: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="d066f-127">passaggio successivo</span><span class="sxs-lookup"><span data-stu-id="d066f-127">Next Step</span></span>

<span data-ttu-id="d066f-128">Al termine di questo passaggio, il passaggio successivo è: [pianificare uno storyboard](scheduling-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="d066f-128">After completing this step, the next step is: [Schedule a Storyboard](scheduling-a-storyboard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d066f-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d066f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d066f-130">**IUIAnimationManager:: CreateStoryboard**</span><span class="sxs-lookup"><span data-stu-id="d066f-130">**IUIAnimationManager::CreateStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[<span data-ttu-id="d066f-131">**IUIAnimationStoryboard:: AddTransition**</span><span class="sxs-lookup"><span data-stu-id="d066f-131">**IUIAnimationStoryboard::AddTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[<span data-ttu-id="d066f-132">**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**</span><span class="sxs-lookup"><span data-stu-id="d066f-132">**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[<span data-ttu-id="d066f-133">Panoramica dello storyboard</span><span class="sxs-lookup"><span data-stu-id="d066f-133">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




