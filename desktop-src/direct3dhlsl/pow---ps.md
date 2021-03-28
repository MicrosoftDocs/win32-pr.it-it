---
title: POW-PS
description: Src1 ABS a precisione completa (src0). | POW-PS
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981271"
---
# <a name="pow---ps"></a>POW-PS

<sup>Src1</sup>ABS a precisione completa (src0).

## <a name="syntax"></a>Sintassi



| POW DST, src0, src1 |
|---------------------|



 

dove

-   DST è il registro di destinazione.
-   src0 è un registro di origine di input. Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).
-   src1 è un registro di origine di input. Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| pow                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Questa istruzione funziona nel modo seguente:

dest. x = dest. y = dest. z = dest. w = \[ ABS (src0) \] <sup>src1</sup>;

Si tratta di un'istruzione scalare, pertanto è necessario che i registri di origine dispongano della replica swizzles per indicare i canali utilizzati.

La potenza di input (src1) deve essere scalare.

Il risultato scalare viene replicato in tutti e quattro i canali di output.

Questa istruzione può essere espansa come exp (src1 \* log (src0)).

Il registro DST deve essere un registro temporaneo e non deve essere lo stesso registro di src1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




