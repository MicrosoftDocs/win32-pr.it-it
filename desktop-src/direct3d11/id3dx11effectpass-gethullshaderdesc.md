---
title: Metodo ID3DX11EffectPass GetHullShaderDesc (D3dx11effect. h)
description: Ottenere la descrizione di Hull-shader.
ms.assetid: 1a683e61-da9a-4d78-8073-a6104625852b
keywords:
- Metodo GetHullShaderDesc Direct3D 11
- Metodo GetHullShaderDesc Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo GetHullShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetHullShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2fb35ddd251b6f25163b5ee4ac15ed448dc7884
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762227"
---
# <a name="id3dx11effectpassgethullshaderdesc-method"></a>Metodo ID3DX11EffectPass:: GetHullShaderDesc

Ottenere la descrizione di Hull-shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetHullShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)\***

Puntatore a una descrizione di Hull shader (vedere [**D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)).

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

 

 





