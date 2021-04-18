---
title: Panoramica del livello di debug Direct2D
description: .
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df560595ea0ae6c7a56c3fa568f2f94ae56652ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297833"
---
# <a name="direct2d-debug-layer-overview"></a>Panoramica del livello di debug Direct2D

Il livello di debug Direct2D fornisce messaggi di debug in fase di progettazione per ridurre al minimo l'errore dell'applicazione di Runtime. Questa panoramica descrive le nozioni di base del livello di debug Direct2D. Si presuppone che l'utente abbia familiarità con la creazione di applicazioni Direct2D di base.

Questa panoramica include le sezioni seguenti.

-   [Informazioni sul livello di debug Direct2D](#what-is-the-direct2d-debug-layer)
-   [Installazione del livello di debug Direct2D](#installing-the-direct2d-debug-layer)
-   [Abilitazione del livello di debug](#enabling-the-debug-layer)
-   [Livelli di debug](#debug-levels)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a>Informazioni sul livello di debug Direct2D

Il livello di debug Direct2D, implementato separatamente da Direct2D nella propria DLL denominata d2d1debug.dll, fornisce messaggi di debug che consentono di utilizzare in modo accurato le funzioni Direct2D. I messaggi di debug spesso derivano da violazioni del contratto API, ad esempio parametri non validi (potrebbe essere correlato a Direct3D), risorse non valide, violazioni del threading e problemi di prestazioni, ad esempio l'uso di un livello quando il clip sarebbe sufficiente. Per specificare la quantità di informazioni tracciate dal livello di debug, è possibile specificare uno dei tre livelli di debug, ovvero informazioni, avviso ed errore. un messaggio di errore di livello attiva il punto di interruzione per facilitare il debug.

## <a name="installing-the-direct2d-debug-layer"></a>Installazione del livello di debug Direct2D

Per istruzioni sull'installazione del livello di debug, vedere [installazione del livello di debug Direct2D](installing-the-direct2d-debug-layer.md).

## <a name="enabling-the-debug-layer"></a>Abilitazione del livello di debug

Per abilitare il livello di debug nell'applicazione, specificare un valore del [**\_ \_ livello di debug d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) diverso dal **livello di \_ debug d2d1 \_ \_ None** quando si crea una factory con la funzione [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .

> [!Note]  
> Se il livello di debug Direct2D è abilitato, l'effetto di gestione colori Direct2D (CLSID \_ D2D1ColorManagement) può causare una violazione di accesso quando si imposta un contesto di colore. La soluzione alternativa consiste nel disabilitare il livello di debug quando si usa l'effetto di gestione colori

 

L'abilitazione del livello di debug per una factory Abilita anche le informazioni di debug per qualsiasi oggetto creato da tale factory.

Nell'esempio seguente viene abilitato il livello di debug per una factory quando l'applicazione viene compilata per la configurazione della build di DEBUG.


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
> Se non viene specificata alcuna opzione di Factory o viene specificato un livello di debug "None", il livello di debug non viene richiamato. Il livello di debug non dovrebbe mai essere attivo nella versione di rilascio di un'applicazione.

 

Nella sezione successiva vengono descritti i diversi livelli di debug definiti dall'enumerazione del [**\_ \_ livello di debug d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) .

## <a name="debug-levels"></a>Livelli di debug

L'enumerazione del [**\_ \_ livello di debug d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) specifica tre livelli di debug: \_ errore a livello di debug d2d1 \_ \_ (Error), \_ \_ \_ avviso a livello di debug D2D1 (avviso) e \_ informazioni sul livello di debug d2d1 \_ \_ (informazioni). Questi livelli vengono interpretati nel modo seguente:

-   **Errore:** Direct2D invia messaggi di errore gravi al livello di debug. Se ad esempio si interrompe un vincolo di threading, verrà generato un errore grave.

-   **Avviso:** Direct2D invia messaggi di errore e avvisi al livello di debug in modo che sia possibile risolvere uno di questi messaggi.

-   **Informazioni:** Direct2D invia messaggi di errore, avvisi e informazioni di diagnostica aggiuntive al livello di debug. Ad esempio, i messaggi di miglioramento delle prestazioni verranno inviati a questo livello di debug.

Il valore D2D1 \_ del \_ livello di debug \_ None (nessuno) indica che Direct2D non fornisce alcun output di debug.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di debug](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




