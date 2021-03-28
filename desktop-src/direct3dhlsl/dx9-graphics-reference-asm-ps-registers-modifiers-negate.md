---
title: Negazione registro di origine
description: Esegue una negazione (y-x) su tutti i componenti del registro.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044604"
---
# <a name="source-register-negate"></a>Negazione registro di origine

Esegue una negazione (y =-x) su tutti i componenti del registro.

## <a name="syntax"></a>Sintassi


```
- register
```



## <a name="registers"></a>Registri

Registro di origine. Per altre informazioni sui tipi di registro, vedere la pagina relativa ai registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Commenti

Il contenuto del registro non è stato modificato. Il modificatore viene applicato solo ai dati letti dal registro. L'operazione di negazione viene applicata a tutti e quattro i canali di colore (RGBA).

Questa operazione viene eseguita dopo tutti gli altri modificatori presenti nello stesso argomento.

Questo modificatore si escludono a vicenda con l' [inversione del registro di origine](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) in modo che non possa essere applicato allo stesso registro.

Questo modificatore viene utilizzato solo con istruzioni aritmetiche.

## <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato come utilizzare questo modificatore.


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




