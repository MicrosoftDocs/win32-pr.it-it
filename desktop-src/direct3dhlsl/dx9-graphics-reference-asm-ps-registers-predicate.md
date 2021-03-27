---
title: Registro predicato (riferimenti per HLSL PS)
description: Questo pixel shader registro di output contiene un valore booleano per canale.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54c0706b110e04548c836bed8ae794f8da73747e
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719531"
---
# <a name="predicate-register-hlsl-ps-reference"></a>Registro predicato (riferimenti per HLSL PS)

Questo pixel shader registro di output contiene un valore booleano per canale.

Un registro predicato è supportato dalle versioni seguenti:



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| registro predicato    |      |      |      |      |      |       | x    | x    | x     |



 

Di seguito sono riportate le proprietà Register.



| Tipo di registro | Conteggio | L/S | \# Leggere le porte | \# Letture/Inst | Dimension | Relannr | Valori predefiniti | Richiede DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicato (p)  | 1     | L/S | 1             | 1             | 4         | N/D     | nessuno     | N            |



 

Il registro del predicato può essere modificato con [setp \_ comp-PS](setp-comp---ps.md). Nessun valore predefinito per questo registro. un'applicazione deve impostare il registro prima che venga usato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




