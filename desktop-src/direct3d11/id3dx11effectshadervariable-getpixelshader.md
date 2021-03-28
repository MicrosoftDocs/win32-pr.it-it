---
title: Metodo ID3DX11EffectShaderVariable GetPixelShader (D3dx11effect. h)
description: Ottenere un pixel shader.
ms.assetid: 4ce4b248-23b9-4135-a2b4-262e63247688
keywords:
- Metodo GetPixelShader Direct3D 11
- Metodo GetPixelShader Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- Interfaccia ID3DX11EffectShaderVariable Direct3D 11, metodo GetPixelShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPixelShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6588fd9afb7e58308f0fbc120705d4a22d9f2ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531026"
---
# <a name="id3dx11effectshadervariablegetpixelshader-method"></a>Metodo ID3DX11EffectShaderVariable:: GetPixelShader

Ottenere un pixel shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPixelShader(
   UINT              ShaderIndex,
   ID3D11PixelShader **ppPS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice a base zero.

</dd> <dt>

*PPP* 
</dt> <dd>

Tipo: **[ **ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader)\*\***

Puntatore a un puntatore [**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader) che verrà impostato sulla pixel shader alla restituzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

