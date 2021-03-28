---
title: POW-vs
description: Src1 ABS a precisione completa (src0). | POW-vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3263fa19015bc32c94ae714891c3bbb2128c9463
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234678"
---
# <a name="pow---vs"></a>POW-vs

<sup>Src1</sup>ABS a precisione completa (src0).

## <a name="syntax"></a>Sintassi



| POW DST, src0, src1 |
|---------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 è un registro di origine di input. Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).
-   src1 è un registro di origine di input. Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| pow                    |      | x    | x    | x     | x    | x     |



 

Questa istruzione funziona come illustrato di seguito.


```
dest = pow(abs(src0), src1);
```



Si tratta di un'istruzione scalare, pertanto è necessario che i registri di origine dispongano della replica swizzles per indicare i canali utilizzati.

Il risultato scalare viene replicato in tutti e quattro i canali di output.

Questa istruzione può essere espansa come exp (src1 \* log (src0)).

La precisione non è inferiore a 15 bit.

Il registro dest deve essere un registro temporaneo e non deve essere lo stesso registro di src1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




