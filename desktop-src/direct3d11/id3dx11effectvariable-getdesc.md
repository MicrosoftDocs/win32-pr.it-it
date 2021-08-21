---
title: Metodo ID3DX11EffectVariable GetDesc (D3dx11effect.h)
description: Ottenere una descrizione.
ms.assetid: bf6339d7-8eb0-44da-893e-c805309a3cd3
keywords:
- Metodo GetDesc Direct3D 11
- Metodo GetDesc Direct3D 11, interfaccia ID3DX11EffectVariable
- INTERFACCIA ID3DX11EffectVariable Direct3D 11, metodo GetDesc
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
ms.openlocfilehash: da4c4ac66c8cafee3636491513ba7a70c19be752c6d0769902bb91e771487177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531117"
---
# <a name="id3dx11effectvariablegetdesc-method"></a>Metodo ID3DX11EffectVariable::GetDesc

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

Tipo: **[ **D3DX11 \_ EFFECT \_ VARIABLE \_ DESC**](d3dx11-effect-variable-desc.md)\***

Puntatore a una descrizione della variabile di effetto (vedere [**D3DX11 \_ EFFECT \_ VARIABLE \_ DESC).**](d3dx11-effect-variable-desc.md)

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

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





