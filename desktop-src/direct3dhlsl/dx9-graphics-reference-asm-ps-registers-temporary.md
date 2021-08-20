---
title: Registro temporaneo (informazioni di riferimento su HLSL PS)
description: I registri temporanei di input del pixel shader vengono usati per contenere i risultati intermedi.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47ac2d76c1197349fee9fc5c993d4268e69495367ce3f121b4a59004bff1b3a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090016"
---
# <a name="temporary-register-hlsl-ps-reference"></a>Registro temporaneo (informazioni di riferimento su HLSL PS)

I registri temporanei di input del pixel shader vengono usati per contenere i risultati intermedi.

Sintassi


```
no declaration is required
```





| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registro temporaneo    |      |      |      |      | x    | x     | x    | x    | x     |



 

-   Sono disponibili 12 registri temporanei pixel shader: da r0 a r11.
-   Questi registri vengono usati per archiviare i risultati intermedi durante i calcoli.
-   Se un registro temporaneo usa componenti non definiti nel codice precedente, la convalida dello shader avrà esito negativo.
-   Si tratta almeno di una precisione a virgola mobile.
-   Un massimo di tre può essere usato in una singola istruzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




