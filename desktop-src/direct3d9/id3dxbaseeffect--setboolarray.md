---
description: Imposta una matrice di valori booleani.
ms.assetid: 920b3482-cc30-4ab2-bfce-59f03afe11da
title: 'Metodo ID3DXBaseEffect:: SetBoolArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 813259fc9fcca954c4d7a992c7542387be33bb6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322081"
---
# <a name="id3dxbaseeffectsetboolarray-method"></a>Metodo ID3DXBaseEffect:: SetBoolArray

Imposta una matrice di valori booleani.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hParameter,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*PB* \[ in\]
</dt> <dd>

Tipo: **const [**bool**](../winprog/windows-data-types.md) \***

Matrice di valori booleani.

</dd> <dt>

*Numero* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di valori booleani nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetBoolArray**](id3dxbaseeffect--getboolarray.md)
</dt> </dl>

 

 
