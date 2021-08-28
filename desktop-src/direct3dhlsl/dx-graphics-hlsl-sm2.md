---
title: Modello shader 2
description: Il modello shader 2 ha aggiunto funzionalità aggiuntive al modello shader 1.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed402b34bdb8ba8caed8dc7cd5b66126d242c9ad
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988024"
---
# <a name="shader-model-2"></a>Modello shader 2

Il modello shader 2 ha aggiunto funzionalità aggiuntive al [modello shader 1.](dx-graphics-hlsl-sm1.md)





|--------|-------| | Funzionalità | Funzionalità | | Set di istruzioni | <ul><li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funzioni HLSL</strong></a></li><li>Istruzioni per l'assembly <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">(vedere Instructions - vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">Instructions - vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0 Instructions</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x Instructions</a>)</li></ul> | | Registrare set | <ul><li>Registri pixel shader (vedere registri <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">ps_2_0,</a> <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x di pixel shader)</a></li><li>Registri vertex shader (vedere <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Registri - vs_2_0</a>, Registri - <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">vs_2_x</a>)</li></ul> | | Numero massimo di pixel shader | <ul><li>ps_2_0 - Trama di 32 + 64 aritmetiche</li><li>ps_2_x: almeno 96 e fino al numero di slot in D3DCAPS9. D3DPSHADERCAPS2_0.NumInstructionSlots. Vedere D3DPSHADERCAPS2_0</li></ul> | | Numero massimo di vertex shader | 256 istruzioni | | Profili shader | ps_2_0, ps_2_x, vs_2_0, vs_2_x | 




 

Per altri dettagli sul modello shader 2, vedere:

-   [Pixel shader 2.0,](dx9-graphics-reference-asm-ps-2-0.md) [pixel shader 2.x](dx9-graphics-reference-asm-ps-2-x.md)
-   [Vertex shader 2.0,](dx9-graphics-reference-asm-vs-2-0.md) [Vertex shader 2.x](dx9-graphics-reference-asm-vs-2-x.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli di shader e profili shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




