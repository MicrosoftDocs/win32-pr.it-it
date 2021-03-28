---
title: Metodo ID3DX11EffectPass GetGeometryShaderDesc (D3dx11effect. h)
description: Ottenere una descrizione dello shader di geometria.
ms.assetid: 03298ec3-6b85-40bf-8920-a82c7606d326
keywords:
- Metodo GetGeometryShaderDesc Direct3D 11
- Metodo GetGeometryShaderDesc Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo GetGeometryShaderDesc
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
ms.openlocfilehash: 94c3b84ed9e8c245611c1442987b68a94e7b10ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995954"
---
# <a name="id3dx11effectpassgetgeometryshaderdesc-method"></a>Metodo ID3DX11EffectPass:: GetGeometryShaderDesc

Ottenere una descrizione dello shader di geometria.

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

Tipo: **[ **D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)\***

Puntatore a una descrizione dello shader di geometria (vedere [**D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Un passaggio di effetto può contenere le assegnazioni dello stato di rendering e le assegnazioni degli oggetti shader.

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

 

 





