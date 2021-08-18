---
title: Creare gli oggetti di animazione principali
description: Per usare Windows'animazione nell'applicazione, il primo passaggio consiste nel creare un piccolo set di oggetti di animazione principali.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- oggetti di gestione animazione Windows Animation , creazione
- oggetti timer di animazione Windows Animation , creazione
- transition library objects Windows Animation ,creating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3023e5934581850bb6aa21e7d41d92642bb01fadfcf7531fcacabca74b411f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137404"
---
# <a name="create-the-main-animation-objects"></a>Creare gli oggetti di animazione principali

Per usare Windows'animazione nell'applicazione, il primo passaggio consiste nel creare un piccolo set di oggetti di animazione principali.

## <a name="overview"></a>Panoramica

Usare la [**funzione CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare il gestore dell'animazione, il timer di animazione e gli oggetti della libreria di transizione.

Questi oggetti saranno necessari per creare e visualizzare animazioni, quindi in genere non devono essere rilasciati fino a quando l'applicazione non viene arrestata. Se non è possibile che i callback registrati potrebbero aver creato un ciclo di riferimento, il rilascio degli oggetti è sufficiente per una pulizia corretta. In caso contrario, l'applicazione può eseguire la pulizia cancellando i callback (passando **NULL** al posto di ognuno) o chiamando il metodo [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) del gestore dell'animazione.

## <a name="example-code"></a>Codice di esempio

Il codice di esempio seguente è tratto da MainWindow.cpp negli esempi Windows Animation; vedere il metodo CMainWindow::InitializeAnimation.


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



Si notino le definizioni seguenti di MainWindow.h.


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

Dopo aver completato questo passaggio, il passaggio successivo è: [Creare variabili di animazione](create-animation-variables.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Cocreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationTimer**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[**Libreria IUIAnimationTransition**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[Windows Cenni preliminari sull'animazione](scenic-animation-api-overview.md)
</dt> </dl>

 

 