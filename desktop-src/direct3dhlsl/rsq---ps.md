---
title: RSQ-PS
description: Calcola la radice quadrata reciproca (solo positivo) del valore scalare di origine. | RSQ-PS
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13777810c67ba38b2c8f47f0c0db0cf9b70771ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981551"
---
# <a name="rsq---ps"></a>RSQ-PS

Calcola la radice quadrata reciproca (solo positivo) del valore scalare di origine.

## <a name="syntax"></a>Sintassi



| RSQ DST, src |
|--------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine. Il registro di origine richiede l'uso esplicito di swizzle di replica, ovvero è necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| RSQ                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Il valore assoluto viene prelevato prima dell'elaborazione.

La precisione deve essere un errore assoluto di almeno 1,0/(2 ² ²) nell'intervallo (1,0, 4,0) perché le implementazioni comuni separano mantissa ed esponente.

L'output deve essere esattamente 1,0 se l'input è esattamente 1,0. Un'origine di 0,0 restituisce un valore infinito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




