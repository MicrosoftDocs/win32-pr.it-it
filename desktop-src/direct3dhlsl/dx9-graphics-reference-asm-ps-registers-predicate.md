---
title: Registro del predicato (informazioni di riferimento su HLSL PS)
description: Questo pixel shader di output contiene un valore booleano per canale.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cc8404c9a6be87951142ff3473b283a57f4814b729a8ad5a462f9069b20f3ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950031"
---
# <a name="predicate-register-hlsl-ps-reference"></a>Registro del predicato (informazioni di riferimento su HLSL PS)

Questo pixel shader di output contiene un valore booleano per canale.

Un registro di predicato è supportato dalle versioni seguenti:



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| registro del predicato    |      |      |      |      |      |       | x    | x    | x     |



 

Ecco le proprietà del registro.



| Tipo di registro | Conteggio | L/S | \# Leggere le porte | \# Reads/inst | Dimensione | RelAddr | Valori predefiniti | Richiede la DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicate(p)  | 1     | L/S | 1             | 1             | 4         | N/A     | Nessuno     | N            |



 

Il registro del predicato può essere modificato con [setp \_ comp - ps](setp-comp---ps.md). Non sono presenti valori predefiniti per questo registro. Un'applicazione deve impostare il registro prima che venga usato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




