---
title: Indirizzamento relativo (informazioni di riferimento su HLSL VS)
description: Per i vertex shader, la sintassi \ \ può essere usata solo nei tipi di registro che possono essere relativamente indirizzati in determinati modelli shader.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2bbba694878ba84ac3c2fa9c4e8058bb0d91830e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406694"
---
# <a name="relative-addressing-hlsl-vs-reference"></a>Indirizzamento relativo (informazioni di riferimento su HLSL VS)

La \[ \] sintassi può essere usata solo nei tipi di registro che possono essere relativamente indirizzati in determinati modelli shader. Le forme di \[ \] sintassi supportate sono elencate di seguito:

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



| Tipo di registrazione | Versioni di Vertex Shader |
|---------------|------------------------|
| a0            | Tutti                    |
| aL            | vs \_ 2 \_ 0 e versioni successive    |
| cn            | vs \_ 1 \_ 1 e versioni successive    |
| on            | vs \_ 3 \_ 0               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




