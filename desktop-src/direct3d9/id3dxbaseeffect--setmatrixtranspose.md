---
description: 'Metodo ID3DXBaseEffect::SetMatrixTranspose: imposta una matrice trasposta.'
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: Metodo ID3DXBaseEffect::SetMatrixTranspose (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d516d9fc5a92ff3661caaf5fbca17372804ea2805688542a0283736cf55f4959
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790671"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a>Metodo ID3DXBaseEffect::SetMatrixTranspose

Imposta una matrice trasposta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [Handle (Direct3D 9).](handles.md)

</dd> <dt>

*pMatrix* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntatore a una matrice trasposta. Vedere [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Una matrice trasposta contiene dati principali della colonna. ciò significa che ogni vettore è contenuto in una colonna.

Se la matrice di destinazione è più piccola della matrice di origine, i componenti aggiuntivi della matrice di origine verranno ignorati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetMatrixTranspose**](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




