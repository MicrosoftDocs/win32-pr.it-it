---
title: Registro temporaneo (riferimenti per HLSL PS)
description: I registri temporanei di input pixel shader vengono usati per mantenere i risultati intermedi.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103857830"
---
# <a name="temporary-register-hlsl-ps-reference"></a>Registro temporaneo (riferimenti per HLSL PS)

I registri temporanei di input pixel shader vengono usati per mantenere i risultati intermedi.

Sintassi


```
no declaration is required
```





| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registro temporaneo    |      |      |      |      | x    | x     | x    | x    | x     |



 

-   Sono presenti 12 registri temporanei di pixel shader: da R0 a R11.
-   Questi registri vengono usati per archiviare i risultati intermedi durante i calcoli.
-   Se un registro temporaneo usa componenti non definiti nel codice precedente, la convalida dello shader avrà esito negativo.
-   Si tratta almeno di precisione a virgola mobile.
-   In una singola istruzione è possibile utilizzare un massimo di tre.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




