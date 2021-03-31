---
title: Indirizzamento relativo (riferimento HLSL VS)
description: La sintassi \ \ può essere utilizzata solo nei tipi di registro che possono essere risolti relativamente in determinati modelli shader.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c11d6f6c4b448e1dee5f4237696c110519bc0dd0
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335676"
---
# <a name="relative-addressing-hlsl-vs-reference"></a>Indirizzamento relativo (riferimento HLSL VS)

La \[ \] sintassi può essere utilizzata solo nei tipi di registro che possono essere considerati relativamente in determinati modelli shader. I formati di \[ \] sintassi supportati sono elencati di seguito:

Dove:

-   "R" indica qualsiasi tipo di registro che può essere considerato relativamente.
-   "A" indica tutti i registri che possono essere usati come indice per indirizzare gli altri registri in modo relativamente diverso.
-   N0-NI, M0-MJ e k sono numeri interi >= 0.



| \[\]sintassi di                              | Indice effettivo                       | Esempio                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| R \[ A + M0 +... + MJ \]                  | A + M0 +... + MJ                     | c \[ a0. x + 3 + 7 \]              |
| R \[ k \] (= RK)                         | k                                     | c \[ 10 \] (= C10)              |
| R \[ A \]                                  | A                                     | c \[ a0. y \]                      |
| RK \[ N0 +... + ni + A + M0 +... + MJ \] | A + k + N0 +... + ni + M0 +... + MJ | C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \] |
| R \[ N0 +... + ni + A + M0 +... + MJ \]  | A + N0 +... + ni + M0 +... + MJ     | c \[ 2 + 1 + al + 3 + 4 + 5 \]    |
| RK \[ A \]                                 | A + k                                 | C12 \[ al \] , C0 \[ a0. z \]        |
| RK \[ A + M0 +... + MJ \]                 | A + k + M0 +... + MJ                 | V1 \[ al + 4 + 8 \]               |
| R \[ N0 +... + ni + A \]                  | A + N0 +... + ni                     | o \[ 3 + 1 + al \]                |
| RK \[ N0 +... + ni + A \]                 | A + k + N0 +... + ni                 | O1 \[ 2 + 1 + 3 + al \]           |



 

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

 

 




