---
title: Tipo shader
description: La sintassi per dichiarare una variabile shader in un effetto è stata modificata da Direct3D 9 a Direct3D 10.
ms.assetid: d24ae9ad-1b3a-4a05-b28b-b6a0583c3da8
keywords:
- HLSL di tipo shader
topic_type:
- apiref
api_name:
- Shader Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c08c0d68a57180c8d2cf0b566caaaa383f34fc0b9f096e34484811a73a20d0fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854701"
---
# <a name="shader-type"></a>Tipo shader

La sintassi per dichiarare una variabile shader in un effetto è stata modificata da Direct3D 9 a Direct3D 10.

## <a name="shader-type-for-direct3d-10"></a>Tipo shader per Direct3D 10

Dichiarare una variabile shader all'interno di un passaggio dell'effetto (in Direct3D 10) usando la sintassi del tipo shader:



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SetPixelShader** Compile( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile( **ShaderTarget, ShaderFunction** ); |



 

### <a name="parameters"></a>Parametri



| Elemento                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**<br/>         | Chiamata api Direct3D che crea l'oggetto shader. Può essere **SetPixelShader** o **SetGeometryShader** o **SetVertexShader.**<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>         | Modello shader su cui eseguire la compilazione. Questo è valido per qualsiasi destinazione, incluse tutte le destinazioni Direct3D 9 e il modello [shader 4](dx-graphics-hlsl-sm4.md) destinazioni: vs \_ 4 \_ 0, gs \_ 4 \_ 0 e ps \_ 4 \_ 0.<br/>                                                                                                                                                                                                                                          |
| <span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**<br/> | Stringa ASCII che contiene il nome della funzione del punto di ingresso dello shader. si tratta della funzione che avvia l'esecuzione quando viene richiamato lo shader. (...) rappresenta gli argomenti dello shader. questi sono gli stessi argomenti passati all'API di creazione dello shader: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) o [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) [**o PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).<br/> |



 

### <a name="example"></a>Esempio

Ecco un esempio che crea un vertex shader e un pixel shader, compilati per un particolare modello shader. Nell'esempio Direct3D 10 non è presente alcun geometry shader, quindi il puntatore è impostato su **NULL.**


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

Dichiarare una variabile shader all'interno di un passaggio dell'effetto (per Direct3D 9) usando la sintassi del tipo shader:



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| **PixelShader** = compile **ShaderTarget ShaderFunction(...); VertexShader** = compile **ShaderTarget ShaderFunction(...);** |



 

### <a name="parameters"></a>Parametri



| Elemento                                                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**<br/>                                         | Variabile shader che rappresenta lo shader compilato. Può essere: **PixelShader** o **VertexShader.**<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>                             | Modello [shader su cui](dx-graphics-hlsl-models.md) eseguire la compilazione. dipende dal tipo di variabile shader.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**<br/> | Stringa ASCII che contiene il nome della funzione del punto di ingresso dello shader. si tratta della funzione che avvia l'esecuzione quando viene richiamato lo shader. (...) rappresenta gli argomenti dello shader. questi sono gli stessi argomenti passati all'API di creazione dello shader: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) o [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).<br/> |



 

### <a name="example"></a>Esempio

Ecco un esempio di vertex shader e pixel shader, compilato per un particolare modello shader.


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

 

