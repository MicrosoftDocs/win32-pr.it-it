---
title: Metodo ID3DX11EffectPass GetGeometryShaderDesc (D3dx11effect.h)
description: Ottenere una descrizione geometry-shader.
ms.assetid: 03298ec3-6b85-40bf-8920-a82c7606d326
keywords:
- Metodo GetGeometryShaderDesc Direct3D 11
- Metodo GetGeometryShaderDesc Direct3D 11, interfaccia ID3DX11EffectPass
- Id3DX11EffectPass interface Direct3D 11, GetGeometryShaderDesc method
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetGeometryShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e93c9dfdc2525f2b730f88a9ffaeb5c68d4c9d8304410ddcf891f063cf20729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535037"
---
# <a name="id3dx11effectpassgetgeometryshaderdesc-method"></a>Metodo ID3DX11EffectPass::GetGeometryShaderDesc

Ottenere una descrizione geometry-shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetGeometryShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ PASS \_ SHADER \_ DESC**](d3dx11-pass-shader-desc.md)\***

Puntatore a una descrizione geometry-shader (vedere [**D3DX11 \_ PASS \_ SHADER \_ DESC).**](d3dx11-pass-shader-desc.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei codici [restituiti Direct3D 11 seguenti.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Un passaggio dell'effetto può contenere assegnazioni dello stato di rendering e assegnazioni di oggetti shader.

> [!Note]  
> DirectX SDK non fornisce alcun file binario compilato per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione effects-type. Per altre informazioni sull'uso dell'origine Effetti 11, vedere Differenze [tra gli effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





