---
title: Scala del registro di origine x 2
description: Moltiplicare il valore per due prima di utilizzarlo nell'istruzione.
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976162"
---
# <a name="source-register-scale-x-2"></a>Scala del registro di origine x 2

Moltiplicare il valore per due prima di utilizzarlo nell'istruzione.

## <a name="syntax"></a>Sintassi


```
register_x2
```



## <a name="register"></a>Registrazione

Registro di origine. Per altre informazioni sui tipi di registro, vedere la pagina relativa ai registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Commenti

Il contenuto del registro non è stato modificato. Il modificatore viene applicato solo ai dati letti dal registro.

Questo modificatore si escludono a vicenda con il [Registro di origine invertito](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), pertanto non può essere applicato allo stesso registro.

Questo modificatore è disponibile solo per le istruzioni aritmetiche nella versione 1 \_ 4.

## <a name="example"></a>Esempio

In questo esempio viene campionata una trama, i dati vengono convertiti nell'intervallo compreso tra-1 e + 1 e viene calcolato un prodotto punto.


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




