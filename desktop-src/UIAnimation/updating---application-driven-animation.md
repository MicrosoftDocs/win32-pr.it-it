---
title: Leggere i valori delle variabili di animazione
description: Ogni volta che l'applicazione disegna, deve leggere i valori correnti delle variabili di animazione che rappresentano le caratteristiche visive da animare.
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- variabili di animazione Windows Animation, Reading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16187547bb3efd99a2f45a8fcc0668a6b6603efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300070"
---
# <a name="read-the-animation-variable-values"></a><span data-ttu-id="84815-104">Leggere i valori delle variabili di animazione</span><span class="sxs-lookup"><span data-stu-id="84815-104">Read the Animation Variable Values</span></span>

<span data-ttu-id="84815-105">Ogni volta che l'applicazione disegna, deve leggere i valori correnti delle variabili di animazione che rappresentano le caratteristiche visive da animare.</span><span class="sxs-lookup"><span data-stu-id="84815-105">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span>

## <a name="overview"></a><span data-ttu-id="84815-106">Panoramica</span><span class="sxs-lookup"><span data-stu-id="84815-106">Overview</span></span>

<span data-ttu-id="84815-107">Quando si disegna un frame, un'applicazione può usare il metodo [**IUIAnimationVariable:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) o [**IUIAnimationVariable:: GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) per richiedere i valori di qualsiasi variabile di animazione che influirà sugli oggetti visivi all'interno del frame.</span><span class="sxs-lookup"><span data-stu-id="84815-107">When drawing a frame, an application can use the [**IUIAnimationVariable::GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) or [**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to request the values of any animation variables that will affect visuals within the frame.</span></span> <span data-ttu-id="84815-108">È possibile ritagliare una variabile di animazione in un intervallo di valori ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) e [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) e per richiedere che il relativo valore venga arrotondato a un Integer usando uno schema di arrotondamento specificato ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).</span><span class="sxs-lookup"><span data-stu-id="84815-108">It is possible to clip an animation variable to a range of values ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)), and to request its value be rounded to an integer using a specified rounding scheme ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).</span></span>

<span data-ttu-id="84815-109">Anziché leggere i valori di tutte le variabili per ogni fotogramma, un'applicazione può usare il metodo [**IUIAnimationVariable:: SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) o [**IUIAnimationVariable:: SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) per registrare uno o più gestori di modifiche variabili per ricevere le notifiche solo quando viene apportata una modifica al valore delle variabili ([**IUIAnimationVariableChangeHandler:**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged): OnValueChanged) o al valore arrotondato ([**IUIAnimationVariableIntegerChangeHandler:: OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)).</span><span class="sxs-lookup"><span data-stu-id="84815-109">Instead of reading the values of all variables for every frame, an application can use the [**IUIAnimationVariable::SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) or [**IUIAnimationVariable::SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) method to register one or more variable change handlers to receive notifications only when there is a change to the variables' value ([**IUIAnimationVariableChangeHandler::OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) or rounded value ([**IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)).</span></span> <span data-ttu-id="84815-110">Per identificare le variabili passate ai gestori delle modifiche variabili, un'applicazione può applicare tag alle variabili usando il metodo [**IUIAnimationVariable:: SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) .</span><span class="sxs-lookup"><span data-stu-id="84815-110">To identify the variables passed to variable change handlers, an application can apply tags to variables using the [**IUIAnimationVariable::SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) method.</span></span> <span data-ttu-id="84815-111">Si tratta \* di coppie di oggetti (IUnknown), Integer interpretate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="84815-111">These are object (IUnknown\*), integer pairs that are interpreted by the application.</span></span>

## <a name="example-code"></a><span data-ttu-id="84815-112">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="84815-112">Example Code</span></span>

<span data-ttu-id="84815-113">Il codice di esempio seguente viene tratto da thumbnail. cpp nel [layout di griglia](/windows/desktop/UIAnimation/grid-layout-sample)di esempio dell'animazione Windows; vedere il metodo CMainWindow:: Render.</span><span class="sxs-lookup"><span data-stu-id="84815-113">The following example code is taken from Thumbnail.cpp in the Windows Animation sample [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::Render method.</span></span> <span data-ttu-id="84815-114">Usa il metodo [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) per leggere i valori come valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="84815-114">It uses the [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) method to read the values as floating-point values.</span></span>


```C++
// Get the x-coordinate and y-coordinate animation variable values

DOUBLE x=0;
hr = m_pAnimationVariableX->GetValue(&x);
if (SUCCEEDED(hr))
{
    DOUBLE y=0;
    hr = m_pAnimationVariableY->GetValue(&y);
    if (SUCCEEDED(hr))
    {
        // Draw the object

        ...

    }
}
```



<span data-ttu-id="84815-115">Il codice di esempio seguente viene tratto da MainWindow. cpp nell' [animazione basata sul timer](timer-driven-animation-sample.md)di esempio di Windows Animation; vedere il metodo CMainWindow::D rawBackground.</span><span class="sxs-lookup"><span data-stu-id="84815-115">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::DrawBackground method.</span></span> <span data-ttu-id="84815-116">Usa il metodo [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) per leggere i valori come valori integer.</span><span class="sxs-lookup"><span data-stu-id="84815-116">It uses the [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to read the values as integer values.</span></span>


```C++
// Get the RGB animation variable values

INT32 red;
HRESULT hr = m_pAnimationVariableRed->GetIntegerValue(
    &red
    );
if (SUCCEEDED(hr))
{
    INT32 green;
    hr = m_pAnimationVariableGreen->GetIntegerValue(
        &green
        );
    if (SUCCEEDED(hr))
    {
        INT32 blue;
        hr = m_pAnimationVariableBlue->GetIntegerValue(
            &blue
            );
        if (SUCCEEDED(hr))
        {
            // Set the RGB of the background brush to the new animated value

            ...
                
            // Paint the background

            ...

        }
    }

    ...

}
```



## <a name="previous-step"></a><span data-ttu-id="84815-117">Passaggio precedente</span><span class="sxs-lookup"><span data-stu-id="84815-117">Previous Step</span></span>

<span data-ttu-id="84815-118">Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [aggiornare gestione animazioni e creare frame](introducing-windows-animation-manager.md).</span><span class="sxs-lookup"><span data-stu-id="84815-118">Before starting this step, you should have completed this step: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="84815-119">passaggio successivo</span><span class="sxs-lookup"><span data-stu-id="84815-119">Next Step</span></span>

<span data-ttu-id="84815-120">Al termine di questo passaggio, il passaggio successivo è: [creare uno storyboard e aggiungere transizioni](updating---timer-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="84815-120">After completing this step, the next step is: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84815-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84815-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84815-122">**IUIAnimationVariable:: GetIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="84815-122">**IUIAnimationVariable::GetIntegerValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[<span data-ttu-id="84815-123">**IUIAnimationVariable:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="84815-123">**IUIAnimationVariable::GetValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[<span data-ttu-id="84815-124">Cenni preliminari sull'animazione Windows</span><span class="sxs-lookup"><span data-stu-id="84815-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 