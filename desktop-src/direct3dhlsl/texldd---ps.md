---
title: texldd-PS
description: Esegue il campionamento di una trama con input di sfumatura aggiuntivi.
ms.assetid: 6d6b3180-d82e-4be4-929b-e5a6431bec38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 72f3c4aaf9ac7e6beaad1343c024aa28bd2a85ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399051"
---
# <a name="texldd---ps"></a>texldd-PS

Esegue il campionamento di una trama con input di sfumatura aggiuntivi.

## <a name="syntax"></a>Sintassi



| texldd, DST, src0, src1, src2, src3 |
|-------------------------------------|



 

Dove:

-   DST è un registro di destinazione.
-   src0 è un registro di origine che fornisce le coordinate di trama per l'esempio di trama. Vedere [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   src1 identifica i registri del campionatore \# di origine, dove \# specifica il numero del campionatore di trama da campionare. Il campionatore è associato a una trama e a uno stato del controllo definito dall'enumerazione [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (es. D3DSAMP \_ MINFILTER).
-   src2 è un registro di origine di input che specifica la sfumatura x.
-   src3 è un registro di origine di input che specifica la sfumatura y.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldd                |      |      |      |      |      | x \* | x     | x    | x     |



 

\* Questa istruzione è supportata solo da PS \_ 2 \_ a. Non è supportato da PS \_ 2 \_ b. Per ulteriori informazioni sui profili, vedere [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile).

Questa istruzione esegue il campionamento di una trama usando le coordinate di trama in src0, il campionatore specificato da src1 e le sfumature DSX e DSY provenienti da src2 e src3. I valori delle sfumature x e y vengono usati per selezionare il livello di mipmap appropriato della trama per il campionamento.

Tutte le origini supportano swizzles arbitrario.

Tutte le maschere di scrittura sono valide nella destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 