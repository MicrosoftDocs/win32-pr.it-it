---
title: Creare gli oggetti animazione principali
description: Per utilizzare l'animazione Windows nell'applicazione, il primo passaggio consiste nel creare un piccolo set di oggetti animazione principali.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- Animazione Windows oggetti Animation Manager, creazione
- animazione oggetti timer animazione Windows, creazione
- oggetti libreria di transizione animazione Windows, creazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ccd1cab32e72bf1382469ada52abeecee47b6a1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399495"
---
# <a name="create-the-main-animation-objects"></a>Creare gli oggetti animazione principali

Per utilizzare l'animazione Windows nell'applicazione, il primo passaggio consiste nel creare un piccolo set di oggetti animazione principali.

## <a name="overview"></a>Panoramica

Utilizzare la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare gli oggetti gestione animazioni, timer animazione e libreria di transizione.

Questi oggetti saranno necessari per creare e visualizzare le animazioni, quindi in genere non devono essere rilasciati fino a quando l'applicazione non viene arrestata. Se non è possibile che eventuali callback registrati abbiano creato un ciclo di riferimento, il rilascio degli oggetti è sufficiente per una pulizia corretta. In caso contrario, l'applicazione può essere pulita cancellando i callback (passando **null** al posto di ogni) o chiamando il metodo [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) del gestore animazione.

## <a name="example-code"></a>Codice di esempio

Il codice di esempio seguente viene tratto da MainWindow. cpp negli esempi di animazione Windows; vedere il metodo CMainWindow:: InitializeAnimation.


```C++
// Create the animation manager object

HRESULT hr = CoCreateInstance(
    CLSID_UIAnimationManager,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&m_pAnimationManager)
    );

if (SUCCEEDED(hr))
{
    // Create the animation timer object

    hr = CoCreateInstance(
        CLSID_UIAnimationTimer,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pAnimationTimer)
        );

    if (SUCCEEDED(hr))
    {
        // Create the transition library object

        hr = CoCreateInstance(
            CLSID_UIAnimationTransitionLibrary,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_PPV_ARGS(&m_pTransitionLibrary)
            );

        ...

    }

    ...

}
```



Si notino le seguenti definizioni da MainWindow. h.


```
class CMainWindow
{

    ...

private:

    // Animation components

    IUIAnimationManager *m_pAnimationManager;
    IUIAnimationTimer *m_pAnimationTimer;
    IUIAnimationTransitionLibrary *m_pTransitionLibrary;

    ...

};
```



## <a name="next-step"></a>passaggio successivo

Al termine di questo passaggio, il passaggio successivo è: [Create Animation Variables](create-animation-variables.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationTimer**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[Cenni preliminari sull'animazione Windows](scenic-animation-api-overview.md)
</dt> </dl>

 

 