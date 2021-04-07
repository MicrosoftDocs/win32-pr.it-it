---
description: Direct3D 9 supporta punti, linee, triangoli e primitive griglia.
ms.assetid: 474e8bee-336d-491f-afa0-f0186a8d19c7
title: Primitive di Higher-Order (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67767dd955fa5c0c5c21315d7c1c510de422870c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745562"
---
# <a name="higher-order-primitives-direct3d-9"></a>Primitive di Higher-Order (Direct3D 9)

Direct3D 9 supporta punti, linee, triangoli e primitive griglia. Questi sono stati estesi per supportare l'interpolazione di ordine superiore oltre lineare. Mentre i triangoli e le linee hanno un'estensione spaziale, fino a questo momento sono stati entrambi sottoposti a rendering usando l'interpolazione lineare. In Direct3D 9, Direct3D supporta il rendering di questi tipi primitivi usando un ordine superiore, fino a quinte, l'interpolazione. Inoltre, è ora supportato un nuovo tipo primitivo quad. Questo nuovo tipo può anche essere sottoposto a rendering con l'interpolazione di ordine superiore. Questa funzionalità è basata principalmente sui requisiti per l'animazione e il rendering dei caratteri. Può essere usato anche per altre superfici, ad esempio il terreno o l'acqua.

Le primitive di ordine superiore supportano l'interpolazione di ordine superiore quando vengono trasmesse all'API come elenchi, strisce, ventilatori o mesh indicizzate. Questa operazione viene eseguita usando informazioni aggiuntive codificate nei vertici stessi. Ad esempio, i vettori normali possono essere usati per definire i piani tangente nei vertici per abilitare l'interpolazione cubica. La maggior parte delle implementazioni supporta l'interpolazione di ordine superiore per mosaico in triangoli planari. Il passaggio a mosaico viene applicato logicamente prima della fase vertex shader. Poiché l'API vertex shader non impone la semantica sui dati di input, viene fornito un meccanismo speciale per identificare il componente del flusso di vertici che rappresenta la posizione e, facoltativamente, il vettore normale. Tutti gli altri componenti vengono interpolati di conseguenza.

Questa sezione introduce primitive di ordine superiore e ne illustra il modo in cui possono essere usati nelle applicazioni. Le informazioni sono suddivise negli argomenti seguenti.

-   [Miglioramento della qualità grazie alla funzionalità di miglioramento della risoluzione](#improved-quality-through-resolution-enhancement)
-   [Mapping diretto da strumenti Spline-Based](#direct-mapping-from-spline-based-tools)

## <a name="improved-quality-through-resolution-enhancement"></a>Miglioramento della qualità grazie alla funzionalità di miglioramento della risoluzione

Le primitive correnti non sono ideali per la rappresentazione di superfici smussate. I metodi di interpolazione di ordine superiore, ad esempio i polinomi cubi, consentono calcoli più accurati nel rendering di forme curve. Ciò garantisce un maggiore realismo riducendo o eliminando gli artefatti facet visibili sui bordi della siluetta o sull'illuminazione della superficie speculare. Inoltre, quando si verifica il mosaico sul chip, i triangoli tassellati non hanno alcun effetto sulla larghezza di banda del bus. In molti casi, una piccola quantità di mosaico può offrire miglioramenti alla qualità dell'immagine con un effetto minimo sulle prestazioni.

Direct3D 9 offre un modo semplice per applicare la funzionalità di miglioramento della risoluzione ai contenuti creati da strumenti e pipeline di arte esistenti orientati ai poligoni. L'applicazione deve fornire solo un livello desiderato di suddivisione a mosaico e trasmettere i dati usando la sintassi del triangolo standard che include i vettori normali.

## <a name="direct-mapping-from-spline-based-tools"></a>Mapping diretto da strumenti Spline-Based

Molti strumenti di creazione correnti supportano primitive di ordine superiore per consentire operazioni di modellazione più potenti rispetto a quelle comunemente fornite per con mesh triangolari planari. Se usato in modo efficiente, in modo che il numero di patch generate sia ragionevole, questi strumenti possono produrre contenuto di cui è possibile eseguire il rendering direttamente dall'API. Per soddisfare questo requisito, è stato aggiunto un nuovo punto di ingresso che interpreta il flusso di dati dei vertici in ingresso come matrice 2D di punti di controllo e tessellates alla risoluzione desiderata.

-   [Uso di Higher-Order primitive (Direct3D 9)](using-higher-order-primitives.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline Vertex](vertex-pipeline.md)
</dt> </dl>

 

 



