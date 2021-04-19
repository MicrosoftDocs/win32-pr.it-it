---
description: Ottiene una descrizione della funzione.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: 'Metodo ID3DXBaseEffect:: GetFunctionDesc (D3DX9Effect. h)'
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
ms.openlocfilehash: 718960da7ff73f24f865fdacc09dfe55ff09a466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323602"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a>Metodo ID3DXBaseEffect:: GetFunctionDesc

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

*hFunction* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle di funzione. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXFUNCTION \_ desc**](d3dxfunction-desc.md)\***

Restituisce una descrizione della funzione. Vedere [**D3DXFUNCTION \_ desc**](d3dxfunction-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




