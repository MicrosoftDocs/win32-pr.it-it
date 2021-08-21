---
description: La pipeline grafica Direct3D 10 rappresenta una modifica fondamentale dell'architettura, ricompilata da zero nell'hardware e nel software per alimentare la nuova generazione di giochi e applicazioni multimediali 3D.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: Funzionalità API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 416018fcddf2643ba9fbc8e633ec2f636b8158ff329780a55205034e5dbbe240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858661"
---
# <a name="api-features-direct3d-10"></a>Funzionalità API (Direct3D 10)

La pipeline grafica Direct3D 10 rappresenta una modifica fondamentale dell'architettura, ricompilata da zero nell'hardware e nel software per alimentare la nuova generazione di giochi e applicazioni multimediali 3D. Usa il modello WDDM (Windows Display Driver Model), che consente miglioramenti delle prestazioni e del comportamento, ad esempio la memoria GPU virtuale.

Gli sviluppatori che hanno familiarità con Direct3D 9 scopriranno una serie di miglioramenti funzionali e di prestazioni in Direct3D 10, tra cui:

-   Possibilità di elaborare intere primitive nella nuova [fase geometry-shader](/previous-versions//bb205146(v=vs.85)).
-   Possibilità di eseguire l'output in memoria dei dati dei vertici generati dalla pipeline usando la [fase di output di flusso](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).
-   Organizzazione dello stato della pipeline [](d3d10-graphics-programming-guide-api-features-state-objects.md)in 5 oggetti di stato non modificabili, consentendo una configurazione rapida della pipeline.
-   Organizzazione delle costanti shader in [buffer costanti,](d3d10-graphics-programming-guide-resources-types.md)riducendo al minimo il sovraccarico della larghezza di banda per la fornitura di dati costanti dello shader.
-   Possibilità di eseguire lo scambio e la configurazione di materiali per primitiva usando uno shader geometry.
-   Nuovi [tipi di risorse](d3d10-graphics-programming-guide-resources-types.md) (incluse matrici di trame che possono essere indicizzate da shader) e formati di risorse.
-   Maggiore generalizzazione dell'accesso alle risorse tramite una [visualizzazione](d3d10-graphics-programming-guide-resources-access-views.md).
-   I bit di funzionalità hardware legacy (tappi) sono stati rimossi a favore di un set di funzionalità garantite, destinato all'hardware di classe Direct3D 10 (minimo).
-   [Runtime a](d3d10-graphics-programming-guide-api-features-layers.md) più livelli: l'API Direct3D 10 viene costruita con livelli, a partire dalle funzionalità di base nel core e creando funzionalità facoltative e di supporto per gli sviluppatori (debug e così via) nei livelli esterni.
-   Integrazione HLSL completa: tutti gli shader Direct3D 10 vengono scritti in HLSL e implementati con [common-shader core.](../direct3dhlsl/dx-graphics-hlsl-common-core.md)
-   Aumento del numero di destinazioni di rendering, trame e campionatori. Non esiste inoltre alcun limite di lunghezza dello shader.
-   Operazioni shader intere e bit per bit.
-   Readback di una superficie di profondità/stencil o di una risorsa multicampionata, quando non è più associata come destinazione di rendering.
-   Supporto alfa-to-coverage multicampionato.

Esistono altre differenze di comportamento che gli sviluppatori Direct3D 9 devono tenere presenti (vedere Considerazioni da [Direct3D 9 a Direct3D 10).](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)

Di seguito è riportato un elenco delle funzionalità di Direct3D 9 che non sono più supportate o sono state modificate in Direct3D 10 (vedere [Funzionalità deprecate](d3d10-graphics-programming-guide-api-features-deprecated.md)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
