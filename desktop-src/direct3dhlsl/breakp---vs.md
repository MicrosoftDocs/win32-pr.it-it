---
title: breakp - vs
description: Interrompere in modo condizionale il ciclo corrente all'endloop più vicino , o endrep, rispetto a usare uno dei componenti del registro del predicato come condizione per determinare se eseguire o meno l'istruzione.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a768acaecaa77a42990b34c50cd8eccb24d61353550751f3ed830e7844d7624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794315"
---
# <a name="breakp---vs"></a>breakp - vs

Interrompere in modo condizionale il ciclo corrente [all'endloop](endloop---vs.md) più vicino , o [endrep, rispetto a](endrep---vs.md). Usare uno dei componenti del registro del predicato come condizione per determinare se eseguire o meno l'istruzione.

## <a name="syntax"></a>Sintassi



| breakp \[ ! \] p0. {x\|y\|z\|w} |
|-----------------------------|



 

Dove:

-   \[!\] valore booleano FACOLTATIVO NOT.
-   p0 è il registro del predicato. Vedere [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} è lo swizzle di replica richiesto in p0.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| breakp                 |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




