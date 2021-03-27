---
title: Campionatore (Direct3D 9 ASM-PS)
description: Un campionatore è uno pseudo-registro di input per un pixel shader, che viene usato per identificare la fase di campionamento.
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- Campionatore, tipo (Direct3D 9 ASM-PS)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77875eed0827ad6bcb6d89111b13b6a31232dd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046922"
---
# <a name="sampler-direct3d-9-asm-ps"></a>Campionatore (Direct3D 9 ASM-PS)

Un campionatore è uno pseudo-registro di input per un pixel shader, che viene usato per identificare la fase di campionamento. Sono disponibili 16 registri per la fase di campionamento pixel shader: S0 per S15. Pertanto, è possibile leggere fino a 16 superfici di trama in un singolo passaggio dello shader. Le istruzioni che usano un registro campionatore sono texld e texldp.

Il campionatore deve essere dichiarato prima dell'uso con l'istruzione [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Campionatore               |      |      |      |      | x    | x     | x    | x    | x     |



 

I sampler sono pseudo-registri perché non è possibile leggerli o scriverli direttamente.

Un'unità di campionamento corrisponde alla fase di campionamento della trama, che incapsula lo stato specifico del campionamento fornito da [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate). Ogni campionatore identifica in modo univoco una singola superficie di trama, che viene impostata sul campionatore corrispondente usando la [**texture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Tuttavia, la stessa superficie di trama può essere impostata su più Sampler.

In fase di disegnare non è possibile impostare contemporaneamente una trama come destinazione di rendering e una trama in una fase.

Un campionatore potrebbe apparire come unico argomento nell'istruzione di caricamento della trama: [texldl-PS](texldl---ps.md).

In PS \_ 3 \_ 0, se viene usato un campionatore, è necessario dichiararlo all'inizio del programma shader usando l'istruzione [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .

Il campionamento di una trama con una dimensione superiore a quella presente nelle coordinate di trama non è valido. Il campionamento di una trama con una dimensione inferiore rispetto a quello presente nelle coordinate di trama ignorerà le coordinate di trama aggiuntive.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 