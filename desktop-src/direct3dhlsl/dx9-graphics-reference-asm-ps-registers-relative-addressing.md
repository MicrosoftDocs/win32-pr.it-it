---
title: Indirizzamento relativo (riferimenti per HLSL PS)
description: La sintassi \ \ può essere utilizzata solo nei tipi di registro che possono essere risolti relativamente in determinati modelli shader.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38c7be68245cfedbb27898e0fbb689e9e43755ca
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719528"
---
# <a name="relative-addressing-hlsl-ps-reference"></a>Indirizzamento relativo (riferimenti per HLSL PS)

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



| Tipo di registro                                                                                   | Versioni pixel shader |
|-------------------------------------------------------------------------------------------------|-----------------------|
| [contatore di cicli](dx9-graphics-reference-asm-ps-registers-loop-counter.md): al nei registri di input | PS \_ 3 \_ 0 e versioni successive   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




