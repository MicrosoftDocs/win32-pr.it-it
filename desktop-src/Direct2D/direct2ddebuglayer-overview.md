---
title: Panoramica del livello di debug Direct2D
description: Panoramica del livello di debug Direct2D
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad960c50cd125ec8c335d836949457bb05ef65aba4b2edaff1dfbbd3a9cf6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087771"
---
# <a name="direct2d-debug-layer-overview"></a>Panoramica del livello di debug Direct2D

Il livello di debug Direct2D fornisce messaggi di debug in fase di progettazione per ridurre al minimo gli errori dell'applicazione di runtime. Questa panoramica descrive le nozioni di base del livello di debug Direct2D. Si presuppone che si abbia familiarità con la creazione di applicazioni Direct2D di base.

Questa panoramica contiene le sezioni seguenti.

-   [Informazioni sul livello di debug Direct2D](#what-is-the-direct2d-debug-layer)
-   [Installazione del livello di debug Direct2D](#installing-the-direct2d-debug-layer)
-   [Abilitazione del livello di debug](#enabling-the-debug-layer)
-   [Livelli di debug](#debug-levels)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a>Informazioni sul livello di debug Direct2D

Il livello di debug Direct2D, implementato separatamente da Direct2D nella propria DLL denominata d2d1debug.dll, fornisce messaggi di debug che consentono di usare in modo accurato le funzioni Direct2D. I messaggi di debug spesso derivano da violazioni del contratto API, ad esempio parametri non validi (potrebbero essere correlati a Direct3D), risorse non valide, violazioni del threading e problemi di prestazioni, ad esempio l'uso di un livello quando sarebbe sufficiente un clip. Per specificare la quantità di informazioni tracciate dal livello di debug, è possibile specificare uno dei tre livelli di debug: informazioni, avviso ed errore. e un messaggio di errore di livello attiva il punto di interruzione per facilitare il debug.

## <a name="installing-the-direct2d-debug-layer"></a>Installazione del livello di debug Direct2D

Per istruzioni sull'installazione del livello di debug, vedere [Installazione del livello di debug Direct2D](installing-the-direct2d-debug-layer.md).

## <a name="enabling-the-debug-layer"></a>Abilitazione del livello di debug

Per abilitare il livello di debug nell'applicazione, specificare un valore [**D2D1 \_ DEBUG \_ LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) diverso da **D2D1 \_ DEBUG LEVEL \_ \_ NONE** quando si crea una factory con la [**funzione D2D1CreateFactory.**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)

> [!Note]  
> Se il livello di debug Direct2D è abilitato, l'effetto di gestione dei colori Direct2D (CLSID D2D1ColorManagement) può causare una violazione di accesso quando si imposta un contesto \_ colori. La soluzione alternativa consiste nel disabilitare il livello di debug quando si usa l'effetto di gestione del colore

 

L'abilitazione del livello di debug per una factory abilita anche le informazioni di debug per qualsiasi oggetto creato da tale factory.

L'esempio seguente abilita il livello di debug per una factory quando l'applicazione viene compilata per la configurazione della build DEBUG.


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
> Se non viene specificata alcuna opzione factory o viene specificato un livello di debug "none", il livello di debug non viene richiamato. Il livello di debug non deve mai essere attivo nella versione di rilascio di un'applicazione.

 

La sezione successiva descrive i diversi livelli di debug definiti [**dall'enumerazione D2D1 \_ DEBUG \_ LEVEL.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level)

## <a name="debug-levels"></a>Livelli di debug

L'enumerazione [**D2D1 \_ DEBUG \_ LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) specifica tre livelli di debug: D2D1 \_ DEBUG LEVEL ERROR \_ \_ (error), D2D1 \_ DEBUG LEVEL WARNING (avviso) e \_ \_ D2D1 \_ DEBUG LEVEL INFORMATION \_ \_ (informazioni). Questi livelli vengono interpretati come segue:

-   **Errore:** Direct2D invia messaggi di errore gravi al livello di debug. Ad esempio, l'interruzione di un vincolo di threading genererà un errore grave.

-   **Avviso:** Direct2D invia messaggi di errore e avvisi al livello di debug in modo che sia possibile risolvere uno qualsiasi di questi messaggi.

-   **Informazioni:** Direct2D invia messaggi di errore, avvisi e informazioni di diagnostica aggiuntive al livello di debug. Ad esempio, i messaggi di miglioramento delle prestazioni verranno inviati a questo livello di debug.

Il valore D2D1 DEBUG LEVEL NONE (nessuno) indica che \_ \_ \_ Direct2D non fornisce alcun output di debug.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di debug](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




