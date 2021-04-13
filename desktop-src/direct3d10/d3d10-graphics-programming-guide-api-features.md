---
description: La pipeline grafica Direct3D 10 rappresenta una modifica dell'architettura fondamentale, ricompilata in base all'hardware e al software per potenziare la prossima generazione di giochi e applicazioni multimediali 3D.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: Funzionalità API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab12285509441bb429c78d995e68ed1753ceb5bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225580"
---
# <a name="api-features-direct3d-10"></a>Funzionalità API (Direct3D 10)

La pipeline grafica Direct3D 10 rappresenta una modifica dell'architettura fondamentale, ricompilata in base all'hardware e al software per potenziare la prossima generazione di giochi e applicazioni multimediali 3D. Usa Windows Display Driver Model (WDDM), che consente di migliorare le prestazioni e il comportamento, ad esempio la memoria GPU virtuale.

Gli sviluppatori che hanno familiarità con Direct3D 9 scopriranno una serie di miglioramenti funzionali e miglioramenti delle prestazioni in Direct3D 10, tra cui:

-   Possibilità di elaborare intere primitive nella nuova [fase geometry-shader](/previous-versions//bb205146(v=vs.85)).
-   Possibilità di restituire i dati dei vertici generati dalla pipeline alla memoria usando la [fase di output del flusso](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).
-   Organizzazione dello stato della pipeline in 5 [oggetti di stato](d3d10-graphics-programming-guide-api-features-state-objects.md)non modificabili, consentendo una configurazione rapida della pipeline.
-   Organizzazione di costanti shader in [buffer costanti](d3d10-graphics-programming-guide-resources-types.md), riducendo al minimo l'overhead della larghezza di banda per la fornitura di dati della costante shader.
-   Possibilità di eseguire lo swapping e la configurazione di materiali per primitive usando un geometry shader.
-   Nuovi [tipi di risorse](d3d10-graphics-programming-guide-resources-types.md) , incluse le matrici di trama che possono essere indicizzate da shader, e formati di risorse.
-   Aumento della generalizzazione dell'accesso alle risorse tramite una [vista](d3d10-graphics-programming-guide-resources-access-views.md).
-   I bit di funzionalità hardware legacy sono stati rimossi a favore di un set completo di funzionalità garantite, che sono destinate all'hardware di classe Direct3D 10 (minima).
-   [Runtime sovrapposto](d3d10-graphics-programming-guide-api-features-layers.md) : l'API Direct3D 10 è costruita con i livelli, a partire dalle funzionalità di base e la creazione di funzionalità facoltative e di supporto per gli sviluppatori (debug e così via) nei livelli esterni.
-   Integrazione completa di HLSL: tutti gli shader Direct3D 10 sono scritti in HLSL e implementati con il [nucleo di shader comune](../direct3dhlsl/dx-graphics-hlsl-common-core.md).
-   Aumento del numero di destinazioni di rendering, trame e Sampler. Non esiste neanche un limite di lunghezza dello shader.
-   Operazioni shader Integer e bit per bit.
-   Readback di una superficie di profondità/stencil o una risorsa multicampionata, quando non è più associata come destinazione di rendering.
-   Supporto multicampionato da Alpha a code coverage.

Ci sono altre differenze di comportamento che gli sviluppatori di Direct3D 9 devono conoscere (vedere le [considerazioni su Direct3D 9 in Direct3D 10](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).

Di seguito è riportato un elenco di funzionalità di Direct3D 9 che non sono più supportate o sono state rivedute in Direct3D 10 (vedere [funzionalità deprecate](d3d10-graphics-programming-guide-api-features-deprecated.md)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di programmazione per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
