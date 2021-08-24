---
title: Uso della Input-Assembler senza buffer
description: La creazione e l'associazione di buffer non è necessaria se gli shader non richiedono buffer. Questa sezione contiene un esempio di vertici semplici e pixel shader che disegnano un singolo triangolo.
ms.assetid: 84d24494-f2cb-4ca1-84fd-635e20f2c9ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bccbdb059e58efbef9e6c80eacbd9af5eb8a24045bdaab20bf540c13a9b719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752541"
---
# <a name="using-the-input-assembler-stage-without-buffers"></a>Uso della Input-Assembler senza buffer

La creazione e l'associazione di buffer non è necessaria se gli shader non richiedono buffer. Questa sezione contiene un esempio di vertici semplici e pixel shader che disegnano un singolo triangolo.

-   [Vertex Shader](#vertex-shader)
-   [Pixel Shader](#pixel-shader)
-   [Tecnica](#technique)
-   [Codice dell'applicazione](#application-code)
-   [Argomenti correlati](#related-topics)

## <a name="vertex-shader"></a>Vertex shader

Ad esempio, è possibile dichiarare un vertex shader che crea i propri vertici.


```
struct VSIn
{
    uint vertexId : SV_VertexID;
};

struct VSOut
{
    float4 pos : SV_Position;
    float4 color : color;
};

VSOut VSmain(VSIn input)
{
    VSOut output;
    
    if (input.vertexId == 0)
        output.pos = float4(0.0, 0.5, 0.5, 1.0);
    else if (input.vertexId == 2)
        output.pos = float4(0.5, -0.5, 0.5, 1.0);
    else if (input.vertexId == 1)
        output.pos = float4(-0.5, -0.5, 0.5, 1.0);
    
    output.color = clamp(output.pos, 0, 1);
    
    return output;
}
```



## <a name="pixel-shader"></a>Pixel shader


```
// NoBuffer.fx
// Copyright (c) 2004 Microsoft Corporation. All rights reserved.
//

struct PSIn
{
    float4 pos : SV_Position;
    linear float4 color : color;
};

struct PSOut
{
    float4 color : SV_Target;
};


PSOut PSmain(PSIn input)
{
    PSOut output;
    
    output.color = input.color;
    
    return output;
}
```



## <a name="technique"></a>Tecnica

Una tecnica è una raccolta di passaggi di rendering (deve essere presente almeno un passaggio).


```
VertexShader vsCompiled = CompileShader( vs_4_0, VSmain() );

technique10 t0
{
    pass p0
    {
        SetVertexShader( vsCompiled );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PSmain() ));
    }  
}
```



## <a name="application-code"></a>codice dell'applicazione


```
m_pD3D11Device->IASetInputLayout( NULL );

m_pD3D11Device->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
    
ID3DX11EffectTechnique * pTech = NULL;
pTech = m_pEffect->GetTechniqueByIndex(0);
pTech->GetPassByIndex(iPass)->Apply(0);

m_pD3D11Device->Draw( 3, 0 );
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con la Input-Assembler di lavoro](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> </dl>

 

 




