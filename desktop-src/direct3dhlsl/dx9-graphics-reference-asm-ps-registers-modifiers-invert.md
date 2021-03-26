---
title: Inverti registro di origine
description: Esegue un calcolo (valore 1) per ogni canale del registro specificato.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976167"
---
# <a name="source-register-invert"></a>Inverti registro di origine

Esegue un calcolo (valore 1) per ogni canale del registro specificato.

## <a name="syntax"></a>Sintassi


```
1 - register
```



## <a name="registers"></a>Registri

Registro di origine. Per altre informazioni sui tipi di registro, vedere la pagina relativa ai registri PS 1 [ \_ \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS 1 \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Commenti

Il contenuto del registro non è stato modificato. Il modificatore viene applicato solo ai dati letti dal registro. L'operazione di inversione viene applicata a tutti e quattro i canali di colore (RGBA).

Questo modificatore può essere utilizzato solo con istruzioni aritmetiche. Inoltre, questo modificatore non può essere combinato con l'altra [maschera di scrittura del registro di destinazione](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).

## <a name="example"></a>Esempio

Questo esempio USA Inversion per generare il complemento del registro R1.


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




