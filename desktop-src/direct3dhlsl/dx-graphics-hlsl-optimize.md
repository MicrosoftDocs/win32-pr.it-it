---
title: Ottimizzazione degli shader HLSL
description: Questa sezione descrive le strategie generali che è possibile usare per ottimizzare gli shader. È possibile applicare queste strategie agli shader scritti in qualsiasi linguaggio, su qualsiasi piattaforma.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- linguaggio shader di alto livello
- HLSL, prestazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06d3bb806e98e489020aa1755ef2a6c952459d86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045102"
---
# <a name="optimizing-hlsl-shaders"></a>Ottimizzazione degli shader HLSL

Questa sezione descrive le strategie generali che è possibile usare per ottimizzare gli shader. È possibile applicare queste strategie agli shader scritti in qualsiasi linguaggio, su qualsiasi piattaforma.

-   [Informazioni su dove eseguire i calcoli dello shader](#know-where-to-perform-shader-calculations)
-   [Ignora istruzioni non necessarie](#skip-unnecessary-instructions)
-   [Variabili Pack e Interpolants](#pack-variables-and-interpolants)
-   [Ridurre la complessità dello shader](#reduce-shader-complexity)
-   [Argomenti correlati](#related-topics)
-   [Argomenti correlati](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a>Informazioni su dove eseguire i calcoli dello shader

I vertex shader eseguono operazioni che includono il recupero di vertici e l'esecuzione della trasformazione matrice dei dati dei vertici. I vertex shader vengono in genere eseguiti una volta per ogni vertice.

I pixel shader eseguono operazioni che includono il recupero dei dati di trama e l'esecuzione di calcoli di illuminazione. In genere, i pixel shader vengono eseguiti una volta per ogni pixel per una determinata porzione di geometria.

In genere, i pixel superano i vertici in una scena, quindi i pixel shader vengono eseguiti più spesso rispetto ai vertex shader.

Quando si progettano gli algoritmi dello shader, tenere presente quanto segue:

-   Se possibile, eseguire calcoli sul vertex shader. Un calcolo eseguito su un pixel shader è molto più costoso di un calcolo eseguito su un vertex shader.
-   Prendere in considerazione l'uso di calcoli per vertice per migliorare le prestazioni in situazioni come le mesh dense. Per le mesh dense, i calcoli per vertice possono produrre risultati non distinguibili visivamente dai risultati prodotti con calcoli per pixel.

## <a name="skip-unnecessary-instructions"></a>Ignora istruzioni non necessarie

In HLSL, la creazione di rami dinamici consente di limitare il numero di istruzioni eseguite. La creazione di rami dinamici consente pertanto di velocizzare il tempo di esecuzione dello shader. Se la geometria o i pixel non sono visualizzati, utilizzare la diramazione dinamica per uscire dallo shader o per limitare le istruzioni. Se, ad esempio, un pixel non è acceso, non è presente alcun punto nell'esecuzione dell'algoritmo di illuminazione.

Nella tabella seguente sono elencati alcuni casi in cui è possibile testare le condizioni nello shader e utilizzare la diramazione dinamica per ignorare le istruzioni superflue. La tabella non è completa. Piuttosto, è destinato a fornire idee per l'ottimizzazione del codice.



| Condizione da controllare                                    | Risposta nello shader       |
|-------------------------------------------------------|------------------------------|
| Il controllo alfa determina che un pixel non verrà visualizzato. | Ignora il resto dello shader. |
| Il pixel o la geometria è completamente offuscata.                | Ignora il resto dello shader. |
| I pesi dell'interfaccia sono pari a zero.                                | Ignora ossa.                  |
| Attenuazione chiara è pari a zero.                            | Ignora illuminazione.               |
| Termine Lambertian non positivo.                         | Ignora illuminazione.               |



 

## <a name="pack-variables-and-interpolants"></a>Variabili Pack e Interpolants

Tenere presente lo spazio necessario per i dati dello shader. Comprimere la maggior parte delle informazioni in una variabile o interpolabile come possibile. In alcuni casi, le informazioni di due variabili possono essere compresse nello spazio di memoria di una singola variabile.

## <a name="reduce-shader-complexity"></a>Ridurre la complessità dello shader

Mantieni gli shader piccoli e semplici. In generale, gli shader con meno istruzioni vengono eseguiti più rapidamente degli shader con ulteriori istruzioni. È anche più semplice eseguire il debug e ottimizzare gli shader più piccoli e meno complessi.

## <a name="related-topics"></a>Argomenti correlati

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




