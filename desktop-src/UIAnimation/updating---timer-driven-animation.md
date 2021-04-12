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
# <a name="create-a-storyboard-and-add-transitions"></a>Creare uno storyboard e aggiungere transizioni

Per creare un'animazione, un'applicazione deve costruire uno storyboard.

## <a name="overview"></a>Panoramica

I passaggi generali per la creazione di uno storyboard sono i seguenti:

1.  Creare uno storyboard
2.  Creare una o più transizioni
3.  Aggiungere le transizioni allo storyboard, specificando quali variabili vengono animate

È possibile creare uno storyboard vuoto usando Gestione animazioni. L'applicazione deve popolare ogni Storyboard con transizioni. Ogni transizione specifica il modo in cui una singola variabile di animazione viene modificata in un intervallo di tempo specificato. È possibile creare transizioni usando il componente della libreria di transizione incluso nell'animazione di Windows. In alternativa, un'applicazione può creare le proprie transizioni personalizzate o usare una libreria di transizione da terze parti. Quando l'applicazione aggiunge una transizione a uno storyboard, specifica quale variabile di animazione verrà animata dalla transizione.

Uno storyboard può includere transizioni su una o più variabili di animazione. Storyboard più complessi possono usare i fotogrammi chiave per sincronizzare l'inizio o la fine delle transizioni o per specificare parti dello storyboard che devono essere ripetute (un numero fisso di volte o a tempo indefinito).

## <a name="example-code"></a>Codice di esempio

Il codice di esempio seguente viene tratto da MainWindow. cpp nell' [animazione basata sul timer](timer-driven-animation-sample.md)di esempio di Windows Animation; vedere il metodo CMainWindow:: ChangeColor. Questo esempio crea lo storyboard (passaggio 1) usando il metodo [**IUIAnimationManager:: CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) , crea le transizioni (passaggio 2) usando il metodo [**IUIAnimationTransitionLibrary:: CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) e aggiunge le transizioni allo storyboard (passaggio 3) usando il metodo [**IUIAnimationStoryboard:: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) .


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



## <a name="previous-step"></a>Passaggio precedente

Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [leggere i valori della variabile di animazione](updating---application-driven-animation.md).

## <a name="next-step"></a>passaggio successivo

Al termine di questo passaggio, il passaggio successivo è: [pianificare uno storyboard](scheduling-a-storyboard.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAnimationManager:: CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[**IUIAnimationStoryboard:: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[Panoramica dello storyboard](storyboard-construction.md)
</dt> </dl>

 

 




