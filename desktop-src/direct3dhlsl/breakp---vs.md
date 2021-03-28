---
title: Breakp-vs
description: Suddividere in modo condizionale il ciclo corrente al più vicino EndLoop-vs o endrep-vs. utilizzare uno dei componenti del registro predicato come condizione per determinare se eseguire o meno l'istruzione.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046086"
---
# <a name="breakp---vs"></a>Breakp-vs

Suddividere in modo condizionale il ciclo corrente nel [EndLoop-vs](endloop---vs.md) o [endrep-vs](endrep---vs.md)più vicino. Usare uno dei componenti del registro predicato come condizione per determinare se eseguire o meno l'istruzione.

## <a name="syntax"></a>Sintassi



| Breakp \[ ! \] P0. x|y|z|w |
|-----------------------------|



 

Dove:

-   \[!\] valore booleano facoltativo NOT.
-   P0 è il registro predicato. Vedere [registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} è la replica obbligatoria swizzle su P0.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| breakp                 |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




