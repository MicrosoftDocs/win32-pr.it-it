---
title: else - vs
description: Inizio di un blocco else. | else - vs
ms.assetid: c3bd99c2-35a1-4ffd-9781-4bac9f6bb0ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5db315372e7c93232f9d821d9d7e91ec402661c37b8410ac4c8470a4db9e8997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119525"
---
# <a name="else---vs"></a>else - vs

Inizio di un blocco else.

## <a name="syntax"></a>Sintassi



| else |
|------|



 

## <a name="remarks"></a>Commenti



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| else                   |      | x    | x    | x     | x    | x     |



 

Se la condizione nell'istruzione [if bool - vs](if-bool---vs.md) corrispondente è true, viene eseguito il codice racchiuso tra l'istruzione if bool - vs e l'endif corrispondente. [](endif---vs.md) In caso contrario, il codice racchiuso tra else... Vengono eseguite istruzioni endif.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[se bool - vs](if-bool---vs.md)
</dt> <dt>

[endif - vs](endif---vs.md)
</dt> </dl>

 

 




