---
title: Effetto turbolenza
description: Usare l'effetto di turbolenza per generare una bitmap basata sulla funzione di disturbo Perlin.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- effetto turbolenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f67f615ec5b68ca285a048b68bc7bc8eab6e24
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104551996"
---
# <a name="turbulence-effect"></a>Effetto turbolenza

Usare l'effetto di turbolenza per generare una bitmap basata sulla funzione di disturbo Perlin.

L'effetto turbolenza non ha un'immagine di input.

Il CLSID per questo effetto è CLSID \_ D2D1Turbulence.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Modalità rumore](#noise-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

![schermata di esempio di effetto che mostra l'output dell'effetto di turbolenza.](images/32-turbulence.png)

L'effetto di turbolenza calcola la somma di una o più ottave della funzione di disturbo Perlin. Il rumore Perlin è una funzione pseudo-casuale il cui valore dipende dalla frequenza, dalla posizione e dal valore di inizializzazione. L'effetto genera i valori RGBA usando una di queste equazioni.

Se si seleziona la \_ modalità di sintesi rumore del rumore di turbolenza d2d1 \_ \_ \_ , l'effetto usa questa equazione.

![Screenshot che mostra la funzione di turbolenza usata per generare una bitmap.](images/turbulence-equation1.png)

Se si seleziona la \_ \_ \_ modalità rumore di turbolenza del rumore d2d1, l'effetto usa questa equazione.

![funzione di turbolenza usata per generare una bitmap.](images/turbulence-equation2.png)

> [!Note]  
> La `PerlinNoise` funzione ha un intervallo di \[ -1, 1 \] .

 

Questo effetto restituisce i valori dei pixel in alfa premoltiplicati.

## <a name="effect-properties"></a>Proprietà effetto



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome visualizzato e enumerazione dell'indice</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Offset<br/> D2D1_TURBULENCE_PROP_OFFSET<br/></td>
<td>Coordinate in cui viene generato l'output di turbolenza.<br/> L'algoritmo utilizzato per generare il rumore Perlin è dipendente dalla posizione, quindi un offset diverso restituisce un output diverso. Questa proprietà non è associata e le unità sono specificate in DIP <br/>
<blockquote>
[!Note]<br />
L'offset non ha lo stesso effetto di una traduzione perché l'output della funzione Noise è infinito e la funzione esegue il wrapping intorno al riquadro.
</blockquote>
<br/> Il tipo è D2D1_VECTOR_2F.<br/> Il valore predefinito è {0,0 f, 0,0 f}.<br/></td>
</tr>
<tr class="even">
<td>Dimensione<br/> D2D1_TURBULENCE_PROP_SIZE<br/></td>
<td>Dimensioni dell'output di turbolenza.<br/> Questa proprietà non è associata e le unità sono specificate in DIP <br/>
<br/> Il tipo è D2D1_VECTOR_2F.<br/> Il valore predefinito è {0,0 f, 0,0 f}.<br/></td>
</tr>
<tr class="odd">
<td>BaseFrequency<br/> D2D1_TURBULENCE_PROP_BASE_FREQUENCY<br/></td>
<td>Frequenze di base nella direzione X e Y. Questa proprietà è di tipo float e deve essere maggiore di 0. Le unità vengono specificate in 1/dip. <br/> Il valore 1 (1/DIP) per la frequenza di base determina il rumore Perlin che completa un ciclo intero tra due pixel. L'interpolazione semplificata per questi pixel restituisce pixel completamente casuali, poiché non esiste alcuna correlazione tra i pixel.<br/> Il valore 0.1 (1/DIP) per la frequenza di base, la funzione del rumore Perlin si ripete ogni 10 DIP. Ciò comporta una correlazione tra i pixel e l'effetto di turbolenza tipico è visibile.<br/> Il tipo è D2D1_VECTOR_2F.<br/> Il valore predefinito è {0,01 f, 0,01 f}.<br/></td>
</tr>
<tr class="even">
<td>NumOctaves<br/> D2D1_TURBULENCE_PROP_NUM_OCTAVES<br/></td>
<td>Numero di ottave per la funzione noise. Questa proprietà è un oggetto UINT32 e deve essere maggiore di 0.<br/> Il tipo è UINT32.<br/> Il valore predefinito è 1.<br/></td>
</tr>
<tr class="odd">
<td>Seed<br/> D2D1_TURBULENCE_PROP_SEED<br/></td>
<td>Valore di inizializzazione per il generatore pseudo-casuale. Questa proprietà non è associata.<br/> Il tipo è UINT32.<br/> Il valore predefinito è 0.<br/></td>
</tr>
<tr class="even">
<td>Rumore<br/> D2D1_TURBULENCE_PROP_NOISE<br/></td>
<td>Modalità rumore di turbolenza. Questa proprietà può essere una somma o una <em>turbolenza</em> <em>frattale</em> . Indica se generare una bitmap basata sul rumore frattale o sulla funzione di turbolenza. Per altre informazioni, vedere <a href="#noise-modes">modalità di disturbo</a> . <br/> Il tipo è D2D1_TURBULENCE_NOISE.<br/> Il valore predefinito è D2D1_TURBULENCE_NOISE_FRACTAL_SUM.<br/></td>
</tr>
<tr class="odd">
<td>Cucibile<br/> D2D1_TURBULENCE_PROP_STITCHABLE<br/></td>
<td>Attiva o disattiva l'Unione. La frequenza di base viene modificata in modo che sia possibile unire le bitmap di output. Questa opzione è utile se si desidera affiancare più copie dell'output dell'effetto di turbolenza.
<ul>
<li>True la bitmap di output può essere affiancata (usando l'effetto del riquadro) senza l'aspetto di Seam. La frequenza di base viene modificata in modo che sia possibile unire le bitmap di output.</li>
<li>False la frequenza di base non è regolata, quindi le Seam possono apparire tra i riquadri se la bitmap è affiancata.</li>
</ul>
<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a>Modalità rumore



| Enumerazione                           | Descrizione                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| \_ \_ \_ Somma frattale rumore di turbolenza d2d1 \_ | Calcola una somma delle ottave, spostando l'intervallo di output da \[ -1, 1 \] , a \[ 0, 1 \] . |
| \_ \_ Turbolenza del rumore di TURBOLENZa d2d1 \_   | Calcola una somma del valore assoluto di ogni ottava.                                  |



 

> [!Note]  
> Nessuna delle due modalità contiene un morsetto esplicito dei valori di output.

 

## <a name="output-bitmap"></a>Bitmap di output

Questo effetto genera una bitmap di dimensioni infinite logicamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Intestazione                   | d2d1effects. h                                                                      |
| Libreria                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

