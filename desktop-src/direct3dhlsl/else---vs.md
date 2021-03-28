---
title: else-vs
description: Inizio di un blocco else. | else-vs
ms.assetid: c3bd99c2-35a1-4ffd-9781-4bac9f6bb0ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 97481d7cb651719fdf0843fd1b985c6586e54b3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981914"
---
# <a name="else---vs"></a>else-vs

Inizio di un blocco else.

## <a name="syntax"></a>Sintassi



| else |
|------|



 

## <a name="remarks"></a>Commenti



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| else                   |      | x    | x    | x     | x    | x     |



 

Se la condizione nell'istruzione [if bool-vs](if-bool---vs.md) corrispondente è true, viene eseguito il codice racchiuso dall'istruzione If bool-vs e dal [endif](endif---vs.md) corrispondente. In caso contrario, il codice racchiuso da Else... le istruzioni endif vengono eseguite.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni vertex shader](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[Se bool-vs](if-bool---vs.md)
</dt> <dt>

[endif-vs](endif---vs.md)
</dt> </dl>

 

 




