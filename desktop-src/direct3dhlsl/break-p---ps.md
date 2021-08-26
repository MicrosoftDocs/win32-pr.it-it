---
title: breakp - ps
description: Interrompere in modo condizionale il ciclo corrente all'endloop più vicino - ps o endrep - ps. Usare uno dei componenti del registro predicati come condizione per determinare se eseguire o meno l'istruzione .
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2da0d2bceea7a3e44f02e6b732337cb3447d6ef1c9798f95b664bf4da96ec2dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983321"
---
# <a name="breakp---ps"></a>breakp - ps

Interrompere in modo condizionale il ciclo corrente [all'estremità più](endloop---ps.md) vicina - ps o [endrep - ps](endrep---ps.md). Usare uno dei componenti del registro predicati come condizione per determinare se eseguire o meno l'istruzione .

## <a name="syntax"></a>Sintassi



| breakp \[ ! \] p0. {x\|y\|z\|w} |
|-----------------------------|



 

Dove:

-   \[!\] è un modificatore di negazione facoltativo.
-   p0 è il [registro predicati](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} è lo swizzle di replica richiesto in p0.

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| breakp                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




