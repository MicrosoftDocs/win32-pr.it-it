---
title: if pred - ps
description: Inizio di un if bool - ps... else - ps... endif - ps block, con la condizione prelevata dal contenuto del registro del predicato.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1a9e1c531e5dc6cd76bdd220a94730f2fb7b859eb99d9bba217a008fb02b4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511917"
---
# <a name="if-pred---ps"></a>if pred - ps

Inizio di [un if bool - ps](if-bool---ps.md)... [else - ps](else---ps.md)... [endif - ps](endif---ps.md) block, con la condizione prelevata dal contenuto del registro del predicato.

## <a name="syntax"></a>Sintassi



| se \[ ! \] pred.replicateSwizzle |
|-------------------------------|



 

Dove:

-   \[!\] è un modificatore NOT facoltativo. In questo modo viene modificato il valore nel registro del predicato.
-   pred è il [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   replicateSwizzle è un singolo componente che viene copiato (o replicato) in tutti e quattro i componenti (con swizzle). I componenti validi \[ sono: x, y, z, w \] o \[ r, g, b, a \] .

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| if \_ pred              |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione viene usata per ignorare un blocco di codice, in base a un canale del registro predicato. Ogni blocco \_ if pred deve terminare con [un'istruzione else - ps](else---ps.md) o [endif - ps.](endif---ps.md)

Tali restrizioni includono:

se \_ i blocchi pred possono essere annidati. Questo conteggia la profondità di annidamento dinamica totale insieme ai [blocchi \_ comp.](if-comp---ps.md)

Se un blocco pred non può essere in un blocco di ciclo, deve essere completamente al suo interno \_ o racchiuderlo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




