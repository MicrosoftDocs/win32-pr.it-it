---
title: Registro delle coordinate di trama (riferimento di HLSL VS)
description: Questo registro di output del vertex shader contiene coordinate di trama per vertice.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118355"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a>Registro delle coordinate di trama (riferimento di HLSL VS)

Questo registro di output del vertex shader contiene coordinate di trama per vertice.

Un registro è costituito da proprietà che determinano il comportamento di ogni registro.



| Proprietà        | Descrizione   |
|-----------------|---------------|
| Nome            | oT0 - oT7     |
| Conteggio           | Otto vettori |
| Autorizzazioni di I/O | Sola scrittura    |



 

I registri delle coordinate di trama di output sono una matrice di registri di dati di output. I dati del registro vengono iterati e usati come coordinate di trama dalle fasi di campionamento della trama per fornire i dati al pixel shader.

Quando si scrive in un registro delle coordinate di trama, si consiglia di passare solo il numero di valori a virgola mobile della dimensione della mappa di trama corrispondente. Controllare i valori passati con un modificatore. Ad esempio, usare. XY per una mappa di trama 2D.

I flag della pipeline dei vertici della funzione fissa, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF COUNT2, D3DTTFF COUNT3 \_ \_ , D3DTTFF \_ COUNT4), devono essere impostati su zero se si utilizza un vertex shader programmabile.

I dati dei vertici degli oggetti forniscono coordinate di trama di input. Per gli oggetti che non utilizzano trame affiancate sono in genere presenti coordinate di trama nell'intervallo compreso tra \[ 0 e 1 \] . Gli oggetti che utilizzano trame affiancate, ad esempio il terreno, in genere presentano coordinate di trama che variano da \[ -n, + n \] dove n può essere qualsiasi numero a virgola mobile.

L'interpolazione delle coordinate di trama viene eseguita sui dati dei vertici per la rasterizzazione. Durante la rasterizzazione, le coordinate di trama vengono interpolate tra i vertici degli oggetti, modificati dal wrapping della trama e ridimensionate in base alle dimensioni della trama (tenendo conto delle modalità di indirizzamento della trama) per produrre un indice Integer. L'indice viene quindi utilizzato per eseguire una ricerca di trama. Usare il valore MaxTextureRepeat in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) per determinare il numero di volte in cui una trama può essere affiancata.

## <a name="example"></a>Esempio

Dichiarare il registro delle coordinate di trama.


```
dcl_texcoord v7
```



Copiare le coordinate di trama per vertice nel registro di output.


```
mov oT0, v7
```





| Versioni vertex shader      | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------------|------|------|-------|------|------|-------|
| Registro coordinate trama | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 