---
title: Aggiornare gestione animazioni e creare frame
description: Ogni volta che un'applicazione pianifica uno storyboard, l'applicazione deve fornire l'ora corrente al gestore dell'animazione.
ms.assetid: c4f746c3-e47c-4b82-a41b-e2c0d177d097
keywords:
- Animazione Windows oggetti Animation Manager, aggiornamento
- animazione oggetti timer animazione Windows, connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9a48e8d6e273174e502c374727e69b61bc478d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046844"
---
# <a name="update-the-animation-manager-and-draw-frames"></a>Aggiornare gestione animazioni e creare frame

Ogni volta che un'applicazione pianifica uno storyboard, l'applicazione deve fornire l'ora corrente al gestore dell'animazione. L'ora corrente è necessaria anche quando si indica al gestore delle animazioni di aggiornare lo stato e impostare tutte le variabili di animazione sui valori interpolati appropriati.

## <a name="overview"></a>Panoramica

L'animazione Windows supporta due configurazioni: animazioni basate su applicazione e animazioni basate su timer.

Per usare un'animazione basata sull'applicazione nell'applicazione, è necessario aggiornare gestione animazioni prima di disegnare ogni frame e usare un meccanismo appropriato per disegnare i frame con una frequenza sufficiente per l'animazione. Un'applicazione che utilizza un'animazione basata su applicazione può utilizzare qualsiasi meccanismo per determinare l'ora corrente, ma l'oggetto timer di animazione Windows restituisce un tempo preciso nelle unità accettate dal gestore delle animazioni. Per evitare il disegno non necessario quando nessuna animazione viene riprodotta, è necessario fornire anche un gestore eventi di gestione per avviare il ridisegno quando le animazioni vengono pianificate e controllare dopo ogni frame se è possibile sospendere il ridisegno. Per altre informazioni, vedere [animazione basata su applicazioni](scenic-animation-api-overview.md).

Nella configurazione guidata dall'applicazione, un'applicazione può chiamare il metodo [**IUIAnimationManager:: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) per verificare che le animazioni siano attualmente pianificate e continuare a creare frame se sono. Poiché il ridisegno si interrompe quando non sono pianificate animazioni, è necessario riavviarlo alla successiva pianificazione di un'animazione. Un'applicazione può registrare un gestore eventi di gestione per ricevere una notifica quando lo stato del gestore animazioni viene modificato da inattivo (nessuna animazione attualmente pianificata) a occupato.

Per utilizzare l'animazione basata su timer nell'applicazione, è necessario connettere Gestione animazioni a un timer di animazione e fornire un gestore eventi timer. Quando la gestione animazioni è connessa a un timer, il timer può indicare al gestore quando lo stato dell'animazione deve essere aggiornato con l'avanzamento del tempo. L'applicazione deve creare un frame per ogni segno di selezione del timer. Il gestore animazione può a sua volta indicare al timer quando sono in esecuzione animazioni, quindi il timer può spegnersi durante i periodi di inattività quando il ridisegno non è necessario. Per evitare il disegno non necessario quando nessuna animazione viene riprodotta, è necessario configurare il timer in modo che venga disabilitato automaticamente. Per ulteriori informazioni, vedere [animazione basata su timer](scenic-animation-api-overview.md).

## <a name="example-code"></a>Codice di esempio

