---
title: Tipo shader
description: La sintassi per la dichiarazione di una variabile shader in un effetto è cambiata da Direct3D 9 a Direct3D 10.
ms.assetid: d24ae9ad-1b3a-4a05-b28b-b6a0583c3da8
keywords:
- Tipo di shader HLSL
topic_type:
- apiref
api_name:
- Shader Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ca3332c441279d7f9221efe8cfa7638908ddc44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976791"
---
# <a name="shader-type"></a>Tipo shader

La sintassi per la dichiarazione di una variabile shader in un effetto è cambiata da Direct3D 9 a Direct3D 10.

## <a name="shader-type-for-direct3d-10"></a>Tipo di shader per Direct3D 10

Dichiarare una variabile shader in un passaggio di effetto (in Direct3D 10) usando la sintassi del tipo di shader:



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SetPixelShader** Compilazione ( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compilazione ( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compilazione ( **ShaderTarget, ShaderFunction** ); |



 

### <a name="parameters"></a>Parametri



| Elemento                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**<br/>         | Chiamata all'API Direct3D che crea l'oggetto shader. Può essere: **SetPixelShader** o **SetGeometryShader** o **SetVertexShader**.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>         | Modello di shader in base al quale eseguire la compilazione. Questa operazione è valida per qualsiasi destinazione, inclusi tutti gli obiettivi di Direct3D 9 più gli obiettivi di [Shader Model 4](dx-graphics-hlsl-sm4.md) : vs \_ 4 \_ 0, GS \_ 4 \_ 0 e PS \_ 4 \_ 0.<br/>                                                                                                                                                                                                                                          |
| <span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**<br/> | Stringa ASCII che contiene il nome della funzione del punto di ingresso dello shader. si tratta della funzione che inizia l'esecuzione quando viene richiamato lo shader. (...) Rappresenta gli argomenti dello shader; si tratta degli stessi argomenti passati all'API di creazione dello shader: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) o [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) o [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).<br/> |



 

### <a name="example"></a>Esempio

Di seguito è riportato un esempio in cui vengono creati un vertex shader e un oggetto pixel shader, compilati per un particolare modello shader. Nell'esempio Direct3D 10 non è presente alcun geometry shader, quindi il puntatore è impostato su **null**.


```
// Direct3D 10
technique10 Render
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, VS() ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PS() ) );
    }
}
```



## <a name="shader-type-for-direct3d-9"></a>Tipo shader per Direct3D 9

Dichiarare una variabile shader in un passaggio di effetto (per Direct3D 9) usando la sintassi del tipo di shader:



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| **PixelShader** = Compila **ShaderTarget ShaderFunction (...); VertexShader** = Compila **ShaderTarget ShaderFunction (...);** |



 

### <a name="parameters"></a>Parametri



| Elemento                                                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**<br/>                                         | Variabile shader che rappresenta lo shader compilato. Può essere: **PixelShader** o **vertexshader**.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>                             | [Modello di shader](dx-graphics-hlsl-models.md) in base al quale eseguire la compilazione. dipende dal tipo di variabile shader.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**<br/> | Stringa ASCII che contiene il nome della funzione del punto di ingresso dello shader. si tratta della funzione che inizia l'esecuzione quando viene richiamato lo shader. (...) Rappresenta gli argomenti dello shader; si tratta degli stessi argomenti passati all'API di creazione dello shader: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) o [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).<br/> |



 

### <a name="example"></a>Esempio

Di seguito è riportato un esempio di vertex shader e pixel shader oggetto, compilato per un particolare modello shader.


```
// Direct3D 9
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_2_0 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_2_0 RenderScenePS( true );
    }
}
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

