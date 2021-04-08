---
description: Imposta una matrice di puntatori alle matrici nontransposed.
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: 'Metodo ID3DXBaseEffect:: SetMatrixPointerArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0f199c3db335dfc6b9966987678c07b4b3a22402
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969298"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a>Metodo ID3DXBaseEffect:: SetMatrixPointerArray

Imposta una matrice di puntatori alle matrici nontransposed.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
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

*ppMatrix* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***

Matrice di puntatori alle matrici nontransposed. Vedere [**D3DXMATRIX**](d3dxmatrix.md).

</dd> <dt>

*Numero* \[ di in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di matrici nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Una matrice nontransposed contiene dati principali della riga; ovvero ogni vettore è contenuto in una riga.

Se le matrici di destinazione sono più piccole delle matrici di origine, i componenti aggiuntivi delle matrici di origine verranno ignorati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetMatrixArray**](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
