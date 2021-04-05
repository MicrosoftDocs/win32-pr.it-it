---
description: Imposta una matrice di matrici trasposte.
ms.assetid: 100288f2-44f0-4e75-bffb-78732c50a55c
title: 'Metodo ID3DXTextureShader:: SetMatrixTransposeArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c9efd0c81cef8a72880a9755ca40e4dd8b4950ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969332"
---
# <a name="id3dxtextureshadersetmatrixtransposearray-method"></a>Metodo ID3DXTextureShader:: SetMatrixTransposeArray

Imposta una matrice di matrici trasposte.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConstant* \[ in\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco della matrice di costanti della matrice. Vedere [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pmatrix* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matrice di matrici trasposte. Vedere [**D3DXMATRIX**](d3dxmatrix.md).

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

Una matrice trasposta contiene dati di colonne principali; ovvero ogni vettore è contenuto in una colonna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
