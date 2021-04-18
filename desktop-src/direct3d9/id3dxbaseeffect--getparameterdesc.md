---
description: Ottiene una descrizione del parametro o dell'annotazione.
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: 'Metodo ID3DXBaseEffect:: GetParameterDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c3a52c06ebed764b3ab1718488c2dbc55ceda41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323595"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a>Metodo ID3DXBaseEffect:: GetParameterDesc

Ottiene una descrizione del parametro o dell'annotazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Parametro o handle di annotazione. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXPARAMETER \_ desc**](d3dxparameter-desc.md)\***

Restituisce una descrizione del parametro o dell'annotazione specificato. Vedere [**D3DXPARAMETER \_ desc**](d3dxparameter-desc.md).

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

 

 




