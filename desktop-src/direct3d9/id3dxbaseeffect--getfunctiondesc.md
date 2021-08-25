---
description: Ottiene una descrizione della funzione.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: Metodo ID3DXBaseEffect::GetFunctionDesc (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b8f74715b163b3d197f62274c6aa6bf52ae872254db9df8225e061dc54900964
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893721"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a>Metodo ID3DXBaseEffect::GetFunctionDesc

Ottiene una descrizione della funzione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFunction* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle di funzione. Vedere [Handle (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md)\***

Restituisce una descrizione della funzione. Vedere [**D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




