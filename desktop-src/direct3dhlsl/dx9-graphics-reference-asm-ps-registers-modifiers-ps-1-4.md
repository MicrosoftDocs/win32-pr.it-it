---
title: ps \_ 1 \_ 4 modificatori del registro di origine per texld, texcrd
description: Due pixel shader versione 1 4 dell'indirizzo di \_ trama, texld - ps \_ \_ 1 4 e texcrd - ps, hanno una sintassi personalizzata.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 63a0cfd212767a0219af83d734d3562edacc84901098afcf77c786d8895f32d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512877"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a>ps \_ 1 \_ 4 modificatori del registro di origine per texld, texcrd

Due pixel shader 1 4 istruzioni sull'indirizzo di \_ trama, [texld - ps \_ \_ 1 4](texld---ps-1-4.md) e [texcrd - ps](texcrd---ps.md), hanno una sintassi personalizzata. Queste istruzioni supportano il proprio set di modificatori del registro di origine, selettori del registro di origine e maschere di scrittura del registro di destinazione, come illustrato di seguito.

## <a name="source-register-modifiers-for-texld-and-texcrd"></a>Modificatori del registro di origine per texld e texcrd

Questi modificatori forniscono funzionalità di divisione proiettativa dividendo i valori x e y per i valori z o w.



| Modificatori del registro di origine | Descrizione                | Sintassi       |
|---------------------------|----------------------------|--------------|
| \_Dz                      | Dividere i componenti x,y per z | register \_ dz |
| \_db                      | Dividere i componenti x,y per z | register \_ db |
| \_dw                      | Dividere i componenti x,y per w | register \_ dw |
| \_da                      | Dividere i componenti x,y per w | register \_ da |



 

### <a name="remarks"></a>Commenti

Il \_ modificatore dz o \_ db esegue le operazioni seguenti:


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



Il \_ modificatore dw \_ o da esegue le operazioni seguenti:


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




