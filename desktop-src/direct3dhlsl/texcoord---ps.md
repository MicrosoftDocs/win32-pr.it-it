---
title: TEXCOORD-PS
description: Interpreta i dati delle coordinate di trama (UVW1) come dati di colore (RGBA).
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728058"
---
# <a name="texcoord---ps"></a>TEXCOORD-PS

Interpreta i dati delle coordinate di trama (UVW1) come dati di colore (RGBA).

## <a name="syntax"></a>Sintassi



| TEXCOORD DST |
|--------------|



 

dove

-   DST è il registro di destinazione.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcoord              | x    | x    | x    |      |      |      |       |      |       |



 

Questa istruzione interpreta il set di coordinate di trama (UVW1) corrispondente al numero di registro di destinazione come dati colore (RGBA). Se il set di coordinate di trama contiene meno di tre componenti, i componenti mancanti vengono impostati su 0. Il quarto componente viene sempre impostato su 1. Tutti i valori vengono fissati tra 0 e 1.

Il vantaggio di TEXCOORD è che fornisce un modo per passare i dati dei vertici interpolati a precisione elevata direttamente nel pixel shader. Tuttavia, quando i dati vengono scritti nel registro di destinazione, una certa precisione andrà persa, a seconda del numero di bit utilizzati dall'hardware per i registri.

Questa istruzione non consente di campionare alcuna trama. Sono rilevanti solo le coordinate di trama impostate in questa fase della trama.

È possibile eseguire il mapping di qualsiasi dato di trama, ad esempio posizione, normale e direzione di origine, tramite un vertex shader in una coordinata di trama. Questa operazione viene eseguita associando una trama a un registro di trama usando la trama e specificando il modo in cui viene eseguito il campionamento della [**trama usando**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate). Se viene utilizzata la pipeline della funzione fissa, assicurarsi di specificare il \_ flag TEXCOORDINDEX di TSS.

Questa istruzione viene utilizzata come segue:


```
texcoord tn
```



Un [registro delle coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) contiene quattro valori di colore (RGBA). I dati possono essere considerati anche come dati vettoriali (xyzw). TEXCOORD recupererà tre di questi valori (XYZ) dal set di coordinate di trama x e il quarto componente (w) verrà impostato su 1. L'indirizzo di trama viene copiato dal set di coordinate di trama n. Il risultato viene fissato tra 0 e 1.

Questo esempio viene utilizzato solo a scopo illustrativo. Il codice C associato allo shader non è stato ottimizzato per le prestazioni.

Di seguito è riportato un esempio di shader che usa TEXCOORD.


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



L'output di cui è stato eseguito il rendering dal pixel shader è illustrato nella figura seguente. I valori delle coordinate (u, v, w, 1) vengono mappati ai canali (RGB). Il canale alfa è impostato su 1. Negli angoli dell'illustrazione, la coordinata (0, 0, 0, 1) viene interpretata come nera; (1, 0, 0, 1) è rosso; (0, 1, 0, 1) è verde; e (1, 1, 0, 1) contiene verde e rosso, producendo un colore giallo.

![illustrazione dell'output sottoposto a rendering dell'esempio pixel shader](images/pstexcoord.jpg)

Il codice aggiuntivo è necessario per usare questo shader e uno scenario di esempio è illustrato di seguito.


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 