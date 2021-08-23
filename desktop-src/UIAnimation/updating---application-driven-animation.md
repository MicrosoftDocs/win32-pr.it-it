---
title: Leggere i valori delle variabili di animazione
description: Ogni volta che l'applicazione disegna, deve leggere i valori correnti delle variabili di animazione che rappresentano le caratteristiche visive da animare.
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- variabili di animazione Windows Animation , lettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2cc164091be9ecca292e26ab1247ba18c61d89f11dad8fc2530a3e45ca7629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058168"
---
# <a name="read-the-animation-variable-values"></a>Leggere i valori delle variabili di animazione

Ogni volta che l'applicazione disegna, deve leggere i valori correnti delle variabili di animazione che rappresentano le caratteristiche visive da animare.

## <a name="overview"></a>Panoramica

Quando si disegna un frame, un'applicazione può usare il metodo [**IUIAnimationVariable::GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) o [**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) per richiedere i valori di tutte le variabili di animazione che influiranno sugli oggetti visivi all'interno del frame. È possibile ritagliare una variabile di animazione in un intervallo di valori ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) e [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) e richiedere che il relativo valore sia arrotondato a un numero intero usando uno schema di arrotondamento specificato ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).

Invece di leggere i valori di tutte le variabili per ogni frame, Un'applicazione può usare il metodo [**IUIAnimationVariable::SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) o [**IUIAnimationVariable::SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) per registrare uno o più gestori delle modifiche delle variabili per ricevere notifiche solo quando viene apportata una modifica al valore delle variabili ([**IUIAnimationVariableChangeHandler::OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) o un valore arrotondato ([**IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged).**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged) Per identificare le variabili passate ai gestori delle modifiche delle variabili, un'applicazione può applicare tag alle variabili usando il [**metodo IUIAnimationVariable::SetTag.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) Si tratta di coppie di oggetti (IUnknown), \* intere interpretate dall'applicazione.

## <a name="example-code"></a>Codice di esempio

Il codice di esempio seguente è tratto da Thumbnail.cpp nell'esempio di animazione Windows [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample). vedere il metodo CMainWindow::Render. Usa il [**metodo GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) per leggere i valori come valori a virgola mobile.


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



Il codice di esempio seguente è tratto da MainWindow.cpp nell'esempio di animazione Windows [Animazione](timer-driven-animation-sample.md)basata su timer ; vedere il metodo CMainWindow::D rawBackground. Usa il [**metodo GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) per leggere i valori come valori interi.


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

Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [Aggiornare Gestione animazioni e Disegnare fotogrammi](introducing-windows-animation-manager.md).

## <a name="next-step"></a>passaggio successivo

Dopo aver completato questo passaggio, il passaggio successivo è: [Creare uno storyboard e aggiungere transizioni](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[**IUIAnimationVariable::GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[Windows Panoramica dell'animazione](scenic-animation-api-overview.md)
</dt> </dl>

 

 