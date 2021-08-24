---
title: Campionatore (Direct3D 9 asm-vs)
description: Un campionatore è uno pseudoregistro di input per un vertex shader, usato per identificare la fase di campionamento. Sono disponibili quattro campionatori di vertex shader da s0 a s3. Quattro superfici di trama possono essere lette in un singolo passaggio dello shader.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Sampler, Type (Direct3D 9 asm-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3bd822dc085243adeb97a4baaedce35b150db311ab6b98c531a3e33731635666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789081"
---
# <a name="sampler-direct3d-9-asm-vs"></a>Campionatore (Direct3D 9 asm-vs)

Un campionatore è uno pseudoregistro di input per un vertex shader, usato per identificare la fase di campionamento. Sono disponibili quattro campionatori di vertex shader: da s0 a s3. Quattro superfici di trama possono essere lette in un singolo passaggio dello shader.

Sampler (Direct3D 9 asm-vs)s sono pseudoregistri perché non è possibile leggerli o scriverli direttamente.

Un'unità di campionamento corrisponde alla fase di campionamento trame, incapsulando lo stato specifico del campionamento fornito da [**SetSamplerState.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate) Ogni campionatore identifica in modo univoco una singola superficie di trama, che viene impostata sul campionatore corrispondente usando [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Tuttavia, la stessa superficie di trama può essere impostata in più campionatori.

In fase di disegno, una trama non può essere impostata contemporaneamente come destinazione di rendering e come trama in una fase.

Poiché sono disponibili quattro campionatori, è possibile leggere fino a quattro superfici di trama da in un singolo passaggio dello shader. Un campionatore può essere visualizzato come l'unico argomento nell'istruzione di caricamento della trama: [texldl - vs](texldl---vs.md).

In vs 3 0, se viene usato un campionatore, deve essere dichiarato all'inizio del programma shader usando l'istruzione \_ \_ [dcl \_ samplerType (sm3 - vs asm).](dcl-samplertype---vs.md)



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Campionatore                |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[Trame vertice in confronto \_ a \_ 3 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 