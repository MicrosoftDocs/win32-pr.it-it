---
title: exp-PS
description: Fornisce un 2x esponenziale a precisione completa. | exp-PS
ms.assetid: 09e4446f-4149-4ec8-b3e3-2045b55bd591
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acd7c50c1f0d6ff08ee5d66e50fdd3e56939f0d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058508"
---
# <a name="exp---ps"></a>exp-PS

Fornisce la precisione completa esponenziale 2<sup>x</sup>.

## <a name="syntax"></a>Sintassi



| exp DST, src |
|--------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito di swizzle replicate; ovvero, è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a). Vedere il [Registro di origine swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| exp                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Il frammento di codice seguente mostra le operazioni eseguite:


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




