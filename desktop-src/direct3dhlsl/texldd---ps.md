---
title: texldd - ps
description: Campione una trama con input sfumatura aggiuntivi.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45bd755cdc0d183a6b06e42cbd9fb3934a5dc26a729e9982bc54fb9d2a2b01fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561971"
---
# <a name="texldd---ps"></a>texldd - ps

Campione una trama con input sfumatura aggiuntivi.

## <a name="syntax"></a>Sintassi



| texldd, dst, src0, src1, src2, src3 |
|-------------------------------------|



 

Dove:

-   dst è un registro di destinazione.
-   src0 è un registro di origine che fornisce le coordinate di trama per il campione di trama. Vedere [Registro delle coordinate della trama.](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)
-   src1 identifica il registro del campionatore di origine (s ), dove specifica il numero del \# \# campionatore di trama da campionare. Al campionatore è associata una trama e uno stato del controllo definiti [**dall'enumerazione D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (ad esempio D3DSAMP \_ MINFILTER).
-   src2 è un registro di origine di input che specifica la sfumatura x.
-   src3 è un registro di origine di input che specifica la sfumatura y.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldd                |      |      |      |      |      | X \* | x     | x    | x     |



 

\* Questa istruzione è supportata solo da ps \_ 2 \_ a. Non è supportato da ps \_ 2 \_ b. Per altre informazioni sui profili, vedere [**D3DXGetPixelShaderProfile.**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)

Questa istruzione campionare una trama usando le coordinate della trama in src0, il campionatore specificato da src1 e le sfumature DSX e DSY provenienti da src2 e src3. I valori delle sfumature x e y vengono usati per selezionare il livello di mipmap appropriato della trama per il campionamento.

Tutte le origini supportano gli swizzle arbitrari.

Tutte le maschere di scrittura sono valide nella destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 