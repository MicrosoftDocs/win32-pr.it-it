---
title: DST-vs
description: Calcola un vettore di distanza. | DST-vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e41c1da0eae001d314e2682a3295a0b88b993ee1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886091"
---
# <a name="dst---vs"></a>DST-vs

Calcola un vettore di distanza.

## <a name="syntax"></a>Sintassi



| dest DST, src0, src1 |
|----------------------|



 

dove

-   dest è il registro di destinazione.
-   src0 è un registro di origine.
-   src1 è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| DST                    | x    | x    | x    | x     | x    | x     |



 

Il frammento di codice seguente mostra le operazioni eseguite:


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



Si presuppone che il primo operando di origine (src0) sia il vettore (ignorato, d \* d, d \* d, ignorato) e che il secondo operando di origine (src1) sia il vettore (ignorato, 1/d, ignorato, 1/d). La destinazione (dest) è il vettore di risultato (1, d, d \* d, 1/d).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




