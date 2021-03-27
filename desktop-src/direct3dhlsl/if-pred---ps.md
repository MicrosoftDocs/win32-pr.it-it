---
title: Se prede-PS
description: Inizio di un if bool-PS... else-PS... il blocco endif-PS, con la condizione ricavata dal contenuto del registro predicato.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719375"
---
# <a name="if-pred---ps"></a>Se prede-PS

Inizio di un [if bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... il blocco [endif-PS](endif---ps.md) , con la condizione ricavata dal contenuto del registro predicato.

## <a name="syntax"></a>Sintassi



| Se \[ ! \] prede. replicateSwizzle |
|-------------------------------|



 

Dove:

-   \[!\] è un modificatore facoltativo NOT. Il valore viene modificato nel registro predicato.
-   prede è il [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   replicateSwizzle è un singolo componente copiato (o replicato) in tutti i quattro componenti (swizzled). I componenti validi sono: \[ x, y, z, w \] o \[ r, g, b, a \] .

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Se \_ prede              |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione viene utilizzata per ignorare un blocco di codice, in base a un canale del registro predicato. Each se il \_ blocco prede deve terminare con un'istruzione [else-PS](else---ps.md) o [endif-PS](endif---ps.md) .

Tali restrizioni includono:

Se i \_ blocchi di predazione possono essere annidati. Viene conteggiata la profondità di nidificazione dinamica totale insieme a [if \_ comp](if-comp---ps.md) Blocks.

Un blocco If prede non può risiedere in \_ un blocco di ciclo, ma deve essere completamente al suo interno o racchiuderlo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




