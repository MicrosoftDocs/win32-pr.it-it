---
title: label - vs
description: Contrassegnare l'istruzione successiva come con un indice di etichetta. | label - vs
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81c36c3db93acdc82d725c9cf7893c52d7177bbe70e16378c3b86f39ec4d6a2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854181"
---
# <a name="label---vs"></a>label - vs

Contrassegnare l'istruzione successiva come con un indice di etichetta.

## <a name="syntax"></a>Sintassi



| etichetta l\# |
|-----------|



 

dove \# identifica il numero di etichetta.

Per i valori 2 0 e 2 x, il numero di etichetta deve essere compreso tra \_ \_ \_ \_ 0 e 15.

Per vs 2 sw, vs 3 0 e vs 3 sw, il numero di etichetta deve essere compreso tra \_ \_ \_ \_ \_ \_ 0 e 2047.

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| label                  |      | x    | x    | x     | x    | x     |



 

Questa istruzione definisce un'etichetta che si trova in corrispondenza dell'istruzione shader successiva. L'istruzione label può essere presente solo dopo un'istruzione [ret](ret---vs.md) (che definisce la fine della subroutine o del programma principale precedente).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




