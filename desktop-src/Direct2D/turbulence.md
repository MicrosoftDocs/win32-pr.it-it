---
title: Effetto turbolenza
description: Usare l'effetto turbolenza per generare una bitmap basata sulla funzione disturbo Perlin.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- effetto turbolenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4eb8f57f98c8e69591b7772d710d6deb7a78c801f3ca027175c55460c2d529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824506"
---
# <a name="turbulence-effect"></a>Effetto turbolenza

Usare l'effetto turbolenza per generare una bitmap basata sulla funzione disturbo Perlin.

L'effetto turbolenza non ha un'immagine di input.

Il CLSID per questo effetto è CLSID \_ D2D1Turbulence.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Modalità disturbo](#noise-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

![Screenshot di esempio dell'effetto che mostra l'output dell'effetto turbolenza.](images/32-turbulence.png)

L'effetto Turbolenza calcola la somma di una o più ottave della funzione disturbo Perlin. Perlin noise è una funzione pseudo-casuale il cui valore dipende dalla frequenza, dalla posizione e dal valore di seed. L'effetto genera i valori RGBA usando una di queste equazioni.

Se si seleziona la modalità disturbo D2D1 \_ \_ TURBULENCE NOISE \_ FRACTAL \_ SUM, l'effetto usa questa equazione.

![Screenshot che mostra la funzione turbolenza usata per generare una bitmap.](images/turbulence-equation1.png)

Se si seleziona la modalità disturbo D2D1 \_ TURBULENCE \_ NOISE \_ TURBULENCE, l'effetto usa questa equazione.

![funzione turbolenza utilizzata per generare una bitmap.](images/turbulence-equation2.png)

> [!Note]  
> La `PerlinNoise` funzione ha un intervallo di \[ -1, 1 \] .

 

Questo effetto restituisce i valori dei pixel in alfa premoltilied.

## <a name="effect-properties"></a>Proprietà degli effetti



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome visualizzato ed enumerazione dell'indice</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Offset<br/> D2D1_TURBULENCE_PROP_OFFSET<br/></td>
<td>Coordinate in cui viene generato l'output di turbolenza.<br/> L'algoritmo usato per generare il disturbo Perlin dipende dalla posizione, quindi un offset diverso genera un output diverso. Questa proprietà non è delimitata e le unità vengono specificate in DIP <br/>
<blockquote>
[!Note]<br />
L'offset non ha lo stesso effetto di una traslazione perché l'output della funzione noise è infinito e la funzione esegue il wrapping intorno al riquadro.
</blockquote>
<br/> Il tipo è D2D1_VECTOR_2F.<br/> Il valore predefinito è {0.0f, 0.0f}.<br/></td>
</tr>
<tr class="even">
<td>Dimensione<br/> D2D1_TURBULENCE_PROP_SIZE<br/></td>
<td>Dimensioni dell'output di turbolenza.<br/> Questa proprietà non è delimitata e le unità vengono specificate in DIP <br/>
<br/> Il tipo è D2D1_VECTOR_2F.<br/> Il valore predefinito è {0.0f, 0.0f}.<br/></td>
</tr>
<tr class="odd">
<td>BaseFrequency<br/> D2D1_TURBULENCE_PROP_BASE_FREQUENCY<br/></td>
<td>Frequenze di base nella direzione X e Y. Questa proprietà è float e deve essere maggiore di 0. Le unità sono specificate in 1/DIP. <br/> Il valore 1 (1/DIP) per la frequenza di base determina il disturbo Perlin che completa un intero ciclo tra due pixel. La facilità di interpolazione per questi pixel comporta pixel completamente casuali, poiché non esiste alcuna correlazione tra i pixel.<br/> Valore 0,1(1/DIP) per la frequenza di base, la funzione disturbo Perlin si ripete ogni 10 DIP. In questo modo è visibile la correlazione tra i pixel e il tipico effetto turbolenza.<br/> Il tipo è D2D1_VECTOR_2F.<br/> Il valore predefinito è {0.01f, 0.01f}.<br/></td>
</tr>
<tr class="even">
<td>NumOctaves<br/> D2D1_TURBULENCE_PROP_NUM_OCTAVES<br/></td>
<td>Numero di ottave per la funzione noise. Questa proprietà è uiNT32 e deve essere maggiore di 0.<br/> Il tipo è UINT32.<br/> Il valore predefinito è 1.<br/></td>
</tr>
<tr class="odd">
<td>Seed<br/> D2D1_TURBULENCE_PROP_SEED<br/></td>
<td>Valore di seme per lo pseudo generatore casuale. Questa proprietà non è associata.<br/> Il tipo è UINT32.<br/> Il valore predefinito è 0.<br/></td>
</tr>
<tr class="even">
<td>Rumore<br/> D2D1_TURBULENCE_PROP_NOISE<br/></td>
<td>Modalità di disturbo di turbolenza. Questa proprietà può essere <em>somma frattale</em> o <em>turbolenza.</em> Indica se generare una bitmap in base al disturbo frattale o alla funzione Turbolenza. Per <a href="#noise-modes">altre informazioni, vedere</a> Modalità disturbo. <br/> Il tipo è D2D1_TURBULENCE_NOISE.<br/> Il valore predefinito è D2D1_TURBULENCE_NOISE_FRACTAL_SUM.<br/></td>
</tr>
<tr class="odd">
<td>Uniscibile<br/> D2D1_TURBULENCE_PROP_STITCHABLE<br/></td>
<td>Attiva o disattiva l'unione. La frequenza di base viene regolata in modo che sia possibile unire la bitmap di output. Ciò è utile se si desidera affiancare più copie dell'output dell'effetto turbolenza.
<ul>
<li>True La bitmap di output può essere affiancata (usando l'effetto riquadro) senza l'aspetto delle sezioni. La frequenza di base viene regolata in modo che sia possibile unire la bitmap di output.</li>
<li>False La frequenza di base non viene regolata, quindi possono essere visualizzate le sezioni tra i riquadri se la bitmap è affiancata.</li>
</ul>
<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a>Modalità disturbo



| Enumerazione                           | Descrizione                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| D2D1 \_ \_ TURBOLENZA DISTURBO \_ \_ FRATTALE SOMMA | Calcola una somma delle otte, spostando l'intervallo di output da \[ -1, 1 a \] \[ 0, \] 1. |
| TURBOLENZA DEL RUMORE DI TURBOLENZA D2D1 \_ \_ \_   | Calcola una somma del valore assoluto di ogni ottava.                                  |



 

> [!Note]  
> Nessuna delle due modalità contiene un'associazione esplicita dei valori di output.

 

## <a name="output-bitmap"></a>Bitmap di output

Questo effetto genera una bitmap logicamente infinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

