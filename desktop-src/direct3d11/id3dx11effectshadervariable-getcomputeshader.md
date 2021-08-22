---
title: Metodo ID3DX11EffectShaderVariable GetComputeShader (D3dx11effect.h)
description: Ottenere uno shader di calcolo.
ms.assetid: 16a48be1-4e73-4206-837f-615f8d624086
keywords:
- Metodo GetComputeShader Direct3D 11
- Metodo GetComputeShader Direct3D 11, interfaccia ID3DX11EffectShaderVariable
- ID3DX11EffectShaderVariable interface Direct3D 11 , Metodo GetComputeShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetComputeShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27a256c143a7232494e34c2b6c36255f1360cf15225c212d0d7c1be6678d3b7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565901"
---
# <a name="id3dx11effectshadervariablegetcomputeshader-method"></a>Metodo ID3DX11EffectShaderVariable::GetComputeShader

Ottenere uno shader di calcolo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetComputeShader(
   UINT                ShaderIndex,
   ID3D11ComputeShader **ppPS
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ShaderIndex* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice dello shader di calcolo.

</dd> <dt>

*Ppp* 
</dt> <dd>

Tipo: **[ **ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***

Puntatore a [**un puntatore ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader) che verrà impostato sul compute shader al ritorno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra effetti 10 ed effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectShaderVariable](id3dx11effectshadervariable.md)
</dt> </dl>

 

