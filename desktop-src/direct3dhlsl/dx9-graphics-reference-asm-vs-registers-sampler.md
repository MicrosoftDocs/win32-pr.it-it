---
title: Campionatore (Direct3D 9 ASM-vs)
description: Un campionatore è uno pseudo-registro di input per un vertex shader, usato per identificare la fase di campionamento. Sono disponibili quattro campionatori vertex shader S0 per S3. Quattro superfici di trama possono essere lette in un singolo passaggio dello shader.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Campionatore, tipo (Direct3D 9 ASM-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399664"
---
# <a name="sampler-direct3d-9-asm-vs"></a>Campionatore (Direct3D 9 ASM-vs)

Un campionatore è uno pseudo-registro di input per un vertex shader, usato per identificare la fase di campionamento. Sono disponibili quattro campionatori vertex shader: S0 per S3. Quattro superfici di trama possono essere lette in un singolo passaggio dello shader.

Sampler (Direct3D 9 ASM-vs) s sono pseudo-registri perché non è possibile leggere o scrivere direttamente.

Un'unità di campionamento corrisponde alla fase di campionamento della trama, che incapsula lo stato specifico del campionamento fornito da [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate). Ogni campionatore identifica in modo univoco una singola superficie di trama, che viene impostata sul campionatore corrispondente usando la [**texture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Tuttavia, la stessa superficie di trama può essere impostata su più Sampler.

In fase di disegnare non è possibile impostare contemporaneamente una trama come destinazione di rendering e una trama in una fase.

Poiché sono presenti quattro campionatori, è possibile leggere fino a quattro superfici di trama in un unico passaggio dello shader. Un campionatore potrebbe apparire come unico argomento nell'istruzione di caricamento della trama: [texldl-vs](texldl---vs.md).

In vs \_ 3 \_ 0, se viene usato un campionatore, è necessario dichiararlo all'inizio del programma shader usando l'istruzione [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md) .



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Campionatore                |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[Trame di vertici in vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 