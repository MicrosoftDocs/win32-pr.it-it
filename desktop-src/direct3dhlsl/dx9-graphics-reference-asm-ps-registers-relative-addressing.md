---
title: Indirizzamento relativo (informazioni di riferimento su HLSL PS)
description: Per i pixel shader, la sintassi \ \ può essere usata solo in tipi di registro che possono essere relativamente indirizzati in determinati modelli di shader.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8bdafe23696c460da75d87cf1f6d5a968c89ed28
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405484"
---
# <a name="relative-addressing-hlsl-ps-reference"></a>Indirizzamento relativo (informazioni di riferimento su HLSL PS)

La \[ \] sintassi può essere usata solo in tipi di registro che possono essere relativamente gestiti in determinati modelli di shader. Le forme di \[ \] sintassi supportate sono elencate di seguito:

Dove:

-   "R" indica qualsiasi tipo di registro che può essere relativamente indirizzato.
-   "A" indica qualsiasi registro che può essere usato come indice per risolvere relativamente altri registri.
-   n0 - ni, m0 - mj e k sono numeri interi >= 0.



| \[\]sintassi                              | Indice effettivo                       | Esempio                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| R \[ A + m0 + ... + mj \]                  | A + m0 + ... + mj                     | c \[ a0.x + 3 + 7 \]              |
| R \[ k ( = \] Rk )                         | k                                     | c \[ 10 \] ( = c10 )              |
| R \[ A \]                                  | Una                                     | c \[ a0.y \]                      |
| Rk \[ n0 + ... + ni + A + m0 + ... + mj \] | A + k + n0 + ... + ni + m0 + ... + mj | c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \] |
| R \[ n0 + ... + ni + A + m0 + ... + mj \]  | A + n0 + ... + ni + m0 + ... + mj     | c \[ 2 + 1 + aL + 3 + 4 + 5 \]    |
| Rk \[ A \]                                 | A + k                                 | c12 \[ aL \] , c0 \[ a0.z \]        |
| Rk \[ A + m0 + ... + mj \]                 | A + k + m0 + ... + mj                 | v1 \[ aL + 4 + 8 \]               |
| R \[ n0 + ... + ni + A \]                  | A + n0 + ... + ni                     | o \[ 3 + 1 + aL \]                |
| Rk \[ n0 + ... + ni + A \]                 | A + k + n0 + ... + ni                 | o1 \[ 2 + 1 + 3 + aL \]           |



 

I registri sono disponibili nelle versioni seguenti:



| Tipo di registro                                                                                   | Versioni pixel shader |
|-------------------------------------------------------------------------------------------------|-----------------------|
| [contatore di cicli:](dx9-graphics-reference-asm-ps-registers-loop-counter.md)aL nei registri di input | ps \_ 3 \_ 0 e versioni successive   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




