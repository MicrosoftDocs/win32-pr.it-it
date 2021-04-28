---
description: 'Metodo ID3DXBaseEffect::SetMatrixTransposeArray: imposta una matrice di matrici trasposte.'
ms.assetid: 5dc65424-b0cd-490d-900e-60b9f7536ace
title: Metodo ID3DXBaseEffect::SetMatrixTransposeArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7f145dc45f053e208f7890c8afdac6422ecde13
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097509"
---
# <a name="id3dxbaseeffectsetmatrixtransposearray-method"></a>Metodo ID3DXBaseEffect::SetMatrixTransposeArray

Imposta una matrice di matrici trasposte.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMatrixTransposeArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [Handle (Direct3D 9)](handles.md).

</dd> <dt>

*pMatrix* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Matrice di matrici trasposte. Vedere [**D3DXMATRIX**](d3dxmatrix.md).

</dd> <dt>

*Conteggio* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di matrici nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Una matrice trasposta contiene dati principali della colonna. in altri, ogni vettore è contenuto in una colonna.

Se le matrici di destinazione sono più piccole delle matrici di origine, i componenti aggiuntivi delle matrici di origine verranno ignorati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetMatrixTransposeArray**](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
