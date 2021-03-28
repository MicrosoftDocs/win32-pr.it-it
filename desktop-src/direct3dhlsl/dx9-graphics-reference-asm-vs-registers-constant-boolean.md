---
title: Registro booleano costante (HLSL VS Reference)
description: Questo registro è una raccolta di bit utilizzati nelle istruzioni di controllo di flusso statiche, ad esempio, se bool-vs-else-vs-endif-vs.
ms.assetid: bd02d03b-c228-481a-9c98-7442be4cdd07
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b32841f060a29fce2918daca8f8fd008529bef1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976751"
---
# <a name="constant-boolean-register-hlsl-vs-reference"></a>Registro booleano costante (HLSL VS Reference)

Questo registro è una raccolta di bit usati nelle istruzioni per il controllo di flusso statico (ad esempio, [se bool-vs](if-bool---vs.md)  -  [else-vs](else---vs.md)  -  [endif-vs](endif---vs.md)). Ne sono disponibili 16, pertanto uno shader può avere 16 condizioni di ramo indipendenti. Possono essere impostate usando [defb-vs](defb---vs.md) o [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).

Il comportamento delle costanti shader è cambiato tra Direct3D 8 e Direct3D 9.

-   Per Direct3D 9, le costanti impostate con DeFX assegnano valori allo spazio costante dello shader. Il ciclo di vita di una costante dichiarata con DeFX è limitato solo all'esecuzione di tale shader. Viceversa, le costanti impostate utilizzando le API SetXXXShaderConstantX inizializzano costanti nello spazio globale. Le costanti nello spazio globale non vengono copiate nello spazio locale (visibile allo shader) finché non viene chiamato SetxxxShaderConstants.
-   Per Direct3D 8, le costanti impostate con DeFX o le API assegnano entrambi valori allo spazio costante dello shader. Ogni volta che viene eseguito lo shader, le costanti vengono utilizzate dallo shader corrente indipendentemente dalla tecnica utilizzata per impostarle.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 