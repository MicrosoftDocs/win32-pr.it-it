---
description: Esistono due modi per codificare le mappe di trama che presentano una trasparenza più complessa.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Trame con canali alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c361b0335ef4f36b4efc9c90c71270e855f5db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104557200"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a>Trame con canali alfa (Direct3D 9)

Esistono due modi per codificare le mappe di trama che presentano una trasparenza più complessa. In ogni caso, un blocco che descrive la trasparenza precede il blocco a 64 bit già descritto. La trasparenza è rappresentata come bitmap 4x4 con 4 bit per pixel (codifica esplicita) o con meno bit e interpolazione lineare che è analoga a quella usata per la codifica dei colori.

Il blocco di trasparenza e il blocco di colore vengono disposti come illustrato nella tabella seguente.



| Indirizzo di Word | blocco a 64 bit                      |
|--------------|-----------------------------------|
| 3:0          | Blocco trasparenza                |
| 7:4          | Descritto in precedenza blocco a 64 bit |



 

## <a name="explicit-texture-encoding"></a>Codifica della trama esplicita

Per la codifica di trama esplicita (formati DXT2 e DXT3), i componenti alfa dei Texel che descrivono la trasparenza sono codificati in una bitmap 4x4 con 4 bit per Texel. Questi quattro bit possono essere realizzati attraverso diversi mezzi, ad esempio la rethering o l'utilizzo dei quattro bit più significativi dei dati alfa. Tuttavia, vengono usati così come sono, senza alcuna forma di interpolazione.

Il diagramma seguente illustra un blocco di trasparenza a 64 bit.

![diagramma di un blocco di trasparenza a 64 bit](images/colors4.png)

> [!Note]  
> Il metodo di compressione di Direct3D usa i quattro bit più significativi.

 

Le tabelle seguenti illustrano come le informazioni alfa sono disposte in memoria, per ogni parola a 16 bit.

Questa tabella contiene il layout per Word 0.



| BITS          | Alfa      |
|---------------|------------|
| 3:0 (LSB \* )   | \[0 \] \[ 0\] |
| 7:4           | \[0 \] \[ 1\] |
| 11:8          | \[0 \] \[ 2\] |
| 15:12 (MSB \* ) | \[0 \] \[ 3\] |



 

\*bit meno significativo, bit più significativo (MSB)

Questa tabella contiene il layout per Word 1.



| BITS        | Alfa      |
|-------------|------------|
| 3:0 (LSB)   | \[1 \] \[ 0\] |
| 7:4         | \[1 \] \[ 1\] |
| 11:8        | \[1 \] \[ 2\] |
| 15:12 (MSB) | \[1 \] \[ 3\] |



 

Questa tabella contiene il layout per Word 2.



| BITS        | Alfa      |
|-------------|------------|
| 3:0 (LSB)   | \[2 \] \[ 0\] |
| 7:4         | \[2 \] \[ 1\] |
| 11:8        | \[2 \] \[ 2\] |
| 15:12 (MSB) | \[2 \] \[ 3\] |



 

Questa tabella contiene il layout per Word 3.



| BITS        | Alfa      |
|-------------|------------|
| 3:0 (LSB)   | \[3 \] \[ 0\] |
| 7:4         | \[3 \] \[ 1\] |
| 11:8        | \[3 \] \[ 2\] |
| 15:12 (MSB) | \[3 \] \[ 3\] |



 

La differenza tra DXT2 e DXT3 consiste nel fatto che, nel formato DXT2, si presuppone che i dati relativi ai colori siano stati premoltiplicati da Alpha. Nel formato DXT3 si presuppone che il colore non sia premoltiplicato da Alpha. Questi due formati sono necessari perché, nella maggior parte dei casi, nel momento in cui viene utilizzata una trama, solo l'analisi dei dati non è sufficiente per determinare se i valori dei colori sono stati moltiplicati per alfa. Poiché queste informazioni sono necessarie in fase di esecuzione, per distinguere questi casi vengono usati i due codici FOURCC. Tuttavia, i dati e il metodo di interpolazione usati per questi due formati sono identici.

Il confronto dei colori usato in DXT1 per determinare se il Texel è trasparente non viene usato in questo formato. Si presuppone che senza il confronto dei colori i dati del colore vengano sempre considerati come se fossero in modalità a 4 colori. In altre parole, l'istruzione If all'inizio del codice DXT1 dovrebbe essere la seguente:


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a>Interpolazione alfa lineare Three-Bit

La codifica della trasparenza per i formati DXT4 e DXT5 si basa su un concetto simile alla codifica lineare utilizzata per il colore. I valori alfa a 2 8 bit e una bitmap 4x4 con tre bit per pixel vengono archiviati nei primi otto byte del blocco. I valori alfa rappresentativi vengono utilizzati per interpolare i valori alfa intermedi. Ulteriori informazioni sono disponibili nel modo in cui vengono archiviati i due valori alfa. Se alfa \_ 0 è maggiore di alfa \_ 1, verranno creati sei valori alfa intermedi dall'interpolazione. In caso contrario, vengono interpolati quattro valori alfa intermedi tra gli estremi alfa specificati. I due valori alfa impliciti aggiuntivi sono 0 (completamente trasparente) e 255 (completamente opaco).

Nell'esempio di codice riportato di seguito viene illustrato questo algoritmo.


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
| 2    | \[0 \] \[ 2 \] (2 MSBs), \[ 0 \] \[ 1 \] , \[ 0 \] \[ 0\]                    |
| 3    | \[1 \] \[ 1 \] (1 MSB), \[ 1 \] \[ 0 \] , \[ 0 \] \[ 3 \] , \[ 0 \] \[ 2 \] (1 LSB) |
| 4    | \[1 \] \[ 3 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 1 \] (2 LSB)                    |
| 5    | \[2 \] \[ 2 \] (2 MSBs), \[ 2 \] \[ 1 \] , \[ 2 \] \[ 0\]                    |
| 6    | \[3 \] \[ 1 \] (1 MSB), \[ 3 \] \[ 0 \] , \[ 2 \] \[ 3 \] , \[ 2 \] \[ 2 \] (1 LSB) |
| 7    | \[3 \] \[ 3 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 1 \] (2 LSB)                    |



 

La differenza tra DXT4 e DXT5 è che nel formato DXT4 si presuppone che i dati dei colori siano stati premoltiplicati da Alpha. Nel formato DXT5 si presuppone che il colore non sia premoltiplicato da Alpha. Questi due formati sono necessari perché, nella maggior parte dei casi, nel momento in cui viene utilizzata una trama, solo l'analisi dei dati non è sufficiente per determinare se i valori dei colori sono stati moltiplicati per alfa. Poiché queste informazioni sono necessarie in fase di esecuzione, per distinguere questi casi vengono usati i due codici FOURCC. Tuttavia, i dati e il metodo di interpolazione usati per questi due formati sono identici.

Il confronto dei colori usato in DXT1 per determinare se il Texel è trasparente non viene usato con questi formati. Si presuppone che senza il confronto dei colori i dati del colore vengano sempre considerati come se fossero in modalità a 4 colori. In altre parole, l'istruzione If all'inizio del codice DXT1 deve essere:


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse di trama compresse](compressed-texture-resources.md)
</dt> </dl>

 

 



