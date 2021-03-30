---
title: Registro di tipo Integer costante (riferimento di HLSL VS)
description: I registri di tipo integer costanti vengono usati solo da loop-vs e Rep-vs.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4cf2612eccb891ce0cffd04955e4997173e84007
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976775"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a>Registro di tipo Integer costante (riferimento di HLSL VS)

I registri di tipo integer costanti vengono usati solo da [loop-vs](loop---vs.md) e [Rep-vs](rep---vs.md).

Possono essere impostate tramite [defi-vs](defi---vs.md) o [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).

Quando viene usato come argomento dell'istruzione [loop-vs](loop---vs.md) :

-   . x è il numero di iterazioni. ([Rep-vs](rep---vs.md) usa solo questo componente).
-   . y è il valore iniziale del contatore di cicli.
-   . z è il passaggio di incremento per il contatore del ciclo.

Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.

-   Per Direct3D 9, le costanti impostate con DeFX assegnano valori allo spazio costante dello shader. Il ciclo di vita di una costante dichiarata con DeFX è limitato solo all'esecuzione di tale shader. Viceversa, le costanti impostate utilizzando le API SetXXXShaderConstantX inizializzano costanti nello spazio globale. Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) finché non viene chiamato SetxxxShaderConstants.
-   Per Direct3D 8, le costanti impostate con DeFX o le API assegnano entrambi valori allo spazio costante dello shader. Ogni volta che viene eseguito lo shader, le costanti vengono utilizzate dallo shader corrente indipendentemente dalla tecnica utilizzata per impostarle.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 