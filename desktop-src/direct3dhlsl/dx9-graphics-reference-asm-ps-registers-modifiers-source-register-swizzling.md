---
title: Registro di origine swizzling (riferimenti per HLSL PS)
description: Swizzling si riferisce alla possibilità di copiare qualsiasi componente del registro di origine in qualsiasi componente di registro temporaneo. Swizzling non influisce sui dati del registro di origine. Prima dell'esecuzione di un'istruzione, i dati in un registro di origine vengono copiati in un registro temporaneo.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335684"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a>Registro di origine swizzling (riferimenti per HLSL PS)

Swizzling si riferisce alla possibilità di copiare qualsiasi componente del registro di origine in qualsiasi componente di registro temporaneo. Swizzling non influisce sui dati del registro di origine. Prima dell'esecuzione di un'istruzione, i dati in un registro di origine vengono copiati in un registro temporaneo.

## <a name="source-swizzling"></a>Swizzling di origine

Swizzle di origine consente ai singoli componenti di un registro di origine di assumere il valore di uno dei quattro componenti dello stesso registro di origine prima che il registro venga letto per il calcolo.

Ad esempio, il zxxy swizzle significa:

-   il componente. x prenderà il valore del componente. z
-   il componente. y accetta il valore del componente. x
-   il componente. z prenderà il valore del componente. x
-   il componente. w prenderà il valore del componente y

I componenti possono essere visualizzati in qualsiasi ordine. Se vengono specificati meno di quattro componenti, l'ultimo componente viene ripetuto. Ad esempio:


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



Se non viene specificato alcun componente, non viene applicato alcun swizzling.

Per alcune istruzioni sono previste restrizioni per swizzle di origine. Sono elencate nelle pagine di riferimento all'istruzione rispettata.



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| .x                    |      |      |      | x    | x    | x    | x     | x    | x     |
| . y                    |      |      |      | x    | x    | x    | x     | x    | x     |
| . z                    | x\*  | x\*  | x\*  | x    | x    | x    | x     | x    | x     |
| . w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . xyzw (impostazione predefinita)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .yzxw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .zxyw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .wzyx                 |      |      |      |      | x    | x    | x     | x    | x     |
| swizzle arbitrario     |      |      |      |      |      | x    | x     | x    | x     |



 

\* Disponibile solo se la maschera di scrittura della destinazione è. w (. a).

## <a name="arbitrary-swizzle"></a>Swizzle arbitrario

Swizzles può essere applicato ai registri di origine in un ordine arbitrario; ovvero qualsiasi registro di origine può assumere qualsiasi maschera di componente, in qualsiasi ordine.

## <a name="replicate-swizzle"></a>Replica swizzle

Replica swizzle copia un componente in un altro. È necessario specificare esattamente uno dei componenti con estensione x, y, z, w swizzle (o. r,. g,. b,. a equivalenti).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 registri PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[\_registri PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[\_registri PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[\_registri PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




