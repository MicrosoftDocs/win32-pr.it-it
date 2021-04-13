---
title: Creare variabili di animazione
description: Un'applicazione deve creare una variabile di animazione per ogni caratteristica visiva che deve essere animata usando l'animazione di Windows.
ms.assetid: 360aa157-cb50-400a-b373-45885410469d
keywords:
- Animazioni di Windows per variabili di animazione, creazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c059a924e22700bb4abd794435ad708a2775a9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399536"
---
# <a name="create-animation-variables"></a><span data-ttu-id="cc91f-104">Creare variabili di animazione</span><span class="sxs-lookup"><span data-stu-id="cc91f-104">Create Animation Variables</span></span>

<span data-ttu-id="cc91f-105">Un'applicazione deve creare una variabile di animazione per ogni caratteristica visiva che deve essere animata usando l'animazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="cc91f-105">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span>

## <a name="overview"></a><span data-ttu-id="cc91f-106">Panoramica</span><span class="sxs-lookup"><span data-stu-id="cc91f-106">Overview</span></span>

<span data-ttu-id="cc91f-107">Le variabili di animazione vengono create usando Gestione animazioni e l'applicazione deve mantenere un riferimento a ogni per tutto il tempo necessario.</span><span class="sxs-lookup"><span data-stu-id="cc91f-107">Animation variables are created using the animation manager, and the application should retain a reference to each for as long as it is needed.</span></span> <span data-ttu-id="cc91f-108">In genere, l'applicazione creerà ogni variabile di animazione allo stesso tempo dell'oggetto visivo a cui viene animato.</span><span class="sxs-lookup"><span data-stu-id="cc91f-108">Your application will generally create each animation variable at the same time as the visual object it animates.</span></span>

<span data-ttu-id="cc91f-109">Quando viene creata una variabile di animazione, è necessario specificare il valore iniziale.</span><span class="sxs-lookup"><span data-stu-id="cc91f-109">When an animation variable is created, its initial value must be specified.</span></span> <span data-ttu-id="cc91f-110">Successivamente, il suo valore può essere modificato solo tramite la pianificazione degli storyboard che lo animano.</span><span class="sxs-lookup"><span data-stu-id="cc91f-110">Thereafter, its value can only be altered by scheduling storyboards that animate it.</span></span>

<span data-ttu-id="cc91f-111">Le variabili di animazione vengono passate come parametri quando vengono costruiti gli storyboard, quindi l'applicazione non deve rilasciarle fino a quando non è più necessario animare le caratteristiche visive che rappresentano, in genere quando gli oggetti visivi associati stanno per essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="cc91f-111">Animation variables are passed as parameters when storyboards are constructed, so the application should not release them until the visual characteristics they represent no longer need to be animated, typically when the associated visual objects are about to be destroyed.</span></span>

## <a name="example-code"></a><span data-ttu-id="cc91f-112">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="cc91f-112">Example Code</span></span>

-   [<span data-ttu-id="cc91f-113">Animazione di colori</span><span class="sxs-lookup"><span data-stu-id="cc91f-113">Animating Colors</span></span>](#animating-colors)
-   [<span data-ttu-id="cc91f-114">Animazione delle coordinate x e y</span><span class="sxs-lookup"><span data-stu-id="cc91f-114">Animating x and y Coordinates</span></span>](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a><span data-ttu-id="cc91f-115">Animazione di colori</span><span class="sxs-lookup"><span data-stu-id="cc91f-115">Animating Colors</span></span>

<span data-ttu-id="cc91f-116">Il codice di esempio seguente viene tratto da MainWindow. cpp nell'animazione Windows esempi di animazione basata su [applicazioni](application-driven-animation-sample.md) e [animazione basata su timer](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="cc91f-116">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="cc91f-117">Nell'esempio, tre variabili di animazione vengono create usando [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) per rappresentare i colori di sfondo.</span><span class="sxs-lookup"><span data-stu-id="cc91f-117">In the example, three animation variables are created using [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) to represent background colors.</span></span> <span data-ttu-id="cc91f-118">Il codice usa anche i metodi [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) e [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) per controllare il valore della variabile di animazione.</span><span class="sxs-lookup"><span data-stu-id="cc91f-118">The code also uses the [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) methods to control the value of the animation variable.</span></span>


```
const DOUBLE INITIAL_RED = COLOR_MAX;
const DOUBLE INITIAL_GREEN = COLOR_MAX;
const DOUBLE INITIAL_BLUE = COLOR_MAX;

HRESULT hr = m_pAnimationManager->CreateAnimationVariable(
    INITIAL_RED,
    &m_pAnimationVariableRed
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableRed->SetLowerBound(COLOR_MIN);
    if (SUCCEEDED(hr))
    {
        hr = m_pAnimationVariableRed->SetUpperBound(COLOR_MAX);
        if (SUCCEEDED(hr))
        {
            hr = m_pAnimationManager->CreateAnimationVariable(
                INITIAL_GREEN,
                &m_pAnimationVariableGreen
                );
            if (SUCCEEDED(hr))
            {
                hr = m_pAnimationVariableGreen->SetLowerBound(COLOR_MIN);
                if (SUCCEEDED(hr))
                {
                    hr = m_pAnimationVariableGreen->SetUpperBound(COLOR_MAX);
                    if (SUCCEEDED(hr))
                    {
                        hr = m_pAnimationManager->CreateAnimationVariable(
                            INITIAL_BLUE,
                            &m_pAnimationVariableBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            hr = m_pAnimationVariableBlue->SetLowerBound(COLOR_MIN);
                            if (SUCCEEDED(hr))
                            {
                                hr = m_pAnimationVariableBlue->SetUpperBound(COLOR_MAX);
                            }
                        }
                    }
                }
            }
        }
    }
}
```



<span data-ttu-id="cc91f-119">Si notino le seguenti definizioni da MainWindow. h.</span><span class="sxs-lookup"><span data-stu-id="cc91f-119">Note the following definitions from MainWindow.h.</span></span>


```
class CMainWindow
{

    ...

private:

    // Animated Variables

    IUIAnimationVariable *m_pAnimationVariableRed;
    IUIAnimationVariable *m_pAnimationVariableGreen;
    IUIAnimationVariable *m_pAnimationVariableBlue;

    ...

};
```



### <a name="animating-x-and-y-coordinates"></a><span data-ttu-id="cc91f-120">Animazione delle coordinate x e y</span><span class="sxs-lookup"><span data-stu-id="cc91f-120">Animating x and y Coordinates</span></span>

<span data-ttu-id="cc91f-121">Il codice di esempio seguente viene tratto da thumbnail. cpp nell'esempio di [layout della griglia](/windows/desktop/UIAnimation/grid-layout-sample)di animazione Windows; vedere il metodo CMainWindow:: CreateAnimationVariables.</span><span class="sxs-lookup"><span data-stu-id="cc91f-121">The following example code is taken from Thumbnail.cpp in the Windows Animation [Grid Layout Sample](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::CreateAnimationVariables method.</span></span> <span data-ttu-id="cc91f-122">Vengono create due variabili di animazione per rappresentare le coordinate X e Y di ciascun oggetto.</span><span class="sxs-lookup"><span data-stu-id="cc91f-122">Two animation variables are created to represent the X and Y coordinates of each object.</span></span>


```C++
// Create the animation variables for the x and y coordinates

hr = m_pAnimationManager->CreateAnimationVariable(
    xInitial,
    &m_pAnimationVariableX
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->CreateAnimationVariable(
        yInitial,
        &m_pAnimationVariableY
        );

    ...

}
```



<span data-ttu-id="cc91f-123">Si notino le seguenti definizioni di thumbnail. h.</span><span class="sxs-lookup"><span data-stu-id="cc91f-123">Note the following definitions from Thumbnail.h.</span></span>


```
class CThumbnail
{
public:

    ...

    // X and Y Animation Variables

    IUIAnimationVariable *m_pAnimationVariableX;
    IUIAnimationVariable *m_pAnimationVariableY;

    ...

};
```



<span data-ttu-id="cc91f-124">Le variabili di animazione sono numeri a virgola mobile, ma anche i relativi valori possono essere recuperati come numeri interi.</span><span class="sxs-lookup"><span data-stu-id="cc91f-124">Animation variables are floating-point numbers, but their values can be fetched as integers, too.</span></span> <span data-ttu-id="cc91f-125">Per impostazione predefinita, ogni valore verrà arrotondato al numero intero più vicino, ma è possibile eseguire l'override della modalità di arrotondamento utilizzata per una variabile.</span><span class="sxs-lookup"><span data-stu-id="cc91f-125">By default, each value will be rounded to the nearest integer, but it is possible to override the rounding mode used for a variable.</span></span> <span data-ttu-id="cc91f-126">Il codice di esempio seguente usa il metodo [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) per specificare che i valori devono essere sempre arrotondati per difetto.</span><span class="sxs-lookup"><span data-stu-id="cc91f-126">The following example code uses the [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) method to specify that the values should always be rounded down.</span></span>


```C++
hr = m_pAnimationVariableX->SetRoundingMode(
    UI_ANIMATION_ROUNDING_MODE_FLOOR
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableY->SetRoundingMode(
        UI_ANIMATION_ROUNDING_MODE_FLOOR
        );

    ...

}
```



## <a name="previous-step"></a><span data-ttu-id="cc91f-127">Passaggio precedente</span><span class="sxs-lookup"><span data-stu-id="cc91f-127">Previous Step</span></span>

<span data-ttu-id="cc91f-128">Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [creare gli oggetti di animazione principali](adding-animation-to-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="cc91f-128">Before starting this step, you should have completed this step: [Create the Main Animation Objects](adding-animation-to-an-application.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="cc91f-129">passaggio successivo</span><span class="sxs-lookup"><span data-stu-id="cc91f-129">Next Step</span></span>

<span data-ttu-id="cc91f-130">Al termine di questo passaggio, il passaggio successivo è: [aggiornare gestione animazioni e creare frame](introducing-windows-animation-manager.md).</span><span class="sxs-lookup"><span data-stu-id="cc91f-130">After completing this step, the next step is: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc91f-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc91f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc91f-132">**IUIAnimationManager:: CreateAnimationVariable**</span><span class="sxs-lookup"><span data-stu-id="cc91f-132">**IUIAnimationManager::CreateAnimationVariable**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[<span data-ttu-id="cc91f-133">**IUIAnimationVariable:: SetLowerBound**</span><span class="sxs-lookup"><span data-stu-id="cc91f-133">**IUIAnimationVariable::SetLowerBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[<span data-ttu-id="cc91f-134">**IUIAnimationVariable:: SetRoundingMode**</span><span class="sxs-lookup"><span data-stu-id="cc91f-134">**IUIAnimationVariable::SetRoundingMode**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[<span data-ttu-id="cc91f-135">**IUIAnimationVariable:: SetUpperBound**</span><span class="sxs-lookup"><span data-stu-id="cc91f-135">**IUIAnimationVariable::SetUpperBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[<span data-ttu-id="cc91f-136">Cenni preliminari sull'animazione Windows</span><span class="sxs-lookup"><span data-stu-id="cc91f-136">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 