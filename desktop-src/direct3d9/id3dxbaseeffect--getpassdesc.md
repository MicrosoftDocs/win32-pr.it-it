---
description: Ottiene una descrizione del passaggio.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'Metodo ID3DXBaseEffect:: GetPassDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 15a997470fddf5056b7191fcc3226ad210724041
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323590"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a>Metodo ID3DXBaseEffect:: GetPassDesc

Ottiene una descrizione del passaggio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPass* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Handle di pass. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXPASS \_ desc**](d3dxpass-desc.md)\***

Restituisce una descrizione del passaggio specificato. Vedere [**D3DXPASS \_ desc**](d3dxpass-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

> [!Note]  
> Se viene creato un effetto con [D3DXFX \_ non \_ clonabile](d3dxfx.md), questo metodo restituirà puntatori **null** (in [**D3DXPASS \_ desc**](d3dxpass-desc.md)) alle funzioni dello shader.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




