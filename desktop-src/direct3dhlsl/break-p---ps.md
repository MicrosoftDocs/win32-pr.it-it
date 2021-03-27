---
title: Breakp-PS
description: Suddividere in modo condizionale il ciclo corrente nel EndLoop-PS o endrep-PS più vicino. Usare uno dei componenti del registro predicato come condizione per determinare se eseguire o meno l'istruzione.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398255"
---
# <a name="breakp---ps"></a>Breakp-PS

Suddividere in modo condizionale il ciclo corrente nel [EndLoop-PS](endloop---ps.md) o [endrep-PS](endrep---ps.md)più vicino. Usare uno dei componenti del registro predicato come condizione per determinare se eseguire o meno l'istruzione.

## <a name="syntax"></a>Sintassi



| Breakp \[ ! \] P0. x|y|z|w |
|-----------------------------|



 

Dove:

-   \[!\] modificatore negazioni facoltativo.
-   P0 è il [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} è la replica obbligatoria swizzle su P0.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| breakp                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




