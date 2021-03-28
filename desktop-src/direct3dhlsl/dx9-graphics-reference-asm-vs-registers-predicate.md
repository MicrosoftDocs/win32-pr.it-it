---
title: Registro predicato (HLSL VS Reference)
description: Questo registro di output del vertex shader contiene un valore booleano per canale.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f558a5fee10d0403eeaacab9dc29ff3ea52b427c
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104046136"
---
# <a name="predicate-register-hlsl-vs-reference"></a>Registro predicato (HLSL VS Reference)

Questo registro di output del vertex shader contiene un valore booleano per canale.

Un registro predicato è supportato dalle versioni seguenti.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| registro predicato     |      |      |       | x    | x    | x     |



 

Di seguito sono riportate le proprietà Register.



| Tipo di registro | Conteggio | L/S | \# Leggere le porte | \# Letture/Inst | Dimension | Relannr | Valori predefiniti | Richiede DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicato (p)  | 1     | L/S | 1             | 1             | 4         | N/D     | nessuno     | N            |



 

Il registro del predicato può essere modificato con [setp \_ comp-vs](setp-comp---vs.md). Non sono disponibili valori predefiniti per questo registro, un'applicazione deve impostare il registro prima che venga usato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




