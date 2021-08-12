---
description: Esistono due modi per codificare le mappe trame che presentano trasparenza più complessa.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Trame con canali alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 934660a62c0257de1549ccec09f9bb77e5c02c4c22baf1e1dc9cc8dffef03f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290527"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a>Trame con canali alfa (Direct3D 9)

Esistono due modi per codificare le mappe trame che presentano trasparenza più complessa. In ogni caso, un blocco che descrive la trasparenza precede il blocco a 64 bit già descritto. La trasparenza è rappresentata come bitmap 4x4 con 4 bit per pixel (codifica esplicita) o con meno bit e interpolazione lineare analoga a quella usata per la codifica dei colori.

Il blocco di trasparenza e il blocco di colori vengono disposti come illustrato nella tabella seguente.



| Indirizzo di Word | Blocco a 64 bit                      |
|--------------|-----------------------------------|
| 3:0          | Blocco di trasparenza                |
| 7:4          | Blocco a 64 bit descritto in precedenza |



 

## <a name="explicit-texture-encoding"></a>Codifica esplicita delle trame

Per la codifica esplicita delle trame (formati DXT2 e DXT3), i componenti alfa dei texel che descrivono la trasparenza vengono codificati in una bitmap 4x4 con 4 bit per texel. Questi quattro bit possono essere ottenuti in diversi modi, ad esempio il dithering o usando i quattro bit più significativi dei dati alfa. Tuttavia, vengono prodotti, vengono usati così come sono, senza alcuna forma di interpolazione.

Il diagramma seguente mostra un blocco di trasparenza a 64 bit.

![diagramma di un blocco di trasparenza a 64 bit](images/colors4.png)

> [!Note]  
> Il metodo di compressione di Direct3D usa i quattro bit più significativi.

 

Le tabelle seguenti illustrano il modo in cui le informazioni alfa vengono disposte in memoria, per ogni parola a 16 bit.

Questa tabella contiene il layout per la parola 0.



| BITS          | Alfa      |
|---------------|------------|
| 3:0 (LSB \* )   | \[0 \] \[ 0\] |
| 7:4           | \[0 \] \[ 1\] |
| 11:8          | \[0 \] \[ 2\] |
| 15:12 (MSB \* ) | \[0 \] \[ 3\] |



 

\*bit meno significativo, bit più significativo (MSB)

Questa tabella contiene il layout per la parola 1.



| BITS        | Alfa      |
|-------------|------------|
| 3:0 (LSB)   | \[1 \] \[ 0\] |
| 7:4         | \[1 \] \[ 1\] |
| 11:8        | \[1 \] \[ 2\] |
| 15:12 (MSB) | \[1 \] \[ 3\] |



 

Questa tabella contiene il layout per la parola 2.



| BITS        | Alfa      |
|-------------|------------|
| 3:0 (LSB)   | \[2 \] \[ 0\] |
| 7:4         | \[2 \] \[ 1\] |
| 11:8        | \[2 \] \[ 2\] |
| 15:12 (MSB) | \[2 \] \[ 3\] |



 

Questa tabella contiene il layout per la parola 3.



| BITS        | Alfa      |
|-------------|------------|
| 3:0 (LSB)   | \[3 \] \[ 0\] |
| 7:4         | \[3 \] \[ 1\] |
| 11:8        | \[3 \] \[ 2\] |
| 15:12 (MSB) | \[3 \] \[ 3\] |



 

La differenza tra DXT2 e DXT3 è che, nel formato DXT2, si presuppone che i dati di colore siano stati premoltimulati da alfa. Nel formato DXT3 si presuppone che il colore non sia premoltimulato da alfa. Questi due formati sono necessari perché, nella maggior parte dei casi, quando viene usata una trama, la semplice analisi dei dati non è sufficiente per determinare se i valori dei colori sono stati moltiplicati per alfa. Poiché queste informazioni sono necessarie in fase di esecuzione, i due codici FOURCC vengono usati per distinguere questi casi. Tuttavia, i dati e il metodo di interpolazione usati per questi due formati sono identici.

Il confronto colori usato in DXT1 per determinare se il texel è trasparente non viene usato in questo formato. Si presuppone che senza il confronto dei colori i dati dei colori siano sempre trattati come se si tratta di una modalità a 4 colori. In altre parole, l'istruzione if all'inizio del codice DXT1 deve essere la seguente:


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a>Three-Bit interpolazione alfa lineare

La codifica della trasparenza per i formati DXT4 e DXT5 si basa su un concetto simile alla codifica lineare usata per il colore. Due valori alfa a 8 bit e una bitmap 4x4 con tre bit per pixel vengono archiviati nei primi otto byte del blocco . I valori alfa rappresentativi vengono usati per interpolare i valori alfa intermedi. Sono disponibili informazioni aggiuntive sulla modalità di archiviazione dei due valori alfa. Se alpha \_ 0 è maggiore di alpha 1, vengono creati sei valori alfa intermedi \_ dall'interpolazione. In caso contrario, quattro valori alfa intermedi vengono interpolati tra gli estremi alfa specificati. I due valori alfa impliciti aggiuntivi sono 0 (completamente trasparente) e 255 (completamente opaco).

L'esempio di codice seguente illustra questo algoritmo.


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



Il layout di memoria del blocco alfa è il seguente:



| Byte | Alfa                                                          |
|------|----------------------------------------------------------------|
| 0    | Alfa \_ 0                                                       |
| 1    | Alfa \_ 1                                                       |
| 2    | \[0 \] \[ 2 \] (2 MSB), \[ 0 \] \[ 1 \] , \[ 0 \] \[ 0\]                    |
| 3    | \[1 \] \[ 1 \] (1 MSB), \[ 1 \] \[ 0 \] , \[ 0 \] \[ 3 \] , \[ 0 \] \[ 2 \] (1 LSB) |
| 4    | \[1 \] \[ 3 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 1 \] (2 LSB)                    |
| 5    | \[2 \] \[ 2 \] (2 MSB), \[ 2 \] \[ \] 1, \[ 2 \] \[ 0\]                    |
| 6    | \[3 \] \[ 1 \] (1 MSB), \[ 3 \] \[ 0 \] , \[ 2 \] \[ 3 \] , \[ 2 \] \[ 2 \] (1 LSB) |
| 7    | \[3 \] \[ 3 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 1 \] (2 LSB)                    |



 

La differenza tra DXT4 e DXT5 è che nel formato DXT4 si presuppone che i dati di colore siano stati premoltimulati da alfa. Nel formato DXT5 si presuppone che il colore non sia premoltimulato da alfa. Questi due formati sono necessari perché, nella maggior parte dei casi, quando viene usata una trama, la semplice analisi dei dati non è sufficiente per determinare se i valori dei colori sono stati moltiplicati per alfa. Poiché queste informazioni sono necessarie in fase di esecuzione, i due codici FOURCC vengono usati per distinguere questi casi. Tuttavia, i dati e il metodo di interpolazione usati per questi due formati sono identici.

Il confronto colori usato in DXT1 per determinare se il texel è trasparente non viene usato con questi formati. Si presuppone che senza il confronto dei colori i dati dei colori siano sempre trattati come se si tratta di una modalità a 4 colori. In altre parole, l'istruzione if all'inizio del codice DXT1 deve essere:


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse di trama compresse](compressed-texture-resources.md)
</dt> </dl>

 

 



