---
title: label - ps
description: Contrassegnare l'istruzione successiva come con un indice di etichetta. | label - ps
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 921abbc0518182eaef17326082a395e5c5729d8ab550610fe71c8dfabe46dd4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854201"
---
# <a name="label---ps"></a>label - ps

Contrassegnare l'istruzione successiva come con un indice di etichetta.

## <a name="syntax"></a>Sintassi



| etichetta l\# |
|-----------|



 

dove \# identifica il numero dell'etichetta.

Per ps \_ 2 \_ x, il numero di etichetta deve essere compreso tra 0 e 15.

Per ps 2 sw, ps 3 0 e ps 3 sw, il numero di etichetta deve essere compreso tra \_ \_ \_ \_ \_ \_ 0 e 2047.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| label                 |      |      |      |      |      | x    | x     | x    | x     |



 

Questa istruzione definisce un'etichetta che si trova in corrispondenza dell'istruzione shader successiva. L'istruzione label può essere presente solo dopo un'istruzione [ret](ret---ps.md) (che definisce la fine della subroutine o del programma principale precedente).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




