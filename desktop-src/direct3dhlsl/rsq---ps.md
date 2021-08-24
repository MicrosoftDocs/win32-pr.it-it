---
title: rsq - ps
description: Calcola la radice quadrata reciproca (solo positivo) dello scalare di origine. | rsq - ps
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 48a36715113678e199b3da22be9cdf118f385c15397a16ddd39bdd83622f76f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788701"
---
# <a name="rsq---ps"></a>rsq - ps

Calcola la radice quadrata reciproca (solo positivo) dello scalare di origine.

## <a name="syntax"></a>Sintassi



| rsq dst, src |
|--------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito dello swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti .x, .y, .z, .w swizzle (o .r, .g, .b, .a equivalents).

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Rsq                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Il valore assoluto viene preso prima dell'elaborazione.

La precisione deve essere almeno un errore assoluto di 1,0/(2°) nell'intervallo (1.0, 4.0) perché le implementazioni comuni separano mantissa ed esponente.

L'output deve essere esattamente 1,0 se l'input è esattamente 1,0. Un'origine di 0,0 restituisce infinito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




