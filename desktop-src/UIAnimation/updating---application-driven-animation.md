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
# <a name="read-the-animation-variable-values"></a>Leggere i valori delle variabili di animazione

Ogni volta che l'applicazione disegna, deve leggere i valori correnti delle variabili di animazione che rappresentano le caratteristiche visive da animare.

## <a name="overview"></a>Panoramica

Quando si disegna un frame, un'applicazione può usare il metodo [**IUIAnimationVariable:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) o [**IUIAnimationVariable:: GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) per richiedere i valori di qualsiasi variabile di animazione che influirà sugli oggetti visivi all'interno del frame. È possibile ritagliare una variabile di animazione in un intervallo di valori ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) e [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) e per richiedere che il relativo valore venga arrotondato a un Integer usando uno schema di arrotondamento specificato ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).

Anziché leggere i valori di tutte le variabili per ogni fotogramma, un'applicazione può usare il metodo [**IUIAnimationVariable:: SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) o [**IUIAnimationVariable:: SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) per registrare uno o più gestori di modifiche variabili per ricevere le notifiche solo quando viene apportata una modifica al valore delle variabili ([**IUIAnimationVariableChangeHandler:**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged): OnValueChanged) o al valore arrotondato ([**IUIAnimationVariableIntegerChangeHandler:: OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)). Per identificare le variabili passate ai gestori delle modifiche variabili, un'applicazione può applicare tag alle variabili usando il metodo [**IUIAnimationVariable:: SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) . Si tratta \* di coppie di oggetti (IUnknown), Integer interpretate dall'applicazione.

## <a name="example-code"></a>Codice di esempio

Il codice di esempio seguente viene tratto da thumbnail. cpp nel [layout di griglia](/windows/desktop/UIAnimation/grid-layout-sample)di esempio dell'animazione Windows; vedere il metodo CMainWindow:: Render. Usa il metodo [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) per leggere i valori come valori a virgola mobile.


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



Il codice di esempio seguente viene tratto da MainWindow. cpp nell' [animazione basata sul timer](timer-driven-animation-sample.md)di esempio di Windows Animation; vedere il metodo CMainWindow::D rawBackground. Usa il metodo [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) per leggere i valori come valori integer.


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



## <a name="previous-step"></a>Passaggio precedente

Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [aggiornare gestione animazioni e creare frame](introducing-windows-animation-manager.md).

## <a name="next-step"></a>passaggio successivo

Al termine di questo passaggio, il passaggio successivo è: [creare uno storyboard e aggiungere transizioni](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAnimationVariable:: GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[**IUIAnimationVariable:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[Cenni preliminari sull'animazione Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 