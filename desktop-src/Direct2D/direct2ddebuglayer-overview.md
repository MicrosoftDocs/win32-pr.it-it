---
title: Panoramica del livello di debug Direct2D
description: Panoramica del livello di debug Direct2D
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833174e0d18b11e2384d838930d5508601cfceaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099989"
---
# <a name="direct2d-debug-layer-overview"></a><span data-ttu-id="a0a95-103">Panoramica del livello di debug Direct2D</span><span class="sxs-lookup"><span data-stu-id="a0a95-103">Direct2D Debug Layer Overview</span></span>

<span data-ttu-id="a0a95-104">Il livello di debug Direct2D fornisce messaggi di debug in fase di progettazione per ridurre al minimo gli errori dell'applicazione di runtime.</span><span class="sxs-lookup"><span data-stu-id="a0a95-104">The Direct2D debug layer provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="a0a95-105">Questa panoramica descrive le nozioni di base del livello di debug Direct2D.</span><span class="sxs-lookup"><span data-stu-id="a0a95-105">This overview describes the basics of the Direct2D debug layer.</span></span> <span data-ttu-id="a0a95-106">Si presuppone che si abbia familiarità con la creazione di applicazioni Direct2D di base.</span><span class="sxs-lookup"><span data-stu-id="a0a95-106">It assumes that you are familiar with creating basic Direct2D applications.</span></span>

<span data-ttu-id="a0a95-107">Questa panoramica contiene le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="a0a95-107">This overview contains the following sections.</span></span>

-   [<span data-ttu-id="a0a95-108">Informazioni sul livello di debug Direct2D</span><span class="sxs-lookup"><span data-stu-id="a0a95-108">What Is the Direct2D Debug Layer</span></span>](#what-is-the-direct2d-debug-layer)
-   [<span data-ttu-id="a0a95-109">Installazione del livello di debug Direct2D</span><span class="sxs-lookup"><span data-stu-id="a0a95-109">Installing the Direct2D Debug Layer</span></span>](#installing-the-direct2d-debug-layer)
-   [<span data-ttu-id="a0a95-110">Abilitazione del livello di debug</span><span class="sxs-lookup"><span data-stu-id="a0a95-110">Enabling the Debug Layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="a0a95-111">Livelli di debug</span><span class="sxs-lookup"><span data-stu-id="a0a95-111">Debug Levels</span></span>](#debug-levels)
-   [<span data-ttu-id="a0a95-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0a95-112">Related topics</span></span>](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a><span data-ttu-id="a0a95-113">Informazioni sul livello di debug Direct2D</span><span class="sxs-lookup"><span data-stu-id="a0a95-113">What Is the Direct2D Debug Layer</span></span>

<span data-ttu-id="a0a95-114">Il livello di debug Direct2D, implementato separatamente da Direct2D nella propria DLL denominata d2d1debug.dll, fornisce messaggi di debug che consentono di usare in modo accurato le funzioni Direct2D.</span><span class="sxs-lookup"><span data-stu-id="a0a95-114">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides debug messages to enable you to accurately use Direct2D functions.</span></span> <span data-ttu-id="a0a95-115">I messaggi di debug spesso derivano da violazioni del contratto API, ad esempio parametri non validi (potrebbero essere correlati a Direct3D), risorse non valide, violazioni di threading e problemi di prestazioni, ad esempio l'uso di un livello quando una clip è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="a0a95-115">The debug messages often result from API contract violations such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and performance issues such as using a layer when a clip would suffice.</span></span> <span data-ttu-id="a0a95-116">Per specificare la quantità di informazioni tracciate dal livello di debug, è possibile specificare uno dei tre livelli di debug: informazioni, avviso ed errore. e un messaggio di errore di livello attiva il punto di interruzione per facilitare il debug.</span><span class="sxs-lookup"><span data-stu-id="a0a95-116">To specify how much information is traced by the debug layer, you can specify one of the three debug levels: information, warning, and error; and a message of level error triggers the breakpoint to help you debug.</span></span>

## <a name="installing-the-direct2d-debug-layer"></a><span data-ttu-id="a0a95-117">Installazione del livello di debug Direct2D</span><span class="sxs-lookup"><span data-stu-id="a0a95-117">Installing the Direct2D Debug Layer</span></span>

<span data-ttu-id="a0a95-118">Per istruzioni sull'installazione del livello di debug, vedere [Installazione del livello di debug Direct2D.](installing-the-direct2d-debug-layer.md)</span><span class="sxs-lookup"><span data-stu-id="a0a95-118">For instructions on installing the debug layer, see [Installing the Direct2D Debug Layer](installing-the-direct2d-debug-layer.md).</span></span>

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="a0a95-119">Abilitazione del livello di debug</span><span class="sxs-lookup"><span data-stu-id="a0a95-119">Enabling the Debug Layer</span></span>

<span data-ttu-id="a0a95-120">Per abilitare il livello di debug nell'applicazione, specificare un valore [**D2D1 \_ DEBUG \_ LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) diverso da **D2D1 \_ DEBUG LEVEL \_ \_ NONE** quando si crea una factory con la funzione [**D2D1CreateFactory.**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)</span><span class="sxs-lookup"><span data-stu-id="a0a95-120">To enable the debug layer in your application, specify a [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) value other than **D2D1\_DEBUG\_LEVEL\_NONE** when you create a factory with the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>

> [!Note]  
> <span data-ttu-id="a0a95-121">Se il livello di debug Direct2D è abilitato, l'effetto di gestione dei colori Direct2D (CLSID D2D1ColorManagement) può causare una violazione di accesso quando si imposta un contesto \_ colore.</span><span class="sxs-lookup"><span data-stu-id="a0a95-121">If the Direct2D debug layer is enabled, the Direct2D color management effect (CLSID\_D2D1ColorManagement) may cause an access violation when setting a color context.</span></span> <span data-ttu-id="a0a95-122">La soluzione alternativa consiste nel disabilitare il livello di debug quando si usa l'effetto di gestione del colore</span><span class="sxs-lookup"><span data-stu-id="a0a95-122">The workaround is to disable the debug layer when using the color management effect</span></span>

 

<span data-ttu-id="a0a95-123">L'abilitazione del livello di debug per una factory abilita anche le informazioni di debug per qualsiasi oggetto creato da tale factory.</span><span class="sxs-lookup"><span data-stu-id="a0a95-123">Enabling the debug layer for a factory also enables debugging information for any object created by that factory.</span></span>

<span data-ttu-id="a0a95-124">L'esempio seguente abilita il livello di debug per una factory quando l'applicazione viene compilata per la configurazione della build DEBUG.</span><span class="sxs-lookup"><span data-stu-id="a0a95-124">The following example enables the debug layer for a factory when the application is compiled for the DEBUG build configuration.</span></span>


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif
```



> [!Note]  
> <span data-ttu-id="a0a95-125">Se non viene specificata alcuna opzione factory o viene specificato un livello di debug "none", il livello di debug non viene richiamato.</span><span class="sxs-lookup"><span data-stu-id="a0a95-125">If no factory options are specified or a debug level of "none" is specified, the debug layer is not invoked.</span></span> <span data-ttu-id="a0a95-126">Il livello di debug non deve mai essere attivo nella versione di rilascio di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a0a95-126">The debug layer should never be active in the release version of an application.</span></span>

 

<span data-ttu-id="a0a95-127">La sezione successiva descrive i diversi livelli di debug definiti [**dall'enumerazione D2D1 \_ DEBUG \_ LEVEL.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level)</span><span class="sxs-lookup"><span data-stu-id="a0a95-127">The next section describes the different debug levels defined by the [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration.</span></span>

## <a name="debug-levels"></a><span data-ttu-id="a0a95-128">Livelli di debug</span><span class="sxs-lookup"><span data-stu-id="a0a95-128">Debug Levels</span></span>

<span data-ttu-id="a0a95-129">L'enumerazione [**D2D1 \_ DEBUG \_ LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) specifica tre livelli di debug: D2D1 \_ DEBUG LEVEL ERROR \_ \_ (error), D2D1 \_ DEBUG LEVEL WARNING (avviso) e \_ \_ D2D1 \_ DEBUG LEVEL INFORMATION \_ \_ (informazioni).</span><span class="sxs-lookup"><span data-stu-id="a0a95-129">The [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration specifies three debug levels: D2D1\_DEBUG\_LEVEL\_ERROR (error), D2D1\_DEBUG\_LEVEL\_WARNING (warning), and D2D1\_DEBUG\_LEVEL\_INFORMATION (information).</span></span> <span data-ttu-id="a0a95-130">Questi livelli vengono interpretati come segue:</span><span class="sxs-lookup"><span data-stu-id="a0a95-130">These levels are interpreted as follows:</span></span>

-   <span data-ttu-id="a0a95-131">**Errore:** Direct2D invia messaggi di errore gravi al livello di debug.</span><span class="sxs-lookup"><span data-stu-id="a0a95-131">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="a0a95-132">Ad esempio, l'interruzione di un vincolo di threading genererà un errore grave.</span><span class="sxs-lookup"><span data-stu-id="a0a95-132">For example, breaking a threading constraint will generate a severe error.</span></span>

-   <span data-ttu-id="a0a95-133">**Avviso:** Direct2D invia messaggi di errore e avvisi al livello di debug in modo che sia possibile risolvere uno qualsiasi di questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="a0a95-133">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="a0a95-134">**Informazioni:** Direct2D invia messaggi di errore, avvisi e informazioni di diagnostica aggiuntive al livello di debug.</span><span class="sxs-lookup"><span data-stu-id="a0a95-134">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="a0a95-135">Ad esempio, i messaggi di miglioramento delle prestazioni verranno inviati a questo livello di debug.</span><span class="sxs-lookup"><span data-stu-id="a0a95-135">For example, performance improvement messages will be sent at this debug level.</span></span>

<span data-ttu-id="a0a95-136">Il valore D2D1 DEBUG LEVEL NONE (nessuno) indica che \_ \_ \_ Direct2D non fornisce alcun output di debug.</span><span class="sxs-lookup"><span data-stu-id="a0a95-136">The value D2D1\_DEBUG\_LEVEL\_NONE (none) indicates that Direct2D does not provide any debugging output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0a95-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0a95-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0a95-138">Messaggi di debug</span><span class="sxs-lookup"><span data-stu-id="a0a95-138">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




