---
description: La compressione a blocchi è una tecnica di compressione di trama per la riduzione delle dimensioni della trama.
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: Compressione dei blocchi (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fcfb4bc91256415ab23686b7333df7d21df335d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558693"
---
# <a name="block-compression-direct3d-10"></a>Compressione dei blocchi (Direct3D 10)

La compressione a blocchi è una tecnica di compressione di trama per la riduzione delle dimensioni della trama. Rispetto a una trama con 32 bit per colore, una trama compressa da blocchi può essere fino al 75% di dimensioni inferiori. Le applicazioni in genere riscontrano un aumento delle prestazioni quando si usa la compressione a blocchi a causa del footprint di memoria inferiore.

Con la perdita di perdite, la compressione dei blocchi funziona correttamente ed è consigliata per tutte le trame che vengono trasformate e filtrate dalla pipeline. Le trame di cui è stato eseguito il mapping direttamente alla schermata (elementi dell'interfaccia utente come icone e testo) non sono ottime scelte per la compressione perché gli artefatti sono più evidenti.

Una trama compressa a blocchi deve essere creata come un multiplo di dimensioni 4 in tutte le dimensioni e non può essere usata come output della pipeline.

-   [Funzionamento della compressione dei blocchi](#how-does-block-compression-work)
    -   [Archiviazione di dati non compressi](#storing-uncompressed-data)
    -   [Archiviazione di dati compressi](#storing-compressed-data)
-   [Uso della compressione a blocchi](#using-block-compression)
    -   [Dimensioni virtuali rispetto alle dimensioni fisiche](#virtual-size-versus-physical-size)
-   [Algoritmi di compressione](#compression-algorithms)
    -   [BC1](#bc1)
    -   [RB2](#bc2)
    -   [BC3](#bc3)
    -   [BC4](#bc4)
    -   [BC5](#bc5)
-   [Conversione del formato con Direct3D 10,1](#format-conversion-using-direct3d-101)
-   [Argomenti correlati](#related-topics)

## <a name="how-does-block-compression-work"></a>Funzionamento della compressione dei blocchi

La compressione a blocchi è una tecnica che consente di ridurre la quantità di memoria necessaria per archiviare i dati dei colori. Archiviando alcuni colori nelle dimensioni originali e altri colori utilizzando uno schema di codifica, è possibile ridurre notevolmente la quantità di memoria necessaria per archiviare l'immagine. Poiché l'hardware decodifica automaticamente i dati compressi, non si verifica alcuna riduzione delle prestazioni per l'utilizzo di trame compresse.

Per informazioni sul funzionamento della compressione, vedere i due esempi seguenti. Nel primo esempio viene illustrata la quantità di memoria utilizzata per l'archiviazione di dati non compressi; nel secondo esempio viene descritta la quantità di memoria utilizzata per l'archiviazione dei dati compressi.

### <a name="storing-uncompressed-data"></a>Archiviazione di dati non compressi

La figura seguente rappresenta una trama 4 × 4 non compressa. Si supponga che ogni colore contenga un solo componente a colori (rosso per l'istanza) e che sia archiviato in un byte di memoria.

![illustrazione di una trama non compressa 4x4](images/d3d10-block-compress-1.png)

I dati non compressi sono disposti in memoria in sequenza e richiedono 16 byte, come illustrato nella figura seguente.

![illustrazione dei dati non compressi nella memoria sequenziale](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a>Archiviazione di dati compressi

Ora che è stata rilevata la quantità di memoria utilizzata da un'immagine non compressa, esaminare la quantità di memoria salvata da un'immagine compressa. Il formato di compressione [BC1](#bc1) archivia 2 colori (1 byte ciascuno) e indici a 16 3 bit (48 bit o 6 byte) usati per interpolare i colori originali nella trama, come illustrato nella figura seguente.

![illustrazione del formato di compressione BC1](images/d3d10-block-compress-3.png)

Lo spazio totale necessario per archiviare i dati compressi è di 8 byte, che corrisponde a un risparmio di memoria pari al 50% rispetto all'esempio non compresso. Il risparmio è ancora maggiore quando viene usato più di un componente colore.

Il notevole risparmio di memoria offerto dalla compressione dei blocchi può comportare un aumento delle prestazioni. Questa prestazione comporta il costo della qualità dell'immagine (a causa dell'interpolazione dei colori); Tuttavia, la qualità inferiore spesso non è evidente.

Nella sezione successiva viene illustrato come Direct3D 10 semplifica l'utilizzo della compressione a blocchi nell'applicazione.

## <a name="using-block-compression"></a>Uso della compressione a blocchi

Creare una trama compressa a blocchi come una trama non compressa (vedere [creare una trama da un file) con](d3d10-graphics-programming-guide-resources-creating-textures.md)la differenza che si specifica un formato compresso a blocchi.


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



Successivamente, creare una visualizzazione per associare la trama alla pipeline. Poiché una trama compressa a blocchi può essere usata solo come input per una fase shader, è necessario creare una visualizzazione delle risorse dello shader chiamando [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).

Usare una trama compressa a blocchi nello stesso modo in cui si usa una trama non compressa. Se l'applicazione otterrà un puntatore di memoria per i dati compressi in blocchi, è necessario tenere in considerazione la spaziatura della memoria in un mipmap che fa sì che le dimensioni dichiarate differiscano dalle dimensioni effettive.

### <a name="virtual-size-versus-physical-size"></a>Dimensioni virtuali rispetto alle dimensioni fisiche

Se si dispone di un codice dell'applicazione che usa un puntatore di memoria per esaminare la memoria di una trama compressa a blocchi, è necessario tenere presente una considerazione importante che potrebbe richiedere una modifica nel codice dell'applicazione. Una trama compressa a blocchi deve essere un multiplo di 4 in tutte le dimensioni perché gli algoritmi di compressione a blocchi operano su blocchi di Texel 4x4. Si tratta di un problema per un mipmap le cui dimensioni iniziali sono divisibili per 4, ma i livelli subdivisi non lo sono. Il diagramma seguente mostra la differenza di area tra la dimensione virtuale (dichiarata) e la dimensione fisica (effettiva) di ogni livello di mipmap.

![diagramma dei livelli di mipmap non compressi e compressi](images/d3d10-block-compress-pad.png)

Il lato sinistro del diagramma mostra le dimensioni del livello mipmap generate per una trama 60 × 40 non compressa. Le dimensioni di primo livello sono tratte dalla chiamata API che genera la trama; ogni livello successivo è la metà delle dimensioni del livello precedente. Per una trama non compressa, non esiste alcuna differenza tra le dimensioni virtuali (dichiarate) e le dimensioni fisiche (effettive).

Il lato destro del diagramma mostra le dimensioni del livello mipmap generate per la stessa trama 60 × 40 con compressione. Si noti che il secondo e il terzo livello hanno riempimento della memoria per rendere i fattori di dimensioni 4 a ogni livello. Questa operazione è necessaria in modo che gli algoritmi possano operare su blocchi di 4 × 4 Texel. Questo è particolarmente evidente se si considerano i livelli mipmap inferiori a 4 × 4; la dimensione di questi livelli mipmap molto piccoli verrà arrotondata al fattore più vicino di 4 quando viene allocata la memoria della trama.

L'hardware di campionamento usa la dimensione virtuale; Quando si campiona la trama, il riempimento della memoria viene ignorato. Per i livelli mipmap inferiori a 4 × 4, verranno usati solo i primi quattro Texel per una mappa 2 × 2 e solo il primo Texel verrà usato da un blocco 1 × 1. Tuttavia, non esiste alcuna struttura API che espone le dimensioni fisiche (inclusa la spaziatura interna della memoria).

In breve, prestare attenzione a usare blocchi di memoria allineati quando si copiano aree che contengono dati compressi in blocchi. Per eseguire questa operazione in un'applicazione che ottiene un puntatore di memoria, verificare che il puntatore usi il passo della superficie per tenere conto delle dimensioni della memoria fisica.

## <a name="compression-algorithms"></a>Algoritmi di compressione

Le tecniche di compressione dei blocchi in Direct3D suddividono i dati di trama non compressi in 4 × 4 blocchi, comprimono ogni blocco e quindi archiviano i dati. Per questo motivo, è previsto che le trame siano compresse devono avere dimensioni di trama multipli di 4.

![diagramma della compressione dei blocchi](images/d3d10-compression-1.png)

Il diagramma precedente mostra una trama partizionata in blocchi Texel. Il primo blocco Mostra il layout dei 16 Texel con etichetta a-p, ma ogni blocco ha la stessa organizzazione di dati.

Direct3D implementa diversi schemi di compressione, ognuno dei quali implementa un compromesso diverso tra il numero di componenti archiviati, il numero di bit per componente e la quantità di memoria utilizzata. Usare questa tabella per scegliere il formato più adatto al tipo di dati e alla risoluzione dei dati più adatta all'applicazione.



| Origine dati                     | Risoluzione della compressione dei dati (in bit) | Scegliere questo formato di compressione |
|---------------------------------|---------------------------------------|--------------------------------|
| Colore a tre componenti e alfa | Color (5:6:5), Alpha (1) o nessun Alpha  | BC1                            |
| Colore a tre componenti e alfa | Colore (5:6:5), Alfa (4)              | [RB2](#bc2)                    |
| Colore a tre componenti e alfa | Colore (5:6:5), Alfa (8)              | [BC3](#bc3)                    |
| Colore di un componente             | Un componente (8)                     | [BC4](#bc4)                    |
| Colore a due componenti             | Due componenti (8:8)                  | [BC5](#bc5)                    |



 

### <a name="bc1"></a>BC1

Usare il primo formato di compressione a blocchi (BC1) (DXGI \_ Format BC1, formato \_ \_ DXGI \_ BC1 UNORM o DXGI BC1 UNORM \_ \_ \_ \_ \_ sRGB) per archiviare dati di colore a tre componenti usando un colore 5:6:5 (5 bit in rosso, 6 bit verde, 5 bit blu). Questo vale anche se i dati contengono anche Alfa a 1 bit. Supponendo una trama 4 × 4 con il formato dati più grande possibile, il formato BC1 riduce la quantità di memoria richiesta da 48 byte (16 colori × 3 componenti/colore × 1 byte/componente) a 8 byte di memoria.

L'algoritmo funziona su 4 × 4 blocchi di Texel. Anziché archiviare 16 colori, l'algoritmo Salva due colori di riferimento (colore \_ 0 e colore \_ 1) e indici di colore a 16 2 bit (blocca a-p), come illustrato nel diagramma seguente.

![diagramma del layout per la compressione BC1](images/d3d10-compression-bc1.png)

Gli indici di colore (a-p) vengono usati per cercare i colori originali da una tabella dei colori. La tabella dei colori contiene 4 colori. I primi due colori, ovvero colore \_ 0 e colore \_ 1, sono i colori minimo e massimo. Gli altri due colori, colore \_ 2 e colore \_ 3, sono colori intermedi calcolati con l'interpolazione lineare.


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



Ai quattro colori vengono assegnati valori di indice a 2 bit che verranno salvati nei blocchi a-p.


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



Infine, ognuno dei colori nei blocchi a-p viene confrontato con i quattro colori della tabella dei colori e l'indice per il colore più vicino viene archiviato nei blocchi a 2 bit.

Questo algoritmo si presta ai dati che contengono anche Alpha a 1 bit. L'unica differenza è che color \_ 3 è impostato su 0 (che rappresenta un colore trasparente) e il colore \_ 2 è una combinazione lineare di colore \_ 0 e colore \_ 1.


```
color_2 = 1/2*color_0 + 1/2*color_1;
color_3 = 0;
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 10:<br/> Questo formato è disponibile sia in Direct3D 9 che in 10.<br/>
<ul>
<li>In Direct3D 9 il formato BC1 è denominato D3DFMT_DXT1.</li>
<li>In Direct3D 10 il formato BC1 è rappresentato da DXGI_FORMAT_BC1_UNORM o DXGI_FORMAT_BC1_UNORM_SRGB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a>RB2

Usare il formato BC2 (DXGI \_ Format \_ BC2 \_ senza tipo, DXGI Format BC2 UNORM o DXGI BC2 UNORM \_ \_ \_ \_ \_ \_ sRGB) per archiviare i dati che contengono i dati di colore e alfa con coerenza Bassi (usare [BC3](#bc3) per dati alfa altamente coerenti). Il formato BC2 archivia i dati RGB come un colore 5:6:5 (5 bit rosso, 6 bit verde, 5 bit blu) e alfa come valore separato a 4 bit. Supponendo una trama 4 × 4 con il formato dati più grande possibile, questa tecnica di compressione riduce la quantità di memoria richiesta da 64 byte (16 colori × 4 componenti/colore × 1 byte/componente) a 16 byte di memoria.

Il formato BC2 archivia i colori con lo stesso numero di bit e il layout dei dati del formato [BC1](#bc1) ; Tuttavia, BC2 richiede altri 64 bit di memoria per archiviare i dati alfa, come illustrato nel diagramma seguente.

![diagramma del layout per la compressione BC2](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 10:<br/> Questo formato è disponibile sia in Direct3D 9 che in 10.<br/>
<ul>
<li>In Direct3D 9 il formato BC2 è denominato D3DFMT_DXT2 e D3DFMT_DXT3.</li>
<li>In Direct3D 10 il formato BC2 è rappresentato da DXGI_FORMAT_BC2_UNORM o DXGI_FORMAT_BC2_UNORM_SRGB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a>BC3

Usare il formato BC3 (DXGI \_ Format \_ BC3, formato \_ DXGI \_ BC3 UNORM o DXGI BC3 UNORM \_ \_ \_ \_ \_ sRGB) per archiviare dati di colore altamente coerenti (usare [BC2](#bc2) con dati alfa meno coerenti). Il formato BC3 archivia i dati relativi ai colori utilizzando il colore 5:6:5 (5 bit rosso, 6 bit verde, 5 bit blu) e i dati alfa utilizzando un solo byte. Supponendo una trama 4 × 4 con il formato dati più grande possibile, questa tecnica di compressione riduce la quantità di memoria richiesta da 64 byte (16 colori × 4 componenti/colore × 1 byte/componente) a 16 byte di memoria.

Il formato BC3 archivia i colori con lo stesso numero di bit e il layout dei dati del formato [BC1](#bc1) ; Tuttavia, BC3 richiede altri 64 bit di memoria per archiviare i dati alfa. Il formato BC3 gestisce Alpha archiviando due valori di riferimento e interpolando tra di essi, in modo analogo al modo in cui BC1 archivia il colore RGB.

L'algoritmo funziona su 4 × 4 blocchi di Texel. Anziché archiviare 16 valori alfa, l'algoritmo archivia 2 alfa di riferimento (Alpha \_ 0 e Alpha \_ 1) e indici di colore a 16 3 bit (da Alpha a a p), come illustrato nel diagramma seguente.

![diagramma del layout per la compressione BC3](images/d3d10-compression-bc3.png)

Il formato BC3 utilizza gli indici alfa (a-p) per cercare i colori originali da una tabella di ricerca che contiene 8 valori. I primi due valori, ovvero Alpha \_ 0 e Alpha \_ 1, sono i valori minimo e massimo. gli altri sei valori intermedi vengono calcolati usando l'interpolazione lineare.

L'algoritmo determina il numero di valori alfa interpolati esaminando i due valori alfa di riferimento. Se alfa \_ 0 è maggiore di alfa \_ 1, BC3 interpolano 6 valori alfa; in caso contrario, esegue l'interpolazione 4. Quando BC3 interpola solo 4 valori alfa, imposta due valori alfa aggiuntivi (0 per completamente trasparente e 255 per l'intero opaco). BC3 comprime i valori alfa nell'area di Texel 4 × 4 archiviando il codice di bit corrispondente ai valori alfa interpolati che corrisponde maggiormente all'alfa originale per un dato Texel.


```
if( alpha_0 > alpha_1 )
{
  // 6 interpolated alpha values.
  alpha_2 = 6/7*alpha_0 + 1/7*alpha_1; // bit code 010
  alpha_3 = 5/7*alpha_0 + 2/7*alpha_1; // bit code 011
  alpha_4 = 4/7*alpha_0 + 3/7*alpha_1; // bit code 100
  alpha_5 = 3/7*alpha_0 + 4/7*alpha_1; // bit code 101
  alpha_6 = 2/7*alpha_0 + 5/7*alpha_1; // bit code 110
  alpha_7 = 1/7*alpha_0 + 6/7*alpha_1; // bit code 111
}
else
{
  // 4 interpolated alpha values.
  alpha_2 = 4/5*alpha_0 + 1/5*alpha_1; // bit code 010
  alpha_3 = 3/5*alpha_0 + 2/5*alpha_1; // bit code 011
  alpha_4 = 2/5*alpha_0 + 3/5*alpha_1; // bit code 100
  alpha_5 = 1/5*alpha_0 + 4/5*alpha_1; // bit code 101
  alpha_6 = 0;                         // bit code 110
  alpha_7 = 255;                       // bit code 111
}
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 10:<br/>
<ul>
<li>In Direct3D 9 il formato BC3 è denominato D3DFMT_DXT4 e D3DFMT_DXT5.</li>
<li>In Direct3D 10 il formato BC3 è rappresentato da DXGI_FORMAT_BC3_UNORM o DXGI_FORMAT_BC3_UNORM_SRGB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc4"></a>BC4

Usare il formato BC4 per archiviare i dati dei colori di un componente usando 8 bit per ogni colore. A causa della maggiore precisione (rispetto a [BC1](#bc1)), BC4 è la soluzione ideale per l'archiviazione di dati a virgola mobile nell'intervallo compreso tra \[ 0 \] e 1 usando il formato DXGI \_ \_ BC4 \_ UNORM e \[ da-1 a + 1 \] usando il formato DXGI \_ BC4 il \_ \_ formato russamento. Supponendo una trama 4 × 4 con il formato dati più grande possibile, questa tecnica di compressione riduce la quantità di memoria richiesta da 16 byte (16 colori × 1 componenti/colore × 1 byte/componente) a 8 byte.

L'algoritmo funziona su 4 × 4 blocchi di Texel. Anziché archiviare 16 colori, l'algoritmo archivia 2 colori di riferimento (rosso \_ 0 e rosso \_ 1) e indici di colore a 16 3 bit (da rosso a a p rosso), come illustrato nella figura seguente.

![diagramma del layout per la compressione BC4](images/d3d10-compression-bc4.png)

L'algoritmo utilizza gli indici a 3 bit per cercare i colori di una tabella dei colori che contiene 8 colori. I primi due colori, Rossi \_ 0 e rossi \_ 1, sono i colori minimo e massimo. L'algoritmo calcola i colori rimanenti utilizzando l'interpolazione lineare.

L'algoritmo determina il numero di valori dei colori interpolati esaminando i due valori di riferimento. Se il colore rosso \_ 0 è maggiore di quello rosso \_ 1, BC4 interpola i 6 valori dei colori; in caso contrario, interpola 4. Quando BC4 esegue l'interpolazione solo di 4 valori di colore, imposta due valori di colore aggiuntivi (0,0 f per completamente trasparente e 1,0 f per l'opacità completa). BC4 comprime i valori alfa nell'area di Texel 4 × 4 archiviando il codice di bit corrispondente ai valori alfa interpolati che corrispondono maggiormente all'alfa originale per un dato Texel.

-   [\_UNORM BC4](/windows)
-   [BC4 \_ russare](/windows)

### <a name="bc4_unorm"></a>\_UNORM BC4

L'interpolazione dei dati a componente singolo viene eseguita come nell'esempio di codice seguente.


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



Ai colori di riferimento vengono assegnati indici a 3 bit (000 – 111 poiché sono presenti 8 valori), che verranno salvati in blocchi da rosso a a p rosso durante la compressione.

### <a name="bc4_snorm"></a>BC4 \_ russare

Il \_ formato DXGI \_ BC4 \_ russa è identico, ad eccezione del fatto che i dati sono codificati in un intervallo di russamento e quando vengono interpolati 4 valori di colore. L'interpolazione dei dati a componente singolo viene eseguita come nell'esempio di codice seguente.


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                     // bit code 110
  red_7 =  1.0f;                     // bit code 111
}
```



Ai colori di riferimento vengono assegnati indici a 3 bit (000 – 111 poiché sono presenti 8 valori), che verranno salvati in blocchi da rosso a a p rosso durante la compressione.

### <a name="bc5"></a>BC5

Usare il formato BC5 per archiviare i dati di colore a due componenti usando 8 bit per ogni colore. A causa della maggiore precisione (rispetto a [BC1](#bc1)), BC5 è la soluzione ideale per l'archiviazione di dati a virgola mobile nell'intervallo compreso tra \[ 0 \] e 1 usando il formato DXGI \_ \_ BC5 \_ UNORM e \[ da-1 a + 1 \] usando il formato DXGI \_ BC5 il \_ \_ formato russamento. Supponendo una trama 4 × 4 con il formato dati più grande possibile, questa tecnica di compressione riduce la quantità di memoria richiesta da 32 byte (16 colori × 2 componenti/colore × 1 byte/componente) a 16 byte.

L'algoritmo funziona su 4 × 4 blocchi di Texel. Anziché archiviare 16 colori per entrambi i componenti, l'algoritmo archivia 2 colori di riferimento per ogni componente (rosso \_ 0, rosso \_ 1, verde \_ 0 e verde \_ 1) e indici di colore a 16 3 bit per ogni componente (da rosso a a rosso p e da verde a a p verde), come illustrato nel diagramma seguente.

![diagramma del layout per la compressione BC5](images/d3d10-compression-bc5.png)

L'algoritmo utilizza gli indici a 3 bit per cercare i colori di una tabella dei colori che contiene 8 colori. I primi due colori, Rossi \_ 0 e rossi \_ 1 (o verde \_ 0 e verde \_ 1), sono i colori minimo e massimo. L'algoritmo calcola i colori rimanenti utilizzando l'interpolazione lineare.

L'algoritmo determina il numero di valori dei colori interpolati esaminando i due valori di riferimento. Se il colore rosso \_ 0 è maggiore di quello rosso \_ 1, BC5 interpola i 6 valori dei colori; in caso contrario, interpola 4. Quando BC5 esegue l'interpolazione solo di 4 valori di colore, imposta i restanti due valori di colore su 0,0 f e 1,0 f.

-   [\_UNORM BC5](/windows)
-   [BC5 \_ russare](/windows)

### <a name="bc5_unorm"></a>\_UNORM BC5

L'interpolazione dei dati a componente singolo viene eseguita come nell'esempio di codice seguente. I calcoli per i componenti verdi sono simili.


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



Ai colori di riferimento vengono assegnati indici a 3 bit (000 – 111 poiché sono presenti 8 valori), che verranno salvati in blocchi da rosso a a p rosso durante la compressione.

### <a name="bc5_snorm"></a>BC5 \_ russare

Il \_ formato DXGI \_ BC5 \_ russa è identico, ad eccezione del fatto che i dati sono codificati nell'intervallo di russamento e quando 4 valori di dati vengono interpolati, i due valori aggiuntivi sono-1.0 f e 1.0 f. L'interpolazione dei dati a componente singolo viene eseguita come nell'esempio di codice seguente. I calcoli per i componenti verdi sono simili.


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                    // bit code 110
  red_7 =  1.0f;                    // bit code 111
}
```



Ai colori di riferimento vengono assegnati indici a 3 bit (000 – 111 poiché sono presenti 8 valori), che verranno salvati in blocchi da rosso a a p rosso durante la compressione.

## <a name="format-conversion-using-direct3d-101"></a>Conversione del formato con Direct3D 10,1

Direct3D 10,1 Abilita le copie tra trame tipizzate in modo prestrutturato e trame compresse con le stesse larghezze di bit. Le funzioni che possono eseguire questa operazione sono [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).

A partire da Direct3D 10,1, è possibile usare [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) per copiare alcuni tipi di formato. Questo tipo di operazione di copia esegue un tipo di conversione del formato che reinterpreta i dati delle risorse con un tipo di formato diverso. Si consideri questo esempio in cui viene illustrata la differenza tra la reinterpretazione dei dati e il comportamento di un tipo più tipico di conversione:


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



Per interpretare ' f ' come tipo di ' u ', usare [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



Nella riinterpretazione precedente, il valore sottostante dei dati non cambia; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterpreta il float come Unsigned Integer.

Per eseguire il tipo di conversione più comune, usare l'assegnazione:


```
    u = f; // ‘u’ becomes 1.
```



Nella conversione precedente, il valore sottostante dei dati viene modificato.

Nella tabella seguente sono elencati i formati di origine e di destinazione consentiti che è possibile utilizzare in questo tipo di riinterpretazione della conversione del formato. È necessario codificare correttamente i valori affinché la riinterpretazione funzioni come previsto.



| Larghezza bit | Risorsa non compressa                                                                                                                                               | Risorsa Block-Compressed                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 32        | \_Formato DXGI \_ R32 \_ uint<br/> \_Formato DXGI \_ R32 \_ Sint<br/>                                                                                               | \_Formato DXGI \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                   |
| 64        | \_Formato DXGI \_ R16G16B16A16 \_ uint<br/> \_Formato DXGI \_ R16G16B16A16 \_ Sint<br/> \_Formato DXGI \_ R32G32 \_ uint<br/> \_Formato DXGI \_ R32G32 \_ Sint<br/> | \_Formato DXGI \_ BC1 \_ UNORM \[ \_ sRGB\]<br/> \_Formato DXGI \_ BC4 \_ UNORM<br/> DXGI \_ Format \_ BC4 \_ russar<br/>                                               |
| 128       | \_Formato DXGI \_ R32G32B32A32 \_ uint<br/> \_Formato DXGI \_ R32G32B32A32 \_ Sint<br/>                                                                             | \_Formato DXGI \_ BC2 \_ UNORM \[ \_ sRGB\]<br/> \_Formato DXGI \_ BC3 \_ UNORM \[ \_ sRGB\]<br/> \_Formato DXGI \_ BC5 \_ UNORM<br/> DXGI \_ Format \_ BC5 \_ russar<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
