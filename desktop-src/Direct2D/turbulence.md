---
title: Effetto di turbolenza
description: Usare l'effetto di turbolenza per generare una bitmap basata sulla funzione di disturbo Perlin.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- effetto di turbolenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f2aa58be48c759956fe3522812d7ad6c3e9989
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468598"
---
# <a name="turbulence-effect"></a>Effetto di turbolenza

Usare l'effetto di turbolenza per generare una bitmap basata sulla funzione di disturbo Perlin.

L'effetto di turbolenza non ha un'immagine di input.

Il CLSID per questo effetto è CLSID \_ D2D1Turbulence.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Modalità rumore](#noise-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

![Screenshot di esempio dell'effetto che mostra l'output dell'effetto di turbolenza.](images/32-turbulence.png)

L'effetto Turbolenza calcola la somma di uno o più ottave della funzione di disturbo Perlin. Il disturbo perlin è una funzione pseudocasica il cui valore dipende dalla frequenza, dalla posizione e dal valore di seeding. L'effetto genera i valori RGBA usando una di queste equazioni.

Se si seleziona la modalità rumore D2D1 \_ TURBULENCE \_ NOISE \_ FRACTAL \_ SUM, l'effetto usa questa equazione.

![Screenshot che mostra la funzione di turbolenza usata per generare una bitmap.](images/turbulence-equation1.png)

Se si seleziona la modalità rumore D2D1 \_ TURBULENCE \_ NOISE \_ TURBULENCE , l'effetto usa questa equazione.

![Funzione di turbolenza usata per generare una bitmap.](images/turbulence-equation2.png)

> [!Note]  
> La `PerlinNoise` funzione ha un intervallo di \[ -1, 1 \] .

 

Questo effetto restituisce i valori in pixel in valori alfa premoltimulti.

## <a name="effect-properties"></a>Proprietà degli effetti




| Enumerazione del nome visualizzato e dell'indice | Descrizione | 
|------------------------------------|-------------|
| Offset<br /> D2D1_TURBULENCE_PROP_OFFSET<br /> | Coordinate in cui viene generato l'output di turbolenza.<br /> L'algoritmo usato per generare il rumore di Perlin dipende dalla posizione, quindi un offset diverso genera un output diverso. Questa proprietà non è delimitata e le unità vengono specificate in DIP <br /><blockquote>[!Note]<br />L'offset non ha lo stesso effetto di una traslazione perché l'output della funzione noise è infinito e la funzione va a capo intorno al riquadro.</blockquote><br /> Il tipo è D2D1_VECTOR_2F.<br /> Il valore predefinito è {0.0f, 0.0f}.<br /> | 
| Dimensione<br /> D2D1_TURBULENCE_PROP_SIZE<br /> | Dimensioni dell'output di turbolenza.<br /> Questa proprietà non è delimitata e le unità vengono specificate in DIP <br /><br /> Il tipo è D2D1_VECTOR_2F.<br /> Il valore predefinito è {0.0f, 0.0f}.<br /> | 
| BaseFrequency<br /> D2D1_TURBULENCE_PROP_BASE_FREQUENCY<br /> | Frequenze di base nella direzione X e Y. Questa proprietà è di tipo float e deve essere maggiore di 0. Le unità sono specificate in 1/DIP. <br /> Un valore pari a 1 (1/DIP) per la frequenza di base fa in modo che il disturbo Perlin completa un intero ciclo tra due pixel. La facilità di interpolazione per questi pixel comporta pixel completamente casuali, poiché non esiste alcuna correlazione tra i pixel.<br /> Il valore 0,1(1/DIP) per la frequenza di base, la funzione di disturbo Perlin si ripete ogni 10 DIP. Ciò comporta la correlazione tra i pixel e l'effetto di turbolenza tipico è visibile.<br /> Il tipo è D2D1_VECTOR_2F.<br /> Il valore predefinito è {0,01f, 0,01f}.<br /> | 
| NumOctaves<br /> D2D1_TURBULENCE_PROP_NUM_OCTAVES<br /> | Numero di ottetti per la funzione noise. Questa proprietà è un UINT32 e deve essere maggiore di 0.<br /> Il tipo è UINT32.<br /> Il valore predefinito è 1.<br /> | 
| Seed<br /> D2D1_TURBULENCE_PROP_SEED<br /> | Valore di seed per lo pseudo-generatore casuale. Questa proprietà non è associata.<br /> Il tipo è UINT32.<br /> Il valore predefinito è 0.<br /> | 
| Rumore<br /> D2D1_TURBULENCE_PROP_NOISE<br /> | Modalità di disturbo di turbolenza. Questa proprietà può essere una <em>somma frattale</em> o <em>una turbolenza.</em> Indica se generare una bitmap in base al rumore frattale o alla funzione Turbulence. Per <a href="#noise-modes">altre informazioni, vedi</a> Modalità rumore. <br /> Il tipo è D2D1_TURBULENCE_NOISE.<br /> Il valore predefinito è D2D1_TURBULENCE_NOISE_FRACTAL_SUM.<br /> | 
| Uniscibile<br /> D2D1_TURBULENCE_PROP_STITCHABLE<br /> | Attiva o disattiva l'unione. La frequenza di base viene regolata in modo che sia possibile unire la bitmap di output. Ciò è utile se si desidera affiancare più copie dell'output dell'effetto di turbolenza.<ul><li>True La bitmap di output può essere affiancata (usando l'effetto tessera) senza l'aspetto delle sgheghe. La frequenza di base viene regolata in modo che sia possibile unire la bitmap di output.</li><li>False La frequenza di base non viene regolata, quindi se la bitmap è affiancata possono essere visualizzate satinate tra i riquadri.</li></ul><br /> Il tipo è BOOL.<br /> Il valore predefinito è FALSE.<br /> | 




 

## <a name="noise-modes"></a>Modalità rumore



| Enumerazione                           | Descrizione                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| D2D1 \_ TURBULENCE \_ NOISE \_ FRACTAL \_ SUM | Calcola una somma delle ottave, spostando l'intervallo di output da \[ -1, 1 \] a \[ 0, 1 \] . |
| D2D1 \_ TURBOLENZA \_ DEL RUMORE \_   | Calcola una somma del valore assoluto di ogni ottave.                                  |



 

> [!Note]  
> Nessuna delle due modalità contiene un'associazione esplicita dei valori di output.

 

## <a name="output-bitmap"></a>Bitmap di output

Questo effetto genera una bitmap logicamente infinita.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

