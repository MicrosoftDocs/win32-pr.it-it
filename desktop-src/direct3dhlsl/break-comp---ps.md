---
title: break_comp - ps
description: Uscire dal ciclo corrente all'endloop più vicino - ps o endrep - ps, in base a un confronto per componente.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fa79b7aa50bc734ddc1f9fb1fd54e4130c48518dd47ed429b4177b8fb867d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794459"
---
# <a name="break_comp---ps"></a>break \_ comp - ps

Uscire dal ciclo corrente [all'endloop più](endloop---ps.md) vicino - ps o [endrep - ps](endrep---ps.md), in base a un confronto per componente.

## <a name="syntax"></a>Sintassi



| break \_ comp src0, src1 |
|------------------------|



 

Dove:

-   \_comp è un confronto scalare (o singolo) tra i due registri di origine. I possibili valori sono i seguenti: 

    | Sintassi | Confronto            |
    |--------|-----------------------|
    | \_Gt   | Maggiore di          |
    | \_Tenente   | Minore di             |
    | \_Ge   | Maggiore o uguale a |
    | \_le   | Minore o uguale a    |
    | \_Eq   | Uguale a              |
    | \_ne   | Diverso da          |

    

     

-   src0 è un registro di origine. Replicare lo swizzle è obbligatorio se si seleziona un singolo componente.
-   src1 è un registro di origine. Replicare lo swizzle è obbligatorio se si seleziona un singolo componente.

## <a name="remarks"></a>Commenti

Questa istruzione è supportata nelle versioni seguenti.



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| interrompere \_ la compilazione           |      |      |      |      |      | x    | x     | x    | x     |



 

Quando il confronto è true, esce dal ciclo corrente, come illustrato.


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




