---
title: Registro contatori del ciclo (informazioni di riferimento su HLSL PS)
description: Informazioni sul registro dei contatori del ciclo per i pixel shader. L'unico registro in questa banca è il registro corrente del contatore del ciclo (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a2f7f42c83308fa72ceae2875c35c600dfd7db
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405514"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a>Registro contatori del ciclo (informazioni di riferimento su HLSL PS)

L'unico registro in questa banca è il registro corrente del contatore del ciclo (aL). Viene incrementato automaticamente in ogni esecuzione del [ciclo ps](loop---ps.md) / [endloop - blocco ps.](endloop---ps.md) Può quindi essere usato nel blocco per l'indirizzamento relativo, se necessario, e non è valido per usarlo all'esterno del ciclo.



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registro contatori cicli |      |      |      |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




