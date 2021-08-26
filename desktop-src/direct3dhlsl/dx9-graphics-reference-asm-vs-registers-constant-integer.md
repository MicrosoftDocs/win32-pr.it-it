---
title: Constant Integer Register (informazioni di riferimento su HLSL VS)
description: I registri di numeri interi costanti vengono usati solo dal ciclo , rispetto a rep,
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b46390303b2ee3aae2243f25d2a5a76385b9e9dd275c2952e8aa93e18f999e9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949901"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a>Constant Integer Register (informazioni di riferimento su HLSL VS)

I registri di numeri interi costanti vengono usati solo dal [ciclo , da e](loop---vs.md) da [rep, rispetto a](rep---vs.md).

Possono essere impostati usando [defi - o](defi---vs.md) [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).

Se usato come argomento per il [ciclo , rispetto all'istruzione](loop---vs.md) :

-   .x è il conteggio delle iterazioni. ([rep - vs usa](rep---vs.md) solo questo componente).
-   .y è il valore iniziale per il contatore del ciclo.
-   .z è il passaggio di incremento per il contatore del ciclo.

Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.

-   Per Direct3D 9, le costanti impostate con defx assegnano valori allo spazio costante dello shader. La durata di una costante dichiarata con defx è limitata solo all'esecuzione di tale shader. Al contrario, le costanti impostate usando le API SetXXXShaderConstantX inizializzano le costanti nello spazio globale. Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) fino a quando non viene chiamato SetxxxShaderConstants.
-   Per Direct3D 8, le costanti impostate con defx o le API assegnano entrambi valori allo spazio costante dello shader. Ogni volta che lo shader viene eseguito, le costanti vengono usate dallo shader corrente indipendentemente dalla tecnica usata per impostarle.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 