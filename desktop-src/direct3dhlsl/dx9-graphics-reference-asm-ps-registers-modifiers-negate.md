---
title: Negazione registro di origine
description: Esegue un negazione (y -x) su tutti i componenti del registro.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94898dbbf193254165850ee696d2fea72d6d446908021dfbb5fd32f1920b7010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512952"
---
# <a name="source-register-negate"></a>Negazione registro di origine

Esegue una negazione (y = -x) su tutti i componenti del registro.

## <a name="syntax"></a>Sintassi


```
- register
```



## <a name="registers"></a>Registri

Registro di origine. Per altre informazioni sui tipi di registro, vedere [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Commenti

Il contenuto del registro non viene modificato. Il modificatore viene applicato solo ai dati letti dal registro. L'operazione di negazione viene applicata a tutti e quattro i canali di colore (RGBA).

Questa operazione viene eseguita dopo qualsiasi altro modificatore presente nello stesso argomento.

Questo modificatore si escludono a [vicenda con Source Register Invert,](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) quindi non può essere applicato allo stesso registro.

Questo modificatore può essere utilizzato solo con istruzioni aritmetiche.

## <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato come usare questo modificatore.


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




