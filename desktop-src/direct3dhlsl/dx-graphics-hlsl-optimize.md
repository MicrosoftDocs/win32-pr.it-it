---
title: Ottimizzazione degli shader HLSL
description: Questa sezione descrive le strategie per utilizzo generico che è possibile usare per ottimizzare gli shader. È possibile applicare queste strategie agli shader scritti in qualsiasi linguaggio, in qualsiasi piattaforma.
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
ms.openlocfilehash: 9bc707f88fcc731146fcd3a5bbca641e6f0515a728b07af0863894d249c16a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726141"
---
# <a name="optimizing-hlsl-shaders"></a>Ottimizzazione degli shader HLSL

Questa sezione descrive le strategie per utilizzo generico che è possibile usare per ottimizzare gli shader. È possibile applicare queste strategie agli shader scritti in qualsiasi linguaggio, in qualsiasi piattaforma.

-   [Sapere dove eseguire i calcoli dello shader](#know-where-to-perform-shader-calculations)
-   [Ignora istruzioni non necessarie](#skip-unnecessary-instructions)
-   [Creare un pacchetto di variabili e interpolanti](#pack-variables-and-interpolants)
-   [Ridurre la complessità degli shader](#reduce-shader-complexity)
-   [Argomenti correlati](#related-topics)
-   [Argomenti correlati](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a>Sapere dove eseguire i calcoli dello shader

I vertex shader eseguono operazioni che includono il recupero dei vertici e l'esecuzione della trasformazione della matrice dei dati dei vertici. In genere, i vertex shader vengono eseguiti una volta per vertice.

I pixel shader eseguono operazioni che includono il recupero dei dati della trama e l'esecuzione di calcoli di illuminazione. In genere, i pixel shader vengono eseguiti una volta per pixel per una determinata parte della geometria.

In genere, i pixel superano il numero di vertici in una scena, quindi i pixel shader vengono eseguiti più spesso dei vertex shader.

Quando si progettano algoritmi shader, tenere presente quanto segue:

-   Eseguire calcoli sul vertex shader, se possibile. Un calcolo eseguito su un pixel shader è molto più costoso di un calcolo eseguito su un vertex shader.
-   Prendere in considerazione l'uso di calcoli per vertice per migliorare le prestazioni in situazioni come mesh ad alta densità. Per mesh dense, i calcoli per vertice possono produrre risultati visivamente non distinguibili dai risultati prodotti con calcoli per pixel.

## <a name="skip-unnecessary-instructions"></a>Ignora istruzioni non necessarie

In HLSL la diramazione dinamica consente di limitare il numero di istruzioni eseguite. La diramazione dinamica consente quindi di velocizzare il tempo di esecuzione dello shader. Se la geometria o i pixel non vengono visualizzati, usare la diramazione dinamica per uscire dallo shader o per limitare le istruzioni. Ad esempio, se un pixel non è acceso, non ha senso eseguire l'algoritmo di illuminazione.

La tabella seguente elenca alcuni casi in cui è possibile testare le condizioni nello shader e usare la diramazione dinamica per ignorare le istruzioni non necessarie. Tabella non completa. Piuttosto, ha lo scopo di offrire idee per ottimizzare il codice.



| Condizione da controllare                                    | Risposta nello shader       |
|-------------------------------------------------------|------------------------------|
| Il controllo alfa determina che un pixel non verrà visualizzato. | Ignorare il resto dello shader. |
| Il pixel o la geometria è completamente invasa.                | Ignorare il resto dello shader. |
| I pesi dell'interfaccia sono pari a zero.                                | Skip a skip.                  |
| L'attenuazione della luce è zero.                            | Ignorare l'illuminazione.               |
| Termine lambertiano non positivo.                         | Ignorare l'illuminazione.               |



 

## <a name="pack-variables-and-interpolants"></a>Creare un pacchetto di variabili e interpolanti

Tenere presente lo spazio necessario per i dati dello shader. Consente di creare il maggior numero possibile di informazioni in una variabile o interpolazione. In alcuni casi, le informazioni di due variabili possono essere suddivise nello spazio di memoria di una singola variabile.

## <a name="reduce-shader-complexity"></a>Ridurre la complessità degli shader

Mantenere gli shader piccoli e semplici. In generale, gli shader con meno istruzioni vengono eseguiti più rapidamente rispetto agli shader con più istruzioni. È anche più semplice eseguire il debug e ottimizzare shader più piccoli e meno complessi.

## <a name="related-topics"></a>Argomenti correlati

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




