---
title: Swizzling del registro di origine (informazioni di riferimento su HLSL PS)
description: Swizzling si riferisce alla possibilità di copiare qualsiasi componente del registro di origine in qualsiasi componente di registro temporaneo. Lo swizzling non influisce sui dati del registro di origine. Prima dell'esecuzione di un'istruzione, i dati in un registro di origine vengono copiati in un registro temporaneo.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c0357a902c793165149da5c853ac953cf5989f8a472fe936c6c2b95cb9e3197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090114"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a>Swizzling del registro di origine (informazioni di riferimento su HLSL PS)

Swizzling si riferisce alla possibilità di copiare qualsiasi componente del registro di origine in qualsiasi componente di registro temporaneo. Lo swizzling non influisce sui dati del registro di origine. Prima dell'esecuzione di un'istruzione, i dati in un registro di origine vengono copiati in un registro temporaneo.

## <a name="source-swizzling"></a>Swizzling di origine

Lo swizzle di origine consente al singolo componente di un registro di origine di assumere il valore di uno dei quattro componenti dello stesso registro di origine prima che il registro venga letto per il calcolo.

Ad esempio, lo swizzle .zxxy significa:

-   Il componente .x accetta il valore del componente .z
-   Il componente .y accetta il valore del componente .x
-   Il componente .z accetta il valore del componente .x
-   Il componente .w accetta il valore del componente .y

I componenti possono essere visualizzati in qualsiasi ordine. Se vengono specificati meno di quattro componenti, l'ultimo componente viene ripetuto. Esempio:


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



Se non viene specificato alcun componente, non viene applicata alcuna swizzling.

Alcune istruzioni hanno restrizioni per lo swizzle di origine. Sono elencati nelle pagine di riferimento alle istruzioni rispettate.



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| .x                    |      |      |      | x    | x    | x    | x     | x    | x     |
| .y                    |      |      |      | x    | x    | x    | x     | x    | x     |
| .z                    | X\*  | X\*  | x\*  | x    | x    | x    | x     | x    | x     |
| .w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .xyzw (impostazione predefinita)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .yzxw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .zxyw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .wzyx                 |      |      |      |      | x    | x    | x     | x    | x     |
| swizzle arbitrario     |      |      |      |      |      | x    | x     | x    | x     |



 

\* Disponibile solo se la maschera di scrittura di destinazione è w (.a).

## <a name="arbitrary-swizzle"></a>Swizzle arbitrario

Gli swizzle possono essere applicati ai registri di origine in un ordine arbitrario. in altre informazioni, qualsiasi registro di origine può assumere qualsiasi maschera dei componenti, in qualsiasi ordine.

## <a name="replicate-swizzle"></a>Replicare Swizzle

Replica swizzle copia un componente in un altro. Ovvero, è necessario specificare esattamente uno dei componenti .x, .y, .z, .w swizzle (o .r, .g, .b, .a equivalenti).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modificatori del registro di origine pixel shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registri](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[ps \_ 2 \_ 0 Registri](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[ps \_ 2 \_ x Registri](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[ps \_ 3 \_ 0 Registri](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




