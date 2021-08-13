---
title: Registri di output
description: Registri di output
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cfa17c09315f4cdca98f5c5fc10f7ab15541eb8b774835963b06169c4afe225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457771"
---
# <a name="output-registers"></a>Registri di output

-   Registro colori vertice
-   Registro Di Taschia
-   Registro \_ delle posizioni
-   Registro \_ dimensioni \_ punto
-   Registro \_ delle coordinate della \_ trama

I nomi dei registri sono preceduti da una lettera minuscola o, a indicare che i registri di output sono di sola scrittura.

## <a name="vertex-color-register---od0-od1"></a>Registro colori vertice - oD0, oD1

oD0 è il registro colori diffuso. oD1 è il registro colori speculare. Il valore oD0 è interpolato e viene scritto nel registro colori di input 0 (v0) del pixel shader. Il valore oD1 viene interpolato e scritto nel registro colori di input 1 (v1) del pixel shader. Per altre informazioni sui pixel shader colori, vedere Registri.



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro colori vertice  | x    | x    | x     | x    |      |       |



 

## <a name="fog-register---ofog"></a>Registro Di Taschia - oFog

Il valore di nebbia di output viene registrato. Il valore è il fattore di nebbia da interpolare e quindi instradare alla tabella della nebbia. Viene usato solo il componente x scalare della nebbia. I valori sono compresi tra zero e uno prima di passare al rasterizzatore.



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro Di Taschia           | x    | x    | x     | x    |      |       |



 

## <a name="position-register---opos"></a>Registro di posizione - oPos

La posizione di output viene registrato. Il valore è la posizione nello spazio di ritaglio omogeneo. Questo valore deve essere scritto dal vertex shader.



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro delle posizioni      | x    | x    | x     | x    |      |       |



 

## <a name="point-size-register---opts"></a>Registro dimensioni punto - oPts

Registri delle dimensioni del punto di output. Viene usato solo il componente x scalare delle dimensioni in punti.



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro dimensioni punto    | x    | x    | x     | x    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a>Registro coordinate trama - da oT0 a oT7

Le coordinate della trama di output vengono registrate. In particolare, si tratta di una matrice di registri dati di output che vengono iterati e usati come coordinate di trama dalle fasi di campionamento trame instradando i dati al pixel shader.



| Versioni di vertex shader      | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------------|------|------|-------|------|------|-------|
| Registro delle coordinate della trama | x    | x    | x     | x    |      |       |



 

Quando si scrive in un registro delle coordinate della trama, è consigliabile passare solo il numero di valori a virgola mobile della dimensione della mappa trame corrispondente. Controllare i valori passati con un modificatore . Ad esempio, usare .xy per una mappa trame 2D.

Quando la proiezione trame è abilitata per una fase di trama, tutti e quattro i valori a virgola mobile devono essere scritti nel registro trame corrispondente.

Uno dei flag di trasformazione della trama D3DTTFF deve essere zero quando viene usata la \* pipeline programmabile.

### <a name="texture-coordinate-range"></a>Intervallo di coordinate trama

I dati dei vertici dell'oggetto specificano le coordinate della trama di input. Gli oggetti che non usano trame affiancate hanno in genere coordinate di trama nell'intervallo \[ 0,1. \] Gli oggetti che usano trame affiancate, ad esempio terreno, hanno in genere coordinate di trama che vanno \[ da -?,+? \] dove ? può essere un numero a virgola mobile di grandi dimensioni.

L'interpolazione delle coordinate di trama viene eseguita sui dati dei vertici per la rasterizzazione. Durante la rasterizzazione, le coordinate della trama vengono interpolate tra i vertici degli oggetti, modificate dal wrapping della trama e ridimensionate in base alle dimensioni della trama (tenendo conto anche della modalità di indirizzo della trama) per produrre un indice integer. L'indice viene quindi usato per eseguire una ricerca di trame. MaxTextureRepeat può essere usato per determinare quante volte è possibile affiancare una trama.

Se le coordinate della trama vengono lette direttamente in un pixel shader (usando texcoord o texcrd), l'intervallo di coordinate della trama dipende dall'istruzione e dalla pixel shader versione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




