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
# <a name="update-the-animation-manager-and-draw-frames"></a><span data-ttu-id="8a576-105">Aggiornare gestione animazioni e creare frame</span><span class="sxs-lookup"><span data-stu-id="8a576-105">Update the Animation Manager and Draw Frames</span></span>

<span data-ttu-id="8a576-106">Ogni volta che un'applicazione pianifica uno storyboard, l'applicazione deve fornire l'ora corrente al gestore dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="8a576-106">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="8a576-107">L'ora corrente è necessaria anche quando si indica al gestore delle animazioni di aggiornare lo stato e impostare tutte le variabili di animazione sui valori interpolati appropriati.</span><span class="sxs-lookup"><span data-stu-id="8a576-107">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span>

## <a name="overview"></a><span data-ttu-id="8a576-108">Panoramica</span><span class="sxs-lookup"><span data-stu-id="8a576-108">Overview</span></span>

<span data-ttu-id="8a576-109">L'animazione Windows supporta due configurazioni: animazioni basate su applicazione e animazioni basate su timer.</span><span class="sxs-lookup"><span data-stu-id="8a576-109">There are two configurations supported by Windows Animation: application-driven animation and timer-driven animation.</span></span>

<span data-ttu-id="8a576-110">Per usare un'animazione basata sull'applicazione nell'applicazione, è necessario aggiornare gestione animazioni prima di disegnare ogni frame e usare un meccanismo appropriato per disegnare i frame con una frequenza sufficiente per l'animazione.</span><span class="sxs-lookup"><span data-stu-id="8a576-110">To use application-driven animation in your application, you must update the animation manager before drawing each frame and use an appropriate mechanism to draw frames frequently enough for animation.</span></span> <span data-ttu-id="8a576-111">Un'applicazione che utilizza un'animazione basata su applicazione può utilizzare qualsiasi meccanismo per determinare l'ora corrente, ma l'oggetto timer di animazione Windows restituisce un tempo preciso nelle unità accettate dal gestore delle animazioni.</span><span class="sxs-lookup"><span data-stu-id="8a576-111">An application using application-driven animation can use any mechanism to determine the current time, but the Windows Animation timer object returns a precise time in the units accepted by the animation manager.</span></span> <span data-ttu-id="8a576-112">Per evitare il disegno non necessario quando nessuna animazione viene riprodotta, è necessario fornire anche un gestore eventi di gestione per avviare il ridisegno quando le animazioni vengono pianificate e controllare dopo ogni frame se è possibile sospendere il ridisegno.</span><span class="sxs-lookup"><span data-stu-id="8a576-112">To avoid unnecessary drawing when no animations are playing, you should also provide a manager event handler to start redrawing when animations are scheduled and check after each frame whether redrawing can be suspended.</span></span> <span data-ttu-id="8a576-113">Per altre informazioni, vedere [animazione basata su applicazioni](scenic-animation-api-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8a576-113">For more information, see [Application-Driven Animation](scenic-animation-api-overview.md).</span></span>

<span data-ttu-id="8a576-114">Nella configurazione guidata dall'applicazione, un'applicazione può chiamare il metodo [**IUIAnimationManager:: GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) per verificare che le animazioni siano attualmente pianificate e continuare a creare frame se sono.</span><span class="sxs-lookup"><span data-stu-id="8a576-114">In the application-driven configuration, an application can call the [**IUIAnimationManager::GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus) method to verify that animations are currently scheduled and continue to draw frames if they are.</span></span> <span data-ttu-id="8a576-115">Poiché il ridisegno si interrompe quando non sono pianificate animazioni, è necessario riavviarlo alla successiva pianificazione di un'animazione.</span><span class="sxs-lookup"><span data-stu-id="8a576-115">Because redrawing stops when there are no animations scheduled, it is necessary to restart it the next time an animation is scheduled.</span></span> <span data-ttu-id="8a576-116">Un'applicazione può registrare un gestore eventi di gestione per ricevere una notifica quando lo stato del gestore animazioni viene modificato da inattivo (nessuna animazione attualmente pianificata) a occupato.</span><span class="sxs-lookup"><span data-stu-id="8a576-116">An application can register a manager event handler to be notified when the status of the animation manager changes from idle (no animations are currently scheduled) to busy.</span></span>

<span data-ttu-id="8a576-117">Per utilizzare l'animazione basata su timer nell'applicazione, è necessario connettere Gestione animazioni a un timer di animazione e fornire un gestore eventi timer.</span><span class="sxs-lookup"><span data-stu-id="8a576-117">To use timer-driven animation in your application, you must connect the animation manager to an animation timer and provide a timer event handler.</span></span> <span data-ttu-id="8a576-118">Quando la gestione animazioni è connessa a un timer, il timer può indicare al gestore quando lo stato dell'animazione deve essere aggiornato con l'avanzamento del tempo.</span><span class="sxs-lookup"><span data-stu-id="8a576-118">When the animation manager is connected to a timer, the timer can tell the manager when the animation state should be updated as time progresses.</span></span> <span data-ttu-id="8a576-119">L'applicazione deve creare un frame per ogni segno di selezione del timer.</span><span class="sxs-lookup"><span data-stu-id="8a576-119">The application should draw a frame for each timer tick.</span></span> <span data-ttu-id="8a576-120">Il gestore animazione può a sua volta indicare al timer quando sono in esecuzione animazioni, quindi il timer può spegnersi durante i periodi di inattività quando il ridisegno non è necessario.</span><span class="sxs-lookup"><span data-stu-id="8a576-120">The animation manager can in turn tell the timer when there are animations playing, so the timer can shut itself off during idle periods when redrawing is unnecessary.</span></span> <span data-ttu-id="8a576-121">Per evitare il disegno non necessario quando nessuna animazione viene riprodotta, è necessario configurare il timer in modo che venga disabilitato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8a576-121">To avoid unnecessary drawing when no animations are playing, you should configure the timer to disable itself automatically.</span></span> <span data-ttu-id="8a576-122">Per ulteriori informazioni, vedere [animazione basata su timer](scenic-animation-api-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8a576-122">For more information, see [Timer-Driven Animation](scenic-animation-api-overview.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="8a576-123">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="8a576-123">Example Code</span></span>

-   [<span data-ttu-id="8a576-124">Animazione basata su applicazioni</span><span class="sxs-lookup"><span data-stu-id="8a576-124">Application-Driven Animation</span></span>](#application-driven-animation)
-   [<span data-ttu-id="8a576-125">Animazione basata su timer</span><span class="sxs-lookup"><span data-stu-id="8a576-125">Timer-Driven Animation</span></span>](#timer-driven-animation)

### <a name="application-driven-animation"></a><span data-ttu-id="8a576-126">Animazione Application-Driven</span><span class="sxs-lookup"><span data-stu-id="8a576-126">Application-Driven Animation</span></span>

<span data-ttu-id="8a576-127">Il codice di esempio seguente viene tratto da ManagerEventHandler. h dall'animazione di Windows esempi di [animazione basata su applicazioni](application-driven-animation-sample.md) e del [layout di griglia](/windows/desktop/UIAnimation/grid-layout-sample).</span><span class="sxs-lookup"><span data-stu-id="8a576-127">The following example code is taken from ManagerEventHandler.h from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample).</span></span> <span data-ttu-id="8a576-128">Definisce il gestore dell'evento Manager.</span><span class="sxs-lookup"><span data-stu-id="8a576-128">It defines the manager event handler.</span></span>


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



<span data-ttu-id="8a576-129">Il codice di esempio seguente viene tratto da MainWindow. cpp dall' [animazione basata sull'applicazione](application-driven-animation-sample.md)di esempio di animazione Windows; vedere CMainWindow:: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="8a576-129">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="8a576-130">Questo esempio crea un'istanza del gestore eventi Manager usando il metodo [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) e la passa al gestore delle animazioni usando il metodo [**IUIAnimationManager:: SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) .</span><span class="sxs-lookup"><span data-stu-id="8a576-130">This example creates an instance of the manager event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the animation manager using the [**IUIAnimationManager::SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler) method.</span></span>


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



<span data-ttu-id="8a576-131">Poiché il gestore dell'evento Manager mantiene un riferimento all'oggetto finestra principale, il gestore eventi Manager deve essere cancellato (passando **null** a [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) o il gestore animazione deve essere completamente rilasciato prima che la finestra principale venga distrutta.</span><span class="sxs-lookup"><span data-stu-id="8a576-131">Because the manager event handler retains a reference to the main window object, the manager event handler should be cleared (by passing **NULL** to [**SetManagerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)) or the animation manager should be completely released before the main window is destroyed.</span></span>

<span data-ttu-id="8a576-132">Il codice di esempio seguente viene tratto da MainWindow. cpp nell'animazione Windows di esempio basata sull' [applicazione](application-driven-animation-sample.md). vedere il metodo CMainWindow:: OnPaint.</span><span class="sxs-lookup"><span data-stu-id="8a576-132">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Application-Driven Animation](application-driven-animation-sample.md); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="8a576-133">Chiama il metodo [**IUIAnimationManager:: GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) per recuperare l'ora nelle unità richieste dal metodo [**IUIAnimationManager:: Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) .</span><span class="sxs-lookup"><span data-stu-id="8a576-133">It calls the [**IUIAnimationManager::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime) method to retrieve the time in the units required by the [**IUIAnimationManager::Update**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update) method.</span></span>


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



<span data-ttu-id="8a576-134">Il codice di esempio seguente viene tratto da MainWindow. cpp dagli esempi di animazione Windows e dal [layout griglia](/windows/desktop/UIAnimation/grid-layout-sample)e dall' [animazione basata sull'applicazione](application-driven-animation-sample.md) . vedere il metodo CMainWindow:: OnPaint.</span><span class="sxs-lookup"><span data-stu-id="8a576-134">The following example code is taken from MainWindow.cpp from the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::OnPaint method.</span></span> <span data-ttu-id="8a576-135">Si presuppone che l'applicazione usi un'API grafica che si sincronizza automaticamente con la frequenza di aggiornamento del monitoraggio (ad esempio Direct2D con le impostazioni predefinite), nel qual caso una chiamata alla funzione [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) è sufficiente per garantire che il codice di disegno venga chiamato nuovamente quando è il momento di disegnare il frame successivo.</span><span class="sxs-lookup"><span data-stu-id="8a576-135">It assumes that the application is using a graphics API that automatically synchronizes to the monitor refresh rate (such as Direct2D with its default settings), in which case a call to the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function is enough to ensure that the painting code will be called again when it is time to draw the next frame.</span></span> <span data-ttu-id="8a576-136">Anziché chiamare **InvalidateRect** in modo incondizionato, è preferibile controllare se esistono ancora animazioni pianificate tramite [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).</span><span class="sxs-lookup"><span data-stu-id="8a576-136">Rather than call **InvalidateRect** unconditionally, it is better to check if there are still any animations scheduled using [**GetStatus**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus).</span></span>


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



### <a name="timer-driven-animation"></a><span data-ttu-id="8a576-137">Animazione Timer-Driven</span><span class="sxs-lookup"><span data-stu-id="8a576-137">Timer-Driven Animation</span></span>

<span data-ttu-id="8a576-138">Il codice di esempio seguente viene tratto da TimerEventHandler. h dall' [animazione basata sul timer](timer-driven-animation-sample.md)di esempio di animazione Windows.</span><span class="sxs-lookup"><span data-stu-id="8a576-138">The following example code is taken from TimerEventHandler.h from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="8a576-139">Il codice di esempio definisce il gestore dell'evento timer, che invalida l'area client della finestra in modo che causi un ridisegno dopo ogni aggiornamento dello stato dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="8a576-139">The example code defines the timer event handler, which invalidates the window's client area to cause a repaint after each update of the animation state.</span></span>


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



<span data-ttu-id="8a576-140">Il codice di esempio seguente viene tratto da MainWindow. cpp dall' [animazione basata sul timer](timer-driven-animation-sample.md)di esempio di animazione Windows; vedere CMainWindow:: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="8a576-140">The following example code is taken from MainWindow.cpp from the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see CMainWindow::InitializeAnimation.</span></span> <span data-ttu-id="8a576-141">Questo esempio crea un'istanza del gestore eventi timer usando il metodo [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) e la passa al timer usando il metodo [**IUIAnimationTimer:: SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) .</span><span class="sxs-lookup"><span data-stu-id="8a576-141">This example creates an instance of the timer event handler using the [**CreateInstance**](/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance) method and passes it to the timer using the [**IUIAnimationTimer::SetTimerEventHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimereventhandler) method.</span></span> <span data-ttu-id="8a576-142">Poiché il gestore dell'evento timer mantiene un riferimento all'oggetto finestra principale, il gestore eventi del timer deve essere cancellato (passando **null** a **SetTimerEventHandler**) o il timer rilasciato completamente prima che la finestra principale venga distrutta.</span><span class="sxs-lookup"><span data-stu-id="8a576-142">Because the timer event handler retains a reference to the main window object, the timer event handler should be cleared (by passing **NULL** to **SetTimerEventHandler**) or the timer completely released before the main window is destroyed.</span></span>


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



<span data-ttu-id="8a576-143">Il codice di esempio seguente viene tratto da MainWindow. cpp nell' [animazione basata sul timer](timer-driven-animation-sample.md)di esempio di Windows Animation; vedere il metodo CMainWindow:: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="8a576-143">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::InitializeAnimation method.</span></span> <span data-ttu-id="8a576-144">Chiama il metodo [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto Gestione animazioni per ottenere un puntatore a [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), quindi connette gli oggetti [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) e [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) impostando gestione animazioni come gestore di aggiornamento del timer usando il metodo [**IUIAnimationTimer:: SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) .</span><span class="sxs-lookup"><span data-stu-id="8a576-144">It calls the [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the animation manager object to get a pointer to [**IUIAnimationTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimerupdatehandler), then connects the [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)) and [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)) objects by setting the animation manager as the timer's update handler using the [**IUIAnimationTimer::SetTimerUpdateHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler) method.</span></span> <span data-ttu-id="8a576-145">Si noti che non è necessario cancellare esplicitamente la connessione; la connessione viene cancellata in modo sicuro dopo che l'applicazione rilascia sia il gestore animazione sia il timer animazione.</span><span class="sxs-lookup"><span data-stu-id="8a576-145">Note that it is not necessary to explicitly clear this connection; the connection is cleared safely after the application releases both the animation manager and the animation timer.</span></span>


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



<span data-ttu-id="8a576-146">Se non viene usato il **\_ \_ comportamento di inattività dell'animazione \_ \_ dell'interfaccia utente** , è anche necessario abilitare il timer per avviarlo.</span><span class="sxs-lookup"><span data-stu-id="8a576-146">If **UI\_ANIMATION\_IDLE\_BEHAVIOR\_DISABLE** is not used, it is also necessary to enable the timer to start it ticking.</span></span>

## <a name="previous-step"></a><span data-ttu-id="8a576-147">Passaggio precedente</span><span class="sxs-lookup"><span data-stu-id="8a576-147">Previous Step</span></span>

<span data-ttu-id="8a576-148">Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [creare variabili di animazione](create-animation-variables.md).</span><span class="sxs-lookup"><span data-stu-id="8a576-148">Before starting this step, you should have completed this step: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="8a576-149">passaggio successivo</span><span class="sxs-lookup"><span data-stu-id="8a576-149">Next Step</span></span>

<span data-ttu-id="8a576-150">Al termine di questo passaggio, il passaggio successivo è: [leggere i valori delle variabili di animazione](updating---application-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="8a576-150">After completing this step, the next step is: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a576-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a576-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a576-152">**IUIAnimationManager:: GetStatus**</span><span class="sxs-lookup"><span data-stu-id="8a576-152">**IUIAnimationManager::GetStatus**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-getstatus)
</dt> <dt>

[<span data-ttu-id="8a576-153">**IUIAnimationManager:: SetManagerEventHandler**</span><span class="sxs-lookup"><span data-stu-id="8a576-153">**IUIAnimationManager::SetManagerEventHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-setmanagereventhandler)
</dt> <dt>

[<span data-ttu-id="8a576-154">**IUIAnimationManager:: Update**</span><span class="sxs-lookup"><span data-stu-id="8a576-154">**IUIAnimationManager::Update**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-update)
</dt> <dt>

[<span data-ttu-id="8a576-155">**IUIAnimationTimer:: getTime**</span><span class="sxs-lookup"><span data-stu-id="8a576-155">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="8a576-156">**IUIAnimationTimer:: SetTimerUpdateHandler**</span><span class="sxs-lookup"><span data-stu-id="8a576-156">**IUIAnimationTimer::SetTimerUpdateHandler**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-settimerupdatehandler)
</dt> <dt>

<span data-ttu-id="8a576-157">[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8a576-157">[**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8a576-158">[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8a576-158">[**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8a576-159">Cenni preliminari sull'animazione Windows</span><span class="sxs-lookup"><span data-stu-id="8a576-159">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 