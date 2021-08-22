---
title: Registro coordinate trama (informazioni di riferimento su HLSL VS)
description: Questo registro di output vertex shader contiene coordinate di trama per vertice.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e695765d57c7e74c94fe0605ca7ec7b96705d7b37d1dc24cad068a5aed6a2ca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457761"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a>Registro coordinate trama (informazioni di riferimento su HLSL VS)

Questo registro di output vertex shader contiene coordinate di trama per vertice.

Un registro è costituito da proprietà che determinano il comportamento di ogni registro.



| Proprietà        | Descrizione   |
|-----------------|---------------|
| Nome            | oT0 - oT7     |
| Conteggio           | Otto vettori |
| Autorizzazioni di I/O | Sola scrittura    |



 

I registri delle coordinate della trama di output sono una matrice di registri dati di output. I dati del registro vengono iterati e usati come coordinate di trama dalle fasi di campionamento delle trame per fornire dati al pixel shader.

Quando si scrive in un registro delle coordinate di trama, è consigliabile passare solo il numero di valori a virgola mobile della dimensione della mappa di trama corrispondente. Controllare i valori passati con un modificatore . Ad esempio, usare .xy per una mappa trame 2D.

I flag della pipeline dei vertici delle funzioni fisse, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3, D3DTTFF COUNT4), devono essere impostati su zero se si usa \_ un vertex shader programmabile.

I dati dei vertici dell'oggetto specificano le coordinate della trama di input. Gli oggetti che non usano trame affiancate hanno in genere coordinate di trama nell'intervallo \[ 0,1. \] Gli oggetti che usano trame affiancate, ad esempio terreno, hanno in genere coordinate di trama che vanno da \[ -n,+n \] dove n può essere qualsiasi numero a virgola mobile.

L'interpolazione delle coordinate della trama viene eseguita sui dati dei vertici per la rasterizzazione. Durante la rasterizzazione, le coordinate della trama vengono interpolate tra i vertici dell'oggetto, modificate dalla disposizione della trama e ridimensionate in base alle dimensioni della trama (tenendo conto anche delle modalità di indirizzamento della trama) per produrre un indice integer. L'indice viene quindi usato per eseguire una ricerca trame. Usare il valore MaxTextureRepeat in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) per determinare quante volte è possibile affiancare una trama.

## <a name="example"></a>Esempio

Dichiarare il registro delle coordinate della trama.


```
dcl_texcoord v7
```



Copiare le coordinate della trama per vertice nel registro di output.


```
mov oT0, v7
```





| Versioni di vertex shader      | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------------|------|------|-------|------|------|-------|
| Registro delle coordinate della trama | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 