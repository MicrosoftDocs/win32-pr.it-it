---
title: Metodo ID3DX11EffectShaderVariable GetPatchConstantSignatureElementDesc (D3dx11effect.h)
description: Ottenere una descrizione della firma costante della patch.
ms.assetid: 72a86cf6-ace2-4306-ac5c-37d888c087f7
keywords:
- Metodo GetPatchConstantSignatureElementDesc Direct3D 11
- Metodo GetPatchConstantSignatureElementDesc Direct3D 11, INTERFACCIA ID3DX11EffectShaderVariable
- ID3DX11EffectShaderVariable interface Direct3D 11 , GetPatchConstantSignatureElementDesc method
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPatchConstantSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85adc4a022c0f897a2e228aab670ccae60de0ec256e5f88e033991b137863fe1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565871"
---
# <a name="id3dx11effectshadervariablegetpatchconstantsignatureelementdesc-method"></a>Metodo ID3DX11EffectShaderVariable::GetPatchConstantSignatureElementDesc

Ottenere una descrizione della firma costante della patch.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPatchConstantSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice dello shader in base zero.

</dd> <dt>

*elemento* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice dell'elemento in base zero.

</dd> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3D11 \_ SIGNATURE \_ PARAMETER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***

Puntatore a una descrizione del parametro (vedere [**D3D11 \_ SIGNATURE \_ PARAMETER \_ DESC).**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

