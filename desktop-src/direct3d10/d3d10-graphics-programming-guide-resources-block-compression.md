---
description: La compressione a blocchi è una tecnica di compressione delle trame per ridurre le dimensioni della trama.
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: Compressione a blocchi (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c3a74fba0b4c7c2adade210a9a54952b5d1269
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436547"
---
# <a name="block-compression-direct3d-10"></a>Compressione a blocchi (Direct3D 10)

La compressione a blocchi è una tecnica di compressione delle trame per ridurre le dimensioni della trama. Rispetto a una trama con 32 bit per colore, una trama compressa in blocchi può essere fino al 75% più piccola. Le applicazioni in genere vedono un aumento delle prestazioni quando si usa la compressione dei blocchi a causa del footprint di memoria più ridotto.

Anche se la compressione a blocchi è in perdita, funziona bene ed è consigliata per tutte le trame che vengono trasformate e filtrate in base alla pipeline. Le trame mappate direttamente allo schermo (elementi dell'interfaccia utente come icone e testo) non sono scelte valide per la compressione perché gli artefatti sono più evidenti.

Una trama compressa a blocchi deve essere creata come multiplo di dimensioni 4 in tutte le dimensioni e non può essere usata come output della pipeline.

-   [Come funziona la compressione a blocchi?](#how-does-block-compression-work)
    -   [Archiviazione di dati non compressi](#storing-uncompressed-data)
    -   [Archiviazione di dati compressi](#storing-compressed-data)
-   [Uso della compressione dei blocchi](#using-block-compression)
    -   [Dimensioni virtuali e dimensioni fisiche](#virtual-size-versus-physical-size)
-   [Algoritmi di compressione](#compression-algorithms)
    -   [BC1](#bc1)
    -   [RB2](#bc2)
    -   [BC3](#bc3)
    -   [BC4](#bc4)
    -   [BC5](#bc5)
-   [Conversione del formato con Direct3D 10.1](#format-conversion-using-direct3d-101)
-   [Argomenti correlati](#related-topics)

## <a name="how-does-block-compression-work"></a>Come funziona la compressione a blocchi?

La compressione a blocchi è una tecnica per ridurre la quantità di memoria necessaria per archiviare i dati sui colori. Archiviando alcuni colori nelle dimensioni originali e altri colori usando uno schema di codifica, è possibile ridurre notevolmente la quantità di memoria necessaria per archiviare l'immagine. Poiché l'hardware decodifica automaticamente i dati compressi, non vi sono problemi di prestazioni per l'uso di trame compresse.

Per verificare il funzionamento della compressione, vedere i due esempi seguenti. Il primo esempio descrive la quantità di memoria usata per l'archiviazione di dati non compressi. Il secondo esempio descrive la quantità di memoria usata per l'archiviazione di dati compressi.

### <a name="storing-uncompressed-data"></a>Archiviazione di dati non compressi

La figura seguente rappresenta una trama 4×4 non compressa. Si supponga che ogni colore contenga un singolo componente di colore (rosso, ad esempio) e sia archiviato in un byte di memoria.

![Illustrazione di una trama 4x4 non compressa](images/d3d10-block-compress-1.png)

I dati non compressi vengono disposti in memoria in sequenza e richiedono 16 byte, come illustrato nella figura seguente.

![Illustrazione dei dati non compressi nella memoria sequenziale](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a>Archiviazione di dati compressi

Dopo aver visto la quantità di memoria utilizzata da un'immagine non compressa, esaminare la quantità di memoria risparmiata da un'immagine compressa. Il formato di compressione [BC4](#bc4) archivia 2 colori (1 byte ciascuno) e 16 indici a 3 bit (48 bit o 6 byte) usati per interpolare i colori originali nella trama, come illustrato nella figura seguente.

![Illustrazione del formato di compressione bc4](images/d3d10-block-compress-3.png)

Lo spazio totale necessario per archiviare i dati compressi è di 8 byte, ovvero un risparmio di memoria del 50% rispetto all'esempio non compresso. Il risparmio è ancora maggiore quando si usa più di un componente di colore.

Il notevole risparmio di memoria offerto dalla compressione dei blocchi può comportare un aumento delle prestazioni. Queste prestazioni sono a costo della qualità dell'immagine (a causa dell'interpolazione dei colori); tuttavia, la qualità inferiore spesso non è evidente.

La sezione successiva illustra come Direct3D 10 semplifica l'uso della compressione a blocchi nell'applicazione.

## <a name="using-block-compression"></a>Uso della compressione dei blocchi

Creare una trama compressa a blocchi esattamente come una trama non compressa (vedere Creare una trama da un [file](d3d10-graphics-programming-guide-resources-creating-textures.md)), ad eccezione del fatto che si specifica un formato compresso a blocchi.


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



Creare quindi una vista per associare la trama alla pipeline. Poiché una trama compressa a blocchi può essere usata solo come input per una fase shader, si vuole creare una visualizzazione di risorse shader chiamando [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).

Usare una trama compressa a blocchi nello stesso modo in cui si usa una trama non compressa. Se l'applicazione otterrà un puntatore di memoria ai dati compressi in blocchi, è necessario prendere in considerazione la spaziatura interna della memoria in un mipmap che fa sì che le dimensioni dichiarate siano diverse dalle dimensioni effettive.

### <a name="virtual-size-versus-physical-size"></a>Dimensioni virtuali e dimensioni fisiche

Se si dispone di codice dell'applicazione che usa un puntatore di memoria per la memoria di una trama compressa in blocchi, è importante considerare che potrebbe essere necessaria una modifica nel codice dell'applicazione. Una trama compressa a blocchi deve essere un multiplo di 4 in tutte le dimensioni perché gli algoritmi di compressione a blocchi operano su blocchi texel 4x4. Si tratta di un problema per un mipmap le cui dimensioni iniziali sono divisibile per 4, ma i livelli suddivisi non lo sono. Il diagramma seguente illustra la differenza nell'area tra le dimensioni virtuali (dichiarate) e le dimensioni fisiche (effettive) di ogni livello mipmap.

![Diagramma dei livelli mipmap non compressi e compressi](images/d3d10-block-compress-pad.png)

Il lato sinistro del diagramma mostra le dimensioni del livello mipmap generate per una trama non compressa di 60×40. Le dimensioni di primo livello vengono prese dalla chiamata API che genera la trama. ogni livello successivo è la metà delle dimensioni del livello precedente. Per una trama non compressa, non esiste alcuna differenza tra le dimensioni virtuali (dichiarate) e le dimensioni fisiche (effettive).

Il lato destro del diagramma mostra le dimensioni del livello mipmap generate per la stessa trama da 60×40 con compressione. Si noti che sia il secondo che il terzo livello hanno spaziatura interna della memoria per rendere i fattori di dimensioni di 4 per ogni livello. Questa operazione è necessaria in modo che gli algoritmi possano operare su 4×4 blocchi di texel. Questo è evidente se si considerano livelli mipmap inferiori a 4×4; le dimensioni di questi livelli mipmap molto piccoli verranno arrotondate al fattore più vicino di 4 quando viene allocata la memoria della trama.

L'hardware di campionamento usa le dimensioni virtuali. Quando la trama viene campionata, la spaziatura interna della memoria viene ignorata. Per i livelli mipmap inferiori a 4×4, verranno usati solo i primi quattro texel per una mappa 2×2 e solo il primo texel verrà usato da un blocco 1×1. Non esiste tuttavia una struttura API che esponga le dimensioni fisiche (inclusa la spaziatura interna della memoria).

In sintesi, prestare attenzione all'uso di blocchi di memoria allineati durante la copia di aree contenenti dati compressi a blocchi. A tale scopo in un'applicazione che ottiene un puntatore di memoria, assicurarsi che il puntatore usi l'altezza della superficie per prendere in considerazione le dimensioni della memoria fisica.

## <a name="compression-algorithms"></a>Algoritmi di compressione

Le tecniche di compressione a blocchi in Direct3D suddivideno i dati di trama non compressi in 4 blocchi×4, comprimono ogni blocco e quindi archiviano i dati. Per questo motivo, si prevede che le trame siano compresse devono avere dimensioni di trama multiple di 4.

![Diagramma della compressione a blocchi](images/d3d10-compression-1.png)

Il diagramma precedente mostra una trama partizionata in blocchi texel. Il primo blocco mostra il layout dei 16 texel con etichetta a-p, ma ogni blocco ha la stessa organizzazione di dati.

Direct3D implementa diversi schemi di compressione, ognuno dei quali implementa un compromesso diverso tra il numero di componenti archiviati, il numero di bit per componente e la quantità di memoria utilizzata. Usare questa tabella per scegliere il formato più adatto al tipo di dati e alla risoluzione dei dati più adatta all'applicazione.



| Origine dati                     | Risoluzione della compressione dei dati (in bit) | Scegliere questo formato di compressione |
|---------------------------------|---------------------------------------|--------------------------------|
| Colore e alfa a tre componenti | Colore (5:6:5), Alfa (1) o nessun carattere alfa  | BC1                            |
| Colore e alfa a tre componenti | Colore (5:6:5), Alfa (4)              | [RB2](#bc2)                    |
| Colore e alfa a tre componenti | Colore (5:6:5), Alfa (8)              | [BC3](#bc3)                    |
| Colore a un componente             | Un componente (8)                     | [BC4](#bc4)                    |
| Colore a due componenti             | Due componenti (8:8)                  | [BC5](#bc5)                    |



 

### <a name="bc1"></a>BC1

Usare il primo formato di compressione blocchi (BC1) (DXGI FORMAT BC1 TYPELESS, DXGI FORMAT BC1 UNORM o DXGI BC1 UNORM SRGB) per archiviare i dati dei colori a tre componenti usando un colore \_ \_ \_ \_ \_ \_ \_ \_ \_ 5:6:5 (5 bit rosso, 6 bit verdi, 5 bit blu). Questo vale anche se i dati contengono anche caratteri alfa a 1 bit. Supponendo che una trama 4×4 utilizzi il formato dati più grande possibile, il formato BC1 riduce la memoria necessaria da 48 byte (16 colori × 3 componenti/colore × 1 byte/componente) a 8 byte di memoria.

L'algoritmo funziona su 4×4 blocchi di texel. Anziché archiviare 16 colori, l'algoritmo salva 2 colori di riferimento (colore 0 e colore 1) e indici di \_ \_ colore a 16 a 2 bit (blocchi a-p), come illustrato nel diagramma seguente.

![Diagramma del layout per la compressione bc1](images/d3d10-compression-bc1.png)

Gli indici dei colori (a-p) vengono usati per cercare i colori originali da una tabella dei colori. La tabella dei colori contiene 4 colori. I primi due colori, ovvero \_ il colore 0 e il \_ colore 1, sono i colori minimo e massimo. Gli altri due colori, il \_ colore 2 e il \_ colore 3, sono colori intermedi calcolati con l'interpolazione lineare.


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



Infine, ognuno dei colori nei blocchi a-p viene confrontato con i quattro colori nella tabella dei colori e l'indice per il colore più vicino viene archiviato nei blocchi a 2 bit.

Questo algoritmo si presta a dati che contengono anche alfa a 1 bit. L'unica differenza è che il colore 3 è impostato su 0 (che rappresenta un colore trasparente) e il colore 2 è una combinazione lineare di colore \_ \_ \_ 0 e \_ colore 1.


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
<td>Differenze tra Direct3D 9 e Direct3D 10:<br/> Questo formato esiste sia in Direct3D 9 che in 10.<br/>
<ul>
<li>In Direct3D 9 il formato BC1 è denominato D3DFMT_DXT1.</li>
<li>In Direct3D 10 il formato BC1 è rappresentato da DXGI_FORMAT_BC1_UNORM o DXGI_FORMAT_BC1_UNORM_SRGB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a>RB2

Usare il formato BC2 (DXGI \_ FORMAT \_ BC2 \_ TYPELESS, DXGI \_ FORMAT BC2 UNORM o \_ \_ DXGI \_ BC2 UNORM SRGB) per archiviare i dati che contengono dati di colore e alfa con bassa \_ \_ coerenza (usare [BC3](#bc3) per dati alfa altamente coerenti). Il formato BC2 archivia i dati RGB come colore 5:6:5 (rosso a 5 bit, verde a 6 bit, blu a 5 bit) e alfa come valore a 4 bit separato. Supponendo una trama 4×4 con il formato di dati più grande possibile, questa tecnica di compressione riduce la memoria necessaria da 64 byte (16 colori × 4 componenti/colore × 1 byte/componente) a 16 byte di memoria.

Il formato BC2 archivia i colori con lo stesso numero di bit e layout di dati del [formato BC1.](#bc1) TUTTAVIA, BC2 richiede altri 64 bit di memoria per archiviare i dati alfa, come illustrato nel diagramma seguente.

![Diagramma del layout per la compressione bc2](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 10:<br/> Questo formato esiste sia in Direct3D 9 che in 10.<br/>
<ul>
<li>In Direct3D 9 il formato BC2 è denominato D3DFMT_DXT2 e D3DFMT_DXT3.</li>
<li>In Direct3D 10 il formato BC2 è rappresentato da DXGI_FORMAT_BC2_UNORM o DXGI_FORMAT_BC2_UNORM_SRGB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a>BC3

Usare il formato BC3 (DXGI \_ FORMAT \_ BC3 \_ TYPELESS, DXGI \_ FORMAT BC3 UNORM o \_ \_ DXGI \_ BC3 \_ UNORM \_ SRGB) [](#bc2) per archiviare dati di colore altamente coerenti (usare BC2 con dati alfa meno coerenti). Il formato BC3 archivia i dati sui colori usando i dati di colore 5:6:5 (rosso 5 bit, verde a 6 bit, blu a 5 bit) e dati alfa con un byte. Supponendo una trama 4×4 con il formato di dati più grande possibile, questa tecnica di compressione riduce la memoria necessaria da 64 byte (16 colori × 4 componenti/colore × 1 byte/componente) a 16 byte di memoria.

Il formato BC3 archivia i colori con lo stesso numero di bit e layout di dati del [formato BC1.](#bc1) TUTTAVIA, BC3 richiede altri 64 bit di memoria per archiviare i dati alfa. Il formato BC3 gestisce i valori alfa archiviando due valori di riferimento e interpolandoli tra di essi (in modo analogo al modo in cui BC1 archivia il colore RGB).

L'algoritmo funziona su 4×4 blocchi di texel. Anziché archiviare 16 valori alfa, l'algoritmo archivia 2 indici alfa di riferimento (alfa 0 e alfa 1) e 16 indici di colore a \_ 3 bit (da alfa a p), come illustrato nel diagramma \_ seguente.

![Diagramma del layout per la compressione bc3](images/d3d10-compression-bc3.png)

Il formato BC3 usa gli indici alfa (a-p) per cercare i colori originali da una tabella di ricerca che contiene 8 valori. I primi due valori, alfa 0 e alfa 1, sono i valori minimo e massimo. Gli altri sei valori intermedi vengono calcolati usando \_ \_ l'interpolazione lineare.

L'algoritmo determina il numero di valori alfa interpolati esaminando i due valori alfa di riferimento. Se alpha \_ 0 è maggiore di alpha \_ 1, BC3 interpola 6 valori alfa; in caso contrario, interpola 4. Quando BC3 interpola solo 4 valori alfa, imposta due valori alfa aggiuntivi (0 per completamente trasparente e 255 per completamente opaco). BC3 comprime i valori alfa nell'area texel 4×4 archiviando il codice di bit corrispondente ai valori alfa interpolati che corrispondono maggiormente al valore alfa originale per un determinato texel.


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

Usare il formato BC4 per archiviare i dati di colore a un componente usando 8 bit per ogni colore. A causa della maggiore accuratezza (rispetto a [BC1), BC4](#bc1)è ideale per l'archiviazione di dati a virgola mobile nell'intervallo da 0 a 1 usando il formato DXGI FORMAT BC4 UNORM e da -1 a +1 usando il formato \[ \] \_ \_ \_ \[ \] DXGI \_ FORMAT \_ BC4 \_ SNORM. Supponendo una trama 4×4 con il formato di dati più grande possibile, questa tecnica di compressione riduce la memoria necessaria da 16 byte (16 colori × 1 componente/colore × 1 byte/componente) a 8 byte.

L'algoritmo funziona su 4×4 blocchi di texel. Anziché archiviare 16 colori, l'algoritmo archivia 2 colori di riferimento (rosso 0 e rosso 1) e indici di colori a \_ \_ 16 a 3 bit (da rosso a p rosso), come illustrato nel diagramma seguente.

![Diagramma del layout per la compressione bc4](images/d3d10-compression-bc4.png)

L'algoritmo usa gli indici a 3 bit per cercare i colori da una tabella dei colori che contiene 8 colori. I primi due colori, rosso \_ 0 e \_ rosso 1, sono i colori minimo e massimo. L'algoritmo calcola i colori rimanenti usando l'interpolazione lineare.

L'algoritmo determina il numero di valori di colore interpolati esaminando i due valori di riferimento. Se il rosso 0 è maggiore del rosso \_ \_ 1, BC4 interpola 6 valori di colore; in caso contrario, interpola 4. Quando BC4 interpola solo 4 valori di colore, imposta due valori di colore aggiuntivi (0,0f per completamente trasparente e 1,0f per l'opacità completa). BC4 comprime i valori alfa nell'area texel 4×4 archiviando il codice di bit corrispondente ai valori alfa interpolati che corrispondono maggiormente al valore alfa originale per un determinato texel.

-   [BC4 \_ UNORM](/windows)
-   [BC4 \_ SNORM](/windows)

### <a name="bc4_unorm"></a>BC4 \_ UNORM

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



Ai colori di riferimento vengono assegnati indici a 3 bit (da 000 a 111 perché sono presenti 8 valori), che verranno salvati in blocchi rosso da a a p rosso durante la compressione.

### <a name="bc4_snorm"></a>BC4 \_ SNORM

DXGI FORMAT BC4 SNORM è esattamente lo stesso, ad eccezione del fatto che i dati vengono codificati nell'intervallo SNORM e quando \_ \_ vengono \_ interpolati 4 valori di colore. L'interpolazione dei dati a componente singolo viene eseguita come nell'esempio di codice seguente.


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



Ai colori di riferimento vengono assegnati indici a 3 bit (da 000 a 111 perché sono presenti 8 valori), che verranno salvati in blocchi rosso da a a p rosso durante la compressione.

### <a name="bc5"></a>BC5

Usare il formato BC5 per archiviare i dati dei colori a due componenti usando 8 bit per ogni colore. A causa della maggiore accuratezza (rispetto a [BC1), BC5](#bc1)è ideale per l'archiviazione di dati a virgola mobile nell'intervallo da 0 a 1 usando il formato DXGI FORMAT BC5 UNORM e da -1 a +1 usando il formato \[ \] \_ \_ \_ \[ \] DXGI \_ FORMAT \_ BC5 \_ SNORM. Supponendo una trama 4×4 con il formato di dati più grande possibile, questa tecnica di compressione riduce la memoria necessaria da 32 byte (16 colori × 2 componenti/colore × 1 byte/componente) a 16 byte.

L'algoritmo funziona su 4×4 blocchi di texel. Anziché archiviare 16 colori per entrambi i componenti, l'algoritmo archivia 2 colori di riferimento per ogni componente (rosso \_ 0, rosso \_ 1, verde 0 e \_ verde 1) e 16 indici di colore a 3 bit per ogni componente (da rosso a p rosso e verde da a p verde), come illustrato nel \_ diagramma seguente.

![Diagramma del layout per la compressione bc5](images/d3d10-compression-bc5.png)

L'algoritmo usa gli indici a 3 bit per cercare i colori da una tabella dei colori che contiene 8 colori. I primi due colori, rosso 0 e rosso 1 (o verde 0 e \_ \_ verde \_ 1), sono i colori \_ minimo e massimo. L'algoritmo calcola i colori rimanenti usando l'interpolazione lineare.

L'algoritmo determina il numero di valori di colore interpolati esaminando i due valori di riferimento. Se il rosso 0 è maggiore del rosso \_ \_ 1, BC5 interpola 6 valori di colore; in caso contrario, interpola 4. Quando BC5 interpola solo 4 valori di colore, imposta i due valori di colore rimanenti su 0,0f e 1,0f.

-   [BC5 \_ UNORM](/windows)
-   [BC5 \_ SNORM](/windows)

### <a name="bc5_unorm"></a>BC5 \_ UNORM

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



Ai colori di riferimento vengono assegnati indici a 3 bit (da 000 a 111 perché sono presenti 8 valori), che verranno salvati in blocchi rosso da a a p rosso durante la compressione.

### <a name="bc5_snorm"></a>BC5 \_ SNORM

DXGI FORMAT BC5 SNORM è esattamente lo stesso, ad eccezione del fatto che i dati vengono codificati nell'intervallo SNORM e quando vengono interpolati 4 valori di dati, i due valori aggiuntivi sono \_ \_ \_ -1,0f e 1,0f. L'interpolazione dei dati a componente singolo viene eseguita come nell'esempio di codice seguente. I calcoli per i componenti verdi sono simili.


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



Ai colori di riferimento vengono assegnati indici a 3 bit (da 000 a 111 perché sono presenti 8 valori), che verranno salvati in blocchi rosso da a a p rosso durante la compressione.

## <a name="format-conversion-using-direct3d-101"></a>Conversione del formato con Direct3D 10.1

Direct3D 10.1 consente copie tra trame prestrutturate e trame compresse in blocchi con la stessa larghezza di bit. Le funzioni che possono eseguire questa operazione sono [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**CopySubresourceRegion.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)

A partire da Direct3D 10.1, è possibile usare [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) per copiare tra alcuni tipi di formato. Questo tipo di operazione di copia esegue un tipo di conversione del formato che reinterpreta i dati delle risorse come un tipo di formato diverso. Si consideri questo esempio che illustra la differenza tra la reinterpretazione dei dati con il comportamento di un tipo di conversione più tipico:


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



Per reinterpretare 'f' come tipo di 'u', usare [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



Nella reinterpretazione precedente, il valore sottostante dei dati non cambia; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterpreta il float come intero senza segno.

Per eseguire il tipo di conversione più tipico, usare l'assegnazione:


```
    u = f; // ‘u’ becomes 1.
```



Nella conversione precedente il valore sottostante dei dati cambia.

Nella tabella seguente sono elencati i formati di origine e di destinazione consentiti che è possibile utilizzare in questo tipo di reinterpretazione della conversione del formato. È necessario codificare correttamente i valori perché la reinterpretazione funzioni come previsto.



| Larghezza in bit | Risorsa non compressa                                                                                                                                               | Block-Compressed risorsa                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 32        | INTERFACCIA UTENTE DI DXGI \_ FORMAT \_ R32 \_<br/> FORMATO DXGI \_ \_ R32 \_ SINT<br/>                                                                                               | FORMATO DXGI \_ \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                   |
| 64        | FORMATO DXGI \_ \_ R16G16B16A16 \_ UINT<br/> FORMATO DXGI \_ \_ R16G16B16A16 \_ SINT<br/> FORMATO DXGI \_ \_ R32G32 \_ UINT<br/> FORMATO DXGI \_ \_ R32G32 \_ SINT<br/> | FORMATO DXGI \_ \_ BC1 \_ UNORM \[ \_ SRGB\]<br/> FORMATO DXGI \_ \_ BC4 \_ UNORM<br/> DXGI \_ FORMAT \_ BC4 \_ SNORM<br/>                                               |
| 128       | FORMATO DXGI \_ \_ R32G32B32A32 \_ UINT<br/> FORMATO DXGI \_ \_ R32G32B32A32 \_ SINT<br/>                                                                             | FORMATO DXGI \_ \_ BC2 \_ UNORM \[ \_ SRGB\]<br/> FORMATO DXGI \_ \_ BC3 \_ UNORM \[ \_ SRGB\]<br/> DXGI \_ FORMAT \_ BC5 \_ UNORM<br/> DXGI \_ FORMAT \_ BC5 \_ SNORM<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
