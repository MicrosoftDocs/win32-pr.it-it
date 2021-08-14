---
title: if pred - vs
description: Inizio di un oggetto if pred - vs... else - vs... endif - vs block, con la condizione prelevata dal contenuto del registro del predicato.
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad9aba5c9f18b88577a456764a71cc27637d24856cdafa95d811344034d514f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511907"
---
# <a name="if-pred---vs"></a>if pred - vs

Inizio di un oggetto if pred - vs... [else - vs](else---vs.md)... [endif - vs](endif---vs.md) block, con la condizione prelevata dal contenuto del registro del predicato.

## <a name="syntax"></a>Sintassi



| se \[ ! \] pred.replicateSwizzle |
|-------------------------------|



 

Dove:

-   \[!\] Modificatore NOT facoltativo. In questo modo viene modificato il valore nel registro del predicato.
-   pred è il registro del predicato, p0. Vedere [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   replicateSwizzle è un singolo componente che viene copiato (o replicato) in tutti e quattro i componenti (con swizzle). I componenti validi sono: x, y, z, w o r, g, b, a.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| if pred                |      |      | x    | x     | x    | x     |



 

Questa istruzione viene usata per ignorare un blocco di codice, in base a un canale del registro predicato. Ogni blocco \_ if pred deve terminare con un'istruzione else o endif.

Tali restrizioni includono:

se \_ i blocchi pred possono essere annidati. Questo conteggia la profondità di annidamento dinamica totale insieme ai [blocchi \_ comp.](if-comp---vs.md)

Se un blocco pred non può essere in un blocco di ciclo, deve essere completamente al suo interno \_ o racchiuderlo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




