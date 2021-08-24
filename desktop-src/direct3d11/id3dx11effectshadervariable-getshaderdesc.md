---
title: Metodo ID3DX11EffectShaderVariable GetShaderDesc (D3dx11effect.h)
description: Ottenere una descrizione dello shader.
ms.assetid: 7dd667d3-c500-4486-b279-a165befe8733
keywords:
- Metodo GetShaderDesc Direct3D 11
- Metodo GetShaderDesc Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- ID3DX11EffectShaderVariable interface Direct3D 11 , Metodo GetShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f78e3a41fbd7f1063abdbd8c782119f62e141b7fa5a160106cf85be274435fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676851"
---
# <a name="id3dx11effectshadervariablegetshaderdesc-method"></a>Metodo ID3DX11EffectShaderVariable::GetShaderDesc

Ottenere una descrizione dello shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetShaderDesc(
   UINT                      ShaderIndex,
   D3DX11_EFFECT_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice a base zero.

</dd> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ EFFECT \_ SHADER \_ DESC**](d3dx11-effect-shader-desc.md)\***

Puntatore a una descrizione dello shader (vedere [**D3DX11 \_ EFFECT \_ SHADER \_ DESC).**](d3dx11-effect-shader-desc.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra gli effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

