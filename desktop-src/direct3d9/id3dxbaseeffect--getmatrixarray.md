---
description: Ottiene una matrice di matrici nontransposed.
ms.assetid: 37b08f55-22f1-4b60-8cd4-566a77e7dbd6
title: 'Metodo ID3DXBaseEffect:: GetMatrixArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 242b3c42976f9bfe4ad8ecad4d965c473839ffdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323599"
---
# <a name="id3dxbaseeffectgetmatrixarray-method"></a>Metodo ID3DXBaseEffect:: GetMatrixArray

Ottiene una matrice di matrici nontransposed.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMatrixArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [handle (Direct3D 9)](handles.md).

</dd> <dt>

*pmatrix* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Restituisce una matrice di matrici nontransposed. Vedere [**D3DXMATRIX**](d3dxmatrix.md).

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

Se le matrici di destinazione sono più grandi delle matrici di origine, verranno riempiti solo i componenti in alto a sinistra di ogni matrice di destinazione e i componenti della matrice di destinazione rimanenti verranno impostati su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetMatrixArray**](id3dxbaseeffect--setmatrixarray.md)
</dt> </dl>

 

 
