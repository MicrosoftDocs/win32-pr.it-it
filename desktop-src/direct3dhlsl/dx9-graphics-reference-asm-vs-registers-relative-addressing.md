---
title: Indirizzamento relativo (informazioni di riferimento su Visual Studio HLSL)
description: Per i vertex shader, la sintassi \ \ può essere usata solo in tipi di registro che possono essere relativamente gestiti in determinati modelli di shader.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 82fe97a6b78a2257208f3072d5932523d5cd04ba1d044b8a57fad5f3c212b94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744341"
---
# <a name="relative-addressing-hlsl-vs-reference"></a>Indirizzamento relativo (informazioni di riferimento su Visual Studio HLSL)

La \[ \] sintassi può essere usata solo in tipi di registro che possono essere relativamente gestiti in determinati modelli di shader. Le forme di \[ \] sintassi supportate sono elencate di seguito:

Dove:

-   "R" indica qualsiasi tipo di registro che può essere relativamente indirizzato.
-   "A" indica qualsiasi registro che può essere usato come indice per risolvere relativamente altri registri.
-   n0 - ni, m0 - mj e k sono numeri interi >= 0.



| \[\]sintassi                              | Indice effettivo                       | Esempio                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| R \[ A + m0 + ... + mj \]                  | A + m0 + ... + mj                     | c \[ a0.x + 3 + 7 \]              |
| R \[ k ( = \] Rk )                         | k                                     | c \[ 10 \] ( = c10 )              |
| R \[ A \]                                  | A                                     | c \[ a0.y \]                      |
| Rk \[ n0 + ... + ni + A + m0 + ... + mj \] | A + k + n0 + ... + ni + m0 + ... + mj | c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \] |
| R \[ n0 + ... + ni + A + m0 + ... + mj \]  | A + n0 + ... + ni + m0 + ... + mj     | c \[ 2 + 1 + aL + 3 + 4 + 5 \]    |
| Rk \[ A \]                                 | A + k                                 | c12 \[ aL \] , c0 \[ a0.z \]        |
| Rk \[ A + m0 + ... + mj \]                 | A + k + m0 + ... + mj                 | v1 \[ aL + 4 + 8 \]               |
| R \[ n0 + ... + ni + A \]                  | A + n0 + ... + ni                     | o \[ 3 + 1 + aL \]                |
| Rk \[ n0 + ... + ni + A \]                 | A + k + n0 + ... + ni                 | o1 \[ 2 + 1 + 3 + aL \]           |



 

I registri sono disponibili nelle versioni seguenti:



| Tipo di registro | Versioni vertex shader |
|---------------|------------------------|
| a0            | Tutti                    |
| aL            | vs \_ 2 \_ 0 e versioni successive    |
| cn            | vs \_ 1 \_ 1 e versioni successive    |
| on            | vs \_ 3 \_ 0               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




