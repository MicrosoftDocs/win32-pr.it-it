---
title: Registro del contatore di cicli (informazioni di riferimento su HLSL PS)
description: L'unico registro in questa banca è il registro del contatore di cicli corrente (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719540"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a>Registro del contatore di cicli (informazioni di riferimento su HLSL PS)

L'unico registro in questa banca è il registro del contatore di cicli corrente (aL). Viene incrementato automaticamente in ogni esecuzione del blocco [loop-PS](loop---ps.md) / [EndLoop-PS](endloop---ps.md) . Pertanto, può essere utilizzato nel blocco per l'indirizzamento relativo, se necessario, e non è valido per utilizzarlo all'esterno del ciclo.



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registro contatore cicli |      |      |      |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




