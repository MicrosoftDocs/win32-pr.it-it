---
title: Sintassi di dichiarazione del frammento (HLSL Direct3D 9)
description: Ogni funzione HLSL (Microsoft High Level Shader Language) può essere convertita in un frammento di shader con l'aggiunta di una dichiarazione di frammento.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 60ac1153ff3491bc904f4f759f6653cb4243adff
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825728"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a>Sintassi di dichiarazione del frammento (HLSL Direct3D 9)

Ogni funzione HLSL (Microsoft High Level Shader Language) può essere convertita in un frammento di shader con l'aggiunta di una dichiarazione di frammento.

## <a name="syntax"></a>Sintassi


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



dove:



| Valore                  | Descrizione                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fragmentKeyword   | Parola chiave obbligatoria. Deframmentazione pixel o vertexfragment.                                                                                                                                                                                             |
| FragmentName      | Stringa di testo ASCII che specifica il nome del frammento compilato.                                                                                                                                                                                       |
| frammento di \_ compilazione | Parola chiave obbligatoria.                                                                                                                                                                                                                                     |
| shaderProfile     | Modello di shader con cui eseguire la compilazione. Qualsiasi profilo vertex shader valido (vedere [**D3DXGetVertexShaderProfile)**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)o profilo pixel shader (vedere [**D3DXGetPixelShaderProfile).**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile) |
| FunctionName()    | Nome della funzione shader, seguito da parentesi.                                                                                                                                                                                                    |



 

I parametri del frammento condiviso vengono contrassegnati aggiungendo un \_ prefisso 'r' alla relativa semantica.


```
void AmbientDiffuse( float3 vPosWorld: r_PosWorld,
                     float3 vNormalWorld: r_NormalWorld,
                     out float4 vColor: COLOR0 )
{  
    // Compute the light vector
    float3 vLight = normalize( g_vLightPosition - vPosWorld );
    
    // Compute the ambient and diffuse components of illumination
    vColor = g_vLightColor * g_vMaterialAmbient;
    vColor += g_vLightColor * g_vMaterialDiffuse * saturate( dot( vLight, vNormalWorld ) );
}
vertexfragment AmbientDiffuseFragment = compile_fragment vs_1_1 AmbientDiffuse();
```



In questo esempio la semantica r PosWorld e r NormalWorld identificano che questi due parametri sono parametri condivisi \_ \_ tra gli altri frammenti.

> [!Note]  
> Fragment Linker era una tecnologia Microsoft Direct3D 9 in D3DX 9. Fragment Linker era uno strumento (Flink.exe), un'API D3DX 9 e un miglioramento HLSL. Fragment Linker è stato eliminato a partire dalla versione di agosto 2009 di DirectX SDK. Frammento linker mai applicato a Microsoft Direct3D 10, Microsoft Direct3D 10.1 o Microsoft Direct3D 11.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
