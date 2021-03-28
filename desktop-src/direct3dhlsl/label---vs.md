---
title: etichetta-vs
description: Contrassegnare l'istruzione successiva in modo che disponga di un indice di etichetta. | etichetta-vs
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e2b72fe21301aa66d8428dc3696ceb3f12e6214
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995723"
---
# <a name="label---vs"></a>etichetta-vs

Contrassegnare l'istruzione successiva in modo che disponga di un indice di etichetta.

## <a name="syntax"></a>Sintassi



| etichetta l\# |
|-----------|



 

dove \# identifica il numero di etichetta.

Per vs \_ 2 \_ 0 e vs \_ 2 \_ x, il numero di etichetta deve essere compreso tra 0 e 15.

Per vs \_ 2 \_ SW, vs \_ 3 \_ 0 e vs \_ 3 \_ SW, il numero di etichetta deve essere compreso tra 0 e 2047.

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| label                  |      | x    | x    | x     | x    | x     |



 

Questa istruzione definisce un'etichetta che si trova nella successiva istruzione dello shader. L'istruzione label può essere presente solo subito dopo un'istruzione [ret](ret---vs.md) (che definisce la fine della subroutine o del programma principale precedente).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




