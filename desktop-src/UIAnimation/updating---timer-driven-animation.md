---
title: Creare uno storyboard e aggiungere transizioni
description: Per creare un'animazione, un'applicazione deve costruire uno storyboard.
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- storyboard Windows Animation, creazione
- storyboard Windows Animation , aggiunta di transizioni
- transizioni Windows animation, creazione
- transizioni Windows animation , aggiunta allo storyboard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f992ae7720fea692d5e0b813e6cb9c35fab61d4bf2c781c928d9c8fcd08adb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999641"
---
# <a name="create-a-storyboard-and-add-transitions"></a>Creare uno storyboard e aggiungere transizioni

Per creare un'animazione, un'applicazione deve costruire uno storyboard.

## <a name="overview"></a>Panoramica

I passaggi generali per la creazione di uno storyboard sono i seguenti:

1.  Creare uno storyboard
2.  Creare una o più transizioni
3.  Aggiungere le transizioni allo storyboard, specificando le variabili da animare

È possibile creare uno storyboard vuoto usando il gestore dell'animazione. L'applicazione deve popolare ogni storyboard con transizioni. Ogni transizione specifica il modo in cui una singola variabile di animazione cambia in un determinato intervallo di tempo. Le transizioni possono essere create usando il componente della libreria di transizione incluso in Windows animation. In alternativa, un'applicazione può creare transizioni personalizzate o usare una libreria di transizione di terze parti. Quando l'applicazione aggiunge una transizione a uno storyboard, specifica la variabile di animazione che verrà animata dalla transizione.

Uno storyboard può includere transizioni in una o più variabili di animazione. Gli storyboard più complessi possono usare fotogrammi chiave per sincronizzare gli inizi o le estremità delle transizioni o per specificare parti dello storyboard che devono essere ripetute (un numero fisso di volte o per un periodo illimitato).

## <a name="example-code"></a>Codice di esempio

Il codice di esempio seguente è tratto da MainWindow.cpp nell'esempio di Windows animation basata su [timer](timer-driven-animation-sample.md); vedere il metodo CMainWindow::ChangeColor. Questo esempio crea lo storyboard (passaggio 1) usando il metodo [**IUIAnimationManager::CreateStoryboard,**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) crea le transizioni (passaggio 2) usando il metodo [**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) e aggiunge le transizioni allo storyboard (passaggio 3) usando il metodo [**IUIAnimationStoryboard::AddTransition.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)


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

Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [Leggere i valori delle variabili di animazione](updating---application-driven-animation.md).

## <a name="next-step"></a>passaggio successivo

Dopo aver completato questo passaggio, il passaggio successivo è: [Pianificare uno storyboard](scheduling-a-storyboard.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[Cenni preliminari su Storyboard](storyboard-construction.md)
</dt> </dl>

 

 




