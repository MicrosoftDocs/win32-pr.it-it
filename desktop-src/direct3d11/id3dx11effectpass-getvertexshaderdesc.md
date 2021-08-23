---
title: Metodo ID3DX11EffectPass GetVertexShaderDesc (D3dx11effect.h)
description: Ottenere una descrizione di vertex shader.
ms.assetid: 7e02a438-2ff4-4e32-bc16-d112aafa57cb
keywords:
- Metodo GetVertexShaderDesc Direct3D 11
- Metodo GetVertexShaderDesc Direct3D 11, interfaccia ID3DX11EffectPass
- Id3DX11EffectPass interface Direct3D 11 , GetVertexShaderDesc method
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetVertexShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7942fc1f8202065ac904223693c70b4dc8ea70bf3421158a08bad253acc67567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045969"
---
# <a name="id3dx11effectpassgetvertexshaderdesc-method"></a>Metodo ID3DX11EffectPass::GetVertexShaderDesc

Ottenere una descrizione di vertex shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVertexShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ PASS \_ SHADER \_ DESC**](d3dx11-pass-shader-desc.md)\***

Puntatore a una descrizione di vertex shader (vedere [**D3DX11 \_ PASS \_ SHADER \_ DESC).**](d3dx11-pass-shader-desc.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Un passaggio di effetto può contenere assegnazioni dello stato di rendering e assegnazioni di oggetti shader.

> [!Note]  
> DirectX SDK non fornisce file binari compilati per gli effetti. È necessario usare l'origine Effects 11 per compilare l'applicazione del tipo di effetti. Per altre informazioni sull'uso dell'origine effetti 11, vedere Differenze tra gli [effetti 10 e gli effetti 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/D (una libreria di Effetti 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





