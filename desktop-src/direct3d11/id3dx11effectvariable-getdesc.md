---
title: Metodo getdesc ID3DX11EffectVariable (D3dx11effect. h)
description: Ottenere una descrizione.
ms.assetid: bf6339d7-8eb0-44da-893e-c805309a3cd3
keywords:
- Metodo getdesc Direct3D 11
- Metodo getdesc Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo getdesc
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1625b9d72b3ff4afe1880b48125d244da1f68844
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996284"
---
# <a name="id3dx11effectvariablegetdesc-method"></a>Metodo ID3DX11EffectVariable:: getdesc

Ottenere una descrizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_VARIABLE_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDesc* 
</dt> <dd>

Tipo: **[ **D3DX11 \_ Effect \_ variabile \_ desc**](d3dx11-effect-variable-desc.md)\***

Un puntatore a una descrizione della variabile di effetto ( [**vedere \_ variabile effetto D3DX11 \_ \_ desc**](d3dx11-effect-variable-desc.md)).

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

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