-   [Animazione basata su applicazioni](#application-driven-animation)
-   [Animazione basata su timer](#timer-driven-animation)

### <a name="application-driven-animation"></a>Animazione Application-Driven

Il codice di esempio seguente viene tratto da ManagerEventHandler. h dall'animazione di Windows esempi di [animazione basata su applicazioni](application-driven-animation-sample.md) e del [layout di griglia](/windows/desktop/UIAnimation/grid-layout-sample). Definisce il gestore dell'evento Manager.


```C++
#include "UIAnimationHelper.h"

// Event handler object for manager status changes

class CManagerEventHandler :
    public CUIAnimationManagerEventHandlerBase<CManagerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationManagerEventHandler **ppManagerEventHandler
    ) throw()
    {
        CManagerEventHandler *pManagerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppManagerEventHandler,
            &pManagerEventHandler
            );
        if (SUCCEEDED(hr))
        {
            pManagerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationManagerEventHandler

    IFACEMETHODIMP
    OnManagerStatusChanged
    (
        UI_ANIMATION_MANAGER_STATUS newStatus,
        UI_ANIMATION_MANAGER_STATUS previousStatus
    )
    {
        HRESULT hr = S_OK;

        if (newStatus == UI_ANIMATION_MANAGER_BUSY)
        {
            hr = m_pMainWindow->Invalidate();
        }

        return hr;
    }

    ...

};
```



Il codice di esempio seguente viene tratto da MainWindow. cpp dall' [animazione basata sull'applicazione](application-driven-animation-sample.md)di esempio di animazione Windows; vedere CMainWindow:: InitializeAnimation. Questo esempio crea un'istanza del gestore eventi Manager usando il metodo [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) e la passa al gestore delle animazioni usando il metodo [**IUIAnimationManager:: SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) .


```C++
// Create and set the ManagerEventHandler to start updating when animations are scheduled

IUIAnimationManagerEventHandler *pManagerEventHandler;
HRESULT hr = CManagerEventHandler::CreateInstance(
    this,
    &pManagerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->SetManagerEventHandler(
        pManagerEventHandler
        );
    pManagerEventHandler->Release();
}
```



Poiché il gestore dell'evento Manager mantiene un riferimento all'oggetto finestra principale, il gestore eventi Manager deve essere cancellato (passando **null** a [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) o il gestore animazione deve essere completamente rilasciato prima che la finestra principale venga distrutta.

Il codice di esempio seguente viene tratto da MainWindow. cpp nell'animazione Windows di esempio basata sull' [applicazione](application-driven-animation-sample.md). vedere il metodo CMainWindow:: OnPaint. Chiama il metodo [**IUIAnimationManager:: GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) per recuperare l'ora nelle unità richieste dal metodo [**IUIAnimationManager:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) .


```C++
// Update the animation manager with the current time

UI_ANIMATION_SECONDS secondsNow;
HRESULT hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->Update(
        secondsNow
        );

    ...

}
```



Il codice di esempio seguente viene tratto da MainWindow. cpp dagli esempi di animazione Windows e dal [layout griglia](/windows/desktop/UIAnimation/grid-layout-sample)e dall' [animazione basata sull'applicazione](application-driven-animation-sample.md) . vedere il metodo CMainWindow:: OnPaint. Si presuppone che l'applicazione usi un'API grafica che si sincronizza automaticamente con la frequenza di aggiornamento del monitoraggio (ad esempio Direct2D con le impostazioni predefinite), nel qual caso una chiamata alla funzione [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) è sufficiente per garantire che il codice di disegno venga chiamato nuovamente quando è il momento di disegnare il frame successivo. Anziché chiamare **InvalidateRect** in modo incondizionato, è preferibile controllare se esistono ancora animazioni pianificate tramite [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).


```C++
// Read the values of the animation variables and draw the client area

hr = DrawClientArea();
if (SUCCEEDED(hr))
{          
    // Continue redrawing the client area as long as there are animations scheduled
    UI_ANIMATION_MANAGER_STATUS status;
    hr = m_pAnimationManager->GetStatus(
        &status
        );
    if (SUCCEEDED(hr))
    {
        if (status == UI_ANIMATION_MANAGER_BUSY)
        {
            InvalidateRect(
                m_hwnd,
                NULL,
                FALSE
                );
        }
    }
}
```



### <a name="timer-driven-animation"></a>Animazione Timer-Driven

Il codice di esempio seguente viene tratto da TimerEventHandler. h dall' [animazione basata sul timer](timer-driven-animation-sample.md)di esempio di animazione Windows. Il codice di esempio definisce il gestore dell'evento timer, che invalida l'area client della finestra in modo che causi un ridisegno dopo ogni aggiornamento dello stato dell'animazione.


```C++
#include "UIAnimationHelper.h"

// Event handler object for timer events

class CTimerEventHandler :
    public CUIAnimationTimerEventHandlerBase<CTimerEventHandler>
{
public:

    static HRESULT
    CreateInstance
    (
        CMainWindow *pMainWindow,
        IUIAnimationTimerEventHandler **ppTimerEventHandler
    ) throw()
    {
        CTimerEventHandler *pTimerEventHandler;
        HRESULT hr = CUIAnimationCallbackBase::CreateInstance(
            ppTimerEventHandler,
            &pTimerEventHandler
            );

        if (SUCCEEDED(hr))
        {
            pTimerEventHandler->m_pMainWindow = pMainWindow;
        }
        
        return hr;
    }

    // IUIAnimationTimerEventHandler

    IFACEMETHODIMP
    OnPreUpdate()
    {
        return S_OK;
    }

    IFACEMETHODIMP
    OnPostUpdate()
    {
        HRESULT hr = m_pMainWindow->Invalidate();

        return hr;
    }

    IFACEMETHODIMP
    OnRenderingTooSlow
    (
        UINT32 /* fps */
    )
    {
        return S_OK;
    }

    ...

};
```



Il codice di esempio seguente viene tratto da MainWindow. cpp dall' [animazione basata sul timer](timer-driven-animation-sample.md)di esempio di animazione Windows; vedere CMainWindow:: InitializeAnimation. Questo esempio crea un'istanza del gestore eventi timer usando il metodo [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) e la passa al timer usando il metodo [**IUIAnimationTimer:: SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) . Poiché il gestore dell'evento timer mantiene un riferimento all'oggetto finestra principale, il gestore eventi del timer deve essere cancellato (passando **null** a **SetTimerEventHandler**) o il timer rilasciato completamente prima che la finestra principale venga distrutta.


```C++
// Create and set the timer event handler

IUIAnimationTimerEventHandler *pTimerEventHandler;
hr = CTimerEventHandler::CreateInstance(
    this,
    &pTimerEventHandler
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerEventHandler(
        pTimerEventHandler
        );
    pTimerEventHandler->Release();
}
```



Il codice di esempio seguente viene tratto da MainWindow. cpp nell' [animazione basata sul timer](timer-driven-animation-sample.md)di esempio di Windows Animation; vedere il metodo CMainWindow:: InitializeAnimation. Chiama il metodo [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto Gestione animazioni per ottenere un puntatore a [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), quindi connette gli oggetti [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) e [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) impostando gestione animazioni come gestore di aggiornamento del timer usando il metodo [**IUIAnimationTimer:: SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) . Si noti che non è necessario cancellare esplicitamente la connessione; la connessione viene cancellata in modo sicuro dopo che l'applicazione rilascia sia il gestore animazione sia il timer animazione.


```C++
// Connect the animation manager to the timer

IUIAnimationTimerUpdateHandler *pTimerUpdateHandler;
hr = m_pAnimationManager->QueryInterface(
    IID_PPV_ARGS(&pTimerUpdateHandler)
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationTimer->SetTimerUpdateHandler(
        pTimerUpdateHandler
        UI_ANIMATION_IDLE_BEHAVIOR_DISABLE  // timer will shut itself off when there are no animations playing
        );
    pTimerUpdateHandler->Release();
    if (SUCCEEDED(hr))
    {
        // Create and set the timer event handler

        ...

    }
}
```



Se non viene usato il **\_ \_ comportamento di inattività dell'animazione \_ \_ dell'interfaccia utente** , è anche necessario abilitare il timer per avviarlo.

## <a name="previous-step"></a>Passaggio precedente

Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [creare variabili di animazione](create-animation-variables.md).

## <a name="next-step"></a>passaggio successivo

Al termine di questo passaggio, il passaggio successivo è: [leggere i valori delle variabili di animazione](updating---application-driven-animation.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAnimationManager:: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[**IUIAnimationManager:: SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[**IUIAnimationManager:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[**IUIAnimationTimer:: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[**IUIAnimationTimer:: SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))
</dt> <dt>

[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))
</dt> <dt>

[Cenni preliminari sull'animazione Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 