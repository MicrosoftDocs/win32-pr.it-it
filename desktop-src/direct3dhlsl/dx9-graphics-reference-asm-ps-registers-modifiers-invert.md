---
title: Inversione del registro di origine
description: Esegue un calcolo (1 - valore) per ogni canale del registro specificato.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a391219f085c18a4c8bf2925a248800b6a26838cc6e2b8556551eb98b5335241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562771"
---
# <a name="source-register-invert"></a>Inversione del registro di origine

Esegue un calcolo (1 - valore) per ogni canale del registro specificato.

## <a name="syntax"></a>Sintassi


```
1 - register
```



## <a name="registers"></a>Registri

Registro di origine. Per altre informazioni sui tipi di registro, vedere [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Commenti

Il contenuto del registro non viene modificato. Il modificatore viene applicato solo ai dati letti dal registro. L'operazione di inversione viene applicata a tutti e quattro i canali di colore (RGBA).

Questo modificatore può essere usato solo con istruzioni aritmetiche. Inoltre, questo modificatore non può essere combinato con l'altra [maschera di scrittura del registro di destinazione.](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)

## <a name="example"></a>Esempio

In questo esempio viene utilizzata l'inversione per generare il complemento del registro r1.


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




