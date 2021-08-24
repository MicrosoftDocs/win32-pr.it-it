---
description: Direct3D 9 supporta punti, linee, triangoli e primitive della griglia.
ms.assetid: 474e8bee-336d-491f-afa0-f0186a8d19c7
title: Higher-Order primitive (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36ee67cfe4d4a802303091288f3906778e6cb3cdc1ad811602a80bc161d0a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122122"
---
# <a name="higher-order-primitives-direct3d-9"></a>Higher-Order primitive (Direct3D 9)

Direct3D 9 supporta punti, linee, triangoli e primitive della griglia. Queste sono state estese per supportare l'interpolazione di ordine superiore oltre a quella lineare. Mentre i triangoli e le linee hanno estensione spaziale, fino ad ora sono stati entrambi sottoposti a rendering usando l'interpolazione lineare. In Direct3D 9 Direct3D supporta il rendering di questi tipi primitivi usando un ordine superiore, fino all'interpolazione quintica. Inoltre, è ora supportato un nuovo tipo quad primitivo. È anche possibile eseguire il rendering di questo nuovo tipo con un'interpolazione di ordine superiore. Questa funzionalità è principalmente basata sui requisiti per l'animazione e il rendering dei caratteri. Può essere usato anche per altre superfici, ad esempio terreno o acqua.

Le primitive di ordine superiore supportano l'interpolazione di ordine superiore quando vengono trasmesse all'API come elenchi, strisce, ventole o mesh indicizzate. Questa operazione viene ottenuta usando informazioni aggiuntive codificate nei vertici stessi. Ad esempio, i vettori normali possono essere usati per definire piani tangenti ai vertici per abilitare l'interpolazione cubica. La maggior parte delle implementazioni supporta l'interpolazione di ordine superiore tramite l'interpolazione a tessellazione in triangoli planari. Il passaggio a tessellazione viene applicato logicamente prima della fase vertex shader. Poiché l'API vertex shader non impone la semantica sui dati di input, viene fornito un meccanismo speciale per identificare il componente del flusso di vertici che rappresenta la posizione e, facoltativamente, il vettore normale. Tutti gli altri componenti vengono interpolati di conseguenza.

In questa sezione vengono presentate primitive di ordine superiore e viene illustrato come possono essere usate nelle applicazioni. Le informazioni sono suddivise negli argomenti seguenti.

-   [Miglioramento della qualità tramite il miglioramento della risoluzione](#improved-quality-through-resolution-enhancement)
-   [Mapping diretto da Spline-Based strumenti](#direct-mapping-from-spline-based-tools)

## <a name="improved-quality-through-resolution-enhancement"></a>Miglioramento della qualità tramite il miglioramento della risoluzione

Le primitive correnti non sono ideali per la rappresentazione di superfici lisce. I metodi di interpolazione di ordine superiore, ad esempio i polinomi cubici, consentono calcoli più accurati nel rendering di forme curve. Ciò garantisce maggiore realisticità riducendo o eliminando artefatti di viso visibili sui bordi della superficie o sull'illuminazione della superficie speculare. Inoltre, quando si verifica la tessellazione sul chip, i triangoli a tessellati non influiscono sulla larghezza di banda del bus. In molti casi, una piccola quantità di tassellamento può offrire miglioramenti nella qualità delle immagini con un impatto minimo sulle prestazioni.

Direct3D 9 offre un modo semplice per applicare il miglioramento della risoluzione al contenuto creato da strumenti e pipeline d'arte orientati ai poligoni esistenti. L'applicazione deve fornire solo un livello desiderato di tessellazione e trasmettere i dati usando la sintassi del triangolo standard che include vettori normali.

## <a name="direct-mapping-from-spline-based-tools"></a>Mapping diretto da Spline-Based Tools

Molti attuali strumenti di creazione supportano primitive di ordine superiore per consentire operazioni di modellazione più potenti rispetto a quelle comunemente fornite per le mesh a triangolo planare. Se usati in modo efficiente, in modo che il numero di patch generate sia ragionevole, tali strumenti possono produrre contenuto di cui l'API può eseguire il rendering direttamente. Per soddisfare questo requisito, è stato aggiunto un nuovo punto di ingresso che interpreta il flusso di dati dei vertici in ingresso come una matrice 2D di punti di controllo e lo antepose alla risoluzione desiderata.

-   [Uso Higher-Order primitive (Direct3D 9)](using-higher-order-primitives.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline dei vertici](vertex-pipeline.md)
</dt> </dl>

 

 



