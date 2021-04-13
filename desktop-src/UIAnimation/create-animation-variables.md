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
# <a name="create-animation-variables"></a>Creare variabili di animazione

Un'applicazione deve creare una variabile di animazione per ogni caratteristica visiva che deve essere animata usando l'animazione di Windows.

## <a name="overview"></a>Panoramica

Le variabili di animazione vengono create usando Gestione animazioni e l'applicazione deve mantenere un riferimento a ogni per tutto il tempo necessario. In genere, l'applicazione creerà ogni variabile di animazione allo stesso tempo dell'oggetto visivo a cui viene animato.

Quando viene creata una variabile di animazione, è necessario specificare il valore iniziale. Successivamente, il suo valore può essere modificato solo tramite la pianificazione degli storyboard che lo animano.

Le variabili di animazione vengono passate come parametri quando vengono costruiti gli storyboard, quindi l'applicazione non deve rilasciarle fino a quando non è più necessario animare le caratteristiche visive che rappresentano, in genere quando gli oggetti visivi associati stanno per essere eliminati.

## <a name="example-code"></a>Codice di esempio

-   [Animazione di colori](#animating-colors)
-   [Animazione delle coordinate x e y](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a>Animazione di colori

Il codice di esempio seguente viene tratto da MainWindow. cpp nell'animazione Windows esempi di animazione basata su [applicazioni](application-driven-animation-sample.md) e [animazione basata su timer](timer-driven-animation-sample.md). Nell'esempio, tre variabili di animazione vengono create usando [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) per rappresentare i colori di sfondo. Il codice usa anche i metodi [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) e [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) per controllare il valore della variabile di animazione.


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



Si notino le seguenti definizioni da MainWindow. h.


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



### <a name="animating-x-and-y-coordinates"></a>Animazione delle coordinate x e y

Il codice di esempio seguente viene tratto da thumbnail. cpp nell'esempio di [layout della griglia](/windows/desktop/UIAnimation/grid-layout-sample)di animazione Windows; vedere il metodo CMainWindow:: CreateAnimationVariables. Vengono create due variabili di animazione per rappresentare le coordinate X e Y di ciascun oggetto.


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



Si notino le seguenti definizioni di thumbnail. h.


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



Le variabili di animazione sono numeri a virgola mobile, ma anche i relativi valori possono essere recuperati come numeri interi. Per impostazione predefinita, ogni valore verrà arrotondato al numero intero più vicino, ma è possibile eseguire l'override della modalità di arrotondamento utilizzata per una variabile. Il codice di esempio seguente usa il metodo [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) per specificare che i valori devono essere sempre arrotondati per difetto.


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



## <a name="previous-step"></a>Passaggio precedente

Prima di iniziare questo passaggio, è necessario aver completato questo passaggio: [creare gli oggetti di animazione principali](adding-animation-to-an-application.md).

## <a name="next-step"></a>passaggio successivo

Al termine di questo passaggio, il passaggio successivo è: [aggiornare gestione animazioni e creare frame](introducing-windows-animation-manager.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IUIAnimationManager:: CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[**IUIAnimationVariable:: SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[**IUIAnimationVariable:: SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[**IUIAnimationVariable:: SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[Cenni preliminari sull'animazione Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 