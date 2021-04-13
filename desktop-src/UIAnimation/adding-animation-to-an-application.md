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
# <a name="create-the-main-animation-objects"></a><span data-ttu-id="e0783-106">Creare gli oggetti animazione principali</span><span class="sxs-lookup"><span data-stu-id="e0783-106">Create the Main Animation Objects</span></span>

<span data-ttu-id="e0783-107">Per utilizzare l'animazione Windows nell'applicazione, il primo passaggio consiste nel creare un piccolo set di oggetti animazione principali.</span><span class="sxs-lookup"><span data-stu-id="e0783-107">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span>

## <a name="overview"></a><span data-ttu-id="e0783-108">Panoramica</span><span class="sxs-lookup"><span data-stu-id="e0783-108">Overview</span></span>

<span data-ttu-id="e0783-109">Utilizzare la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare gli oggetti gestione animazioni, timer animazione e libreria di transizione.</span><span class="sxs-lookup"><span data-stu-id="e0783-109">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create the animation manager, animation timer, and transition library objects.</span></span>

<span data-ttu-id="e0783-110">Questi oggetti saranno necessari per creare e visualizzare le animazioni, quindi in genere non devono essere rilasciati fino a quando l'applicazione non viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="e0783-110">These objects will be needed to create and display animations, so they usually should not be released until the application is shutting down.</span></span> <span data-ttu-id="e0783-111">Se non è possibile che eventuali callback registrati abbiano creato un ciclo di riferimento, il rilascio degli oggetti è sufficiente per una pulizia corretta.</span><span class="sxs-lookup"><span data-stu-id="e0783-111">If there is no chance that any registered callbacks could have created a reference cycle, releasing the objects is sufficient for a proper cleanup.</span></span> <span data-ttu-id="e0783-112">In caso contrario, l'applicazione può essere pulita cancellando i callback (passando **null** al posto di ogni) o chiamando il metodo [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) del gestore animazione.</span><span class="sxs-lookup"><span data-stu-id="e0783-112">Otherwise, the application can clean up by clearing the callbacks (passing **NULL** in the place of each) or by calling the animation manager's [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method.</span></span>

## <a name="example-code"></a><span data-ttu-id="e0783-113">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="e0783-113">Example Code</span></span>

<span data-ttu-id="e0783-114">Il codice di esempio seguente viene tratto da MainWindow. cpp negli esempi di animazione Windows; vedere il metodo CMainWindow:: InitializeAnimation.</span><span class="sxs-lookup"><span data-stu-id="e0783-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples; see the CMainWindow::InitializeAnimation method.</span></span>


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



<span data-ttu-id="e0783-115">Si notino le seguenti definizioni da MainWindow. h.</span><span class="sxs-lookup"><span data-stu-id="e0783-115">Note the following definitions from MainWindow.h.</span></span>


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



## <a name="next-step"></a><span data-ttu-id="e0783-116">passaggio successivo</span><span class="sxs-lookup"><span data-stu-id="e0783-116">Next Step</span></span>

<span data-ttu-id="e0783-117">Al termine di questo passaggio, il passaggio successivo è: [Create Animation Variables](create-animation-variables.md).</span><span class="sxs-lookup"><span data-stu-id="e0783-117">After completing this step, the next step is: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0783-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0783-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0783-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="e0783-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="e0783-120">**IUIAnimationManager**</span><span class="sxs-lookup"><span data-stu-id="e0783-120">**IUIAnimationManager**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[<span data-ttu-id="e0783-121">**IUIAnimationTimer**</span><span class="sxs-lookup"><span data-stu-id="e0783-121">**IUIAnimationTimer**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[<span data-ttu-id="e0783-122">**IUIAnimationTransitionLibrary**</span><span class="sxs-lookup"><span data-stu-id="e0783-122">**IUIAnimationTransitionLibrary**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[<span data-ttu-id="e0783-123">Cenni preliminari sull'animazione Windows</span><span class="sxs-lookup"><span data-stu-id="e0783-123">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 