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
ms.openlocfilehash: e4a0b397d17b841877796bd9c33432896208ed6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992752"
---
# <a name="output-registers"></a>Registri di output

-   Registro colori vertici
-   Registro di nebbia
-   Posizione \_ Registro
-   \_Registro dimensioni \_ punti
-   \_Registro coordinate \_ trama

I nomi dei registri sono preceduti da una lettera minuscola o, a indicare che i registri di output sono di sola scrittura.

## <a name="vertex-color-register---od0-od1"></a>Registro colori vertici-oD0, oD1

oD0 è il registro colori diffuso. oD1 è il registro colore speculare. Il valore oD0 viene interpolato e viene scritto nel registro colore di input 0 (V0) del pixel shader. Il valore oD1 viene interpolato e scritto nel registro colori di input 1 (V1) del pixel shader. Per ulteriori informazioni sui registri dei colori pixel shader, vedere registri.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro colori vertici  | x    | x    | x     | x    |      |       |



 

## <a name="fog-register---ofog"></a>Registro di nebbia-oFog

Il valore di nebbia di output viene registrato. Il valore è il fattore di nebbia da interpolare e quindi indirizzato alla tabella Fog. Viene utilizzato solo il componente x scalare della nebbia. I valori vengono fissati tra zero e uno prima del passaggio al rasterizzatore.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro di nebbia           | x    | x    | x     | x    |      |       |



 

## <a name="position-register---opos"></a>Posizione Register-oPos

La posizione di output viene registrata. Il valore è la posizione nello spazio di ritaglio omogeneo. Questo valore deve essere scritto dal vertex shader.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Posizione registro      | x    | x    | x     | x    |      |       |



 

## <a name="point-size-register---opts"></a>Registro dimensioni punti-opz

Registri delle dimensioni del punto di output. Viene utilizzato solo il componente x scalare della dimensione del punto.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro dimensioni punti    | x    | x    | x     | x    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a>Registro delle coordinate di trama-oT0 in oT7

Le coordinate di trama di output vengono registrate. In particolare, si tratta di una matrice di registri di dati di output che vengono iterati e usati come coordinate di trama in base alle fasi di campionamento della trama che indirizzano i dati al pixel shader.



| Versioni vertex shader      | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------------|------|------|-------|------|------|-------|
| Registro coordinate trama | x    | x    | x     | x    |      |       |



 

Quando si scrive in un registro delle coordinate di trama, è consigliabile passare solo il numero di valori a virgola mobile della dimensione della mappa di trama corrispondente. Controllare i valori passati con un modificatore. Ad esempio, usare. XY per una mappa di trama 2D.

Quando è abilitata la proiezione di trama per una fase di trama, è necessario scrivere tutti i quattro valori a virgola mobile nel registro di trama corrispondente.

\*Quando si usa la pipeline programmabile, i flag di trasformazione della trama D3DTTFF devono essere pari a zero.

### <a name="texture-coordinate-range"></a>Intervallo di coordinate di trama

I dati dei vertici degli oggetti forniscono coordinate di trama di input. Per gli oggetti che non utilizzano trame affiancate sono in genere presenti coordinate di trama nell'intervallo compreso tra \[ 0 e 1 \] . Gli oggetti che utilizzano trame affiancate, ad esempio il terreno, presentano in genere coordinate di trama che variano da \[ -?, +? \] dove? può essere un numero a virgola mobile di grandi dimensioni.

L'interpolazione delle coordinate di trama viene eseguita sui dati dei vertici per la rasterizzazione. Durante la rasterizzazione, le coordinate di trama vengono interpolate tra i vertici degli oggetti, modificati dal wrapping della trama e ridimensionati in base alle dimensioni della trama (tenendo conto della modalità di indirizzamento della trama) per produrre un indice Integer. L'indice viene quindi utilizzato per eseguire una ricerca di trama. È possibile utilizzare MaxTextureRepeat per determinare il numero di volte in cui una trama può essere affiancata.

Se le coordinate di trama vengono lette direttamente in un pixel shader (usando TEXCOORD o texcrd), l'intervallo delle coordinate di trama dipende dall'istruzione e dalla versione pixel shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




