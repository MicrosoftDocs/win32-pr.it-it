---
title: etichetta-PS
description: Contrassegnare l'istruzione successiva in modo che disponga di un indice di etichetta. | etichetta-PS
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3fb266b649642c82293e8310b6302c6763ddc27
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995576"
---
# <a name="label---ps"></a>etichetta-PS

Contrassegnare l'istruzione successiva in modo che disponga di un indice di etichetta.

## <a name="syntax"></a>Sintassi



| etichetta l\# |
|-----------|



 

dove \# identifica il numero di etichetta.

Per PS \_ 2 \_ x, il numero di etichetta deve essere compreso tra 0 e 15.

Per PS \_ 2 \_ SW, PS \_ 3 \_ 0 e PS \_ 3 \_ SW, il numero di etichetta deve essere compreso tra 0 e 2047.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| label                 |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione definisce un'etichetta che si trova nella successiva istruzione dello shader. L'istruzione label può essere presente solo subito dopo un'istruzione [ret](ret---ps.md) (che definisce la fine della subroutine o del programma principale precedente).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




