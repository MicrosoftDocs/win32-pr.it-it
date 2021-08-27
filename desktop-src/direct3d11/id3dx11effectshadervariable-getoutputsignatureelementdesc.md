---
title: Metodo ID3DX11EffectShaderVariable GetOutputSignatureElementDesc (D3dx11effect.h)
description: Ottenere una descrizione della firma di output.
ms.assetid: 05f43a57-18fa-4be7-814e-ffbe53837cab
keywords:
- Metodo GetOutputSignatureElementDesc Direct3D 11
- Metodo GetOutputSignatureElementDesc Direct3D 11, INTERFACCIA ID3DX11EffectShaderVariable
- Id3DX11EffectShaderVariable interface Direct3D 11, GetOutputSignatureElementDesc method
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetOutputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af968b25a00e32b489a520e9d4a3e870329af910caa8ac1bf45ac49a7ea6132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533267"
---
# <a name="id3dx11effectshadervariablegetoutputsignatureelementdesc-method"></a>Metodo ID3DX11EffectShaderVariable::GetOutputSignatureElementDesc

Ottenere una descrizione della firma di output.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetOutputSignatureElementDesc(
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

Indice shader in base zero.

</dd> <dt>

*elemento* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice di elemento in base zero.

</dd> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3D11 \_ SIGNATURE \_ PARAMETER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***

Puntatore a una descrizione del parametro (vedere [**D3D11 \_ SIGNATURE \_ PARAMETER \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Un effetto contiene uno o più shader. ogni shader ha una firma di input e output; ogni firma contiene uno o più elementi (o parametri). L'indice dello shader identifica lo shader e l'indice dell'elemento identifica l'elemento (o il parametro) nella firma dello shader.

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

 

