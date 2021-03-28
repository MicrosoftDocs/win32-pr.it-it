---
title: Metodo ID3DX11EffectPass GetDomainShaderDesc (D3dx11effect. h)
description: Ottenere una descrizione dello shader di dominio.
ms.assetid: 02109930-0922-46b8-9381-bb75abd0c4a0
keywords:
- Metodo GetDomainShaderDesc Direct3D 11
- Metodo GetDomainShaderDesc Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo GetDomainShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDomainShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2157134d97332fc9c76267f5e0db49d2c40e96a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982433"
---
# <a name="id3dx11effectpassgetdomainshaderdesc-method"></a>Metodo ID3DX11EffectPass:: GetDomainShaderDesc

Ottenere una descrizione dello shader di dominio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDomainShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)\***

Puntatore a una descrizione di Domain shader (vedere [**D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)).

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

 





