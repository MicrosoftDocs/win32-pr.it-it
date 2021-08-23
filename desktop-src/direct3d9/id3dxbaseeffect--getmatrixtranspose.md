---
description: Ottiene una matrice trasposta.
ms.assetid: 255c1e20-0a60-49eb-abaa-66a67322ce73
title: Metodo ID3DXBaseEffect::GetMatrixTranspose (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 59a23e8cde059446dea33d65f90dca9fb7cb2aaf41ab00949e02e34189420b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987781"
---
# <a name="id3dxbaseeffectgetmatrixtranspose-method"></a>Metodo ID3DXBaseEffect::GetMatrixTranspose

Ottiene una matrice trasposta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMatrixTranspose(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hParameter* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificatore univoco. Vedere [Handle (Direct3D 9).](handles.md)

</dd> <dt>

*pMatrix* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Restituisce una matrice trasposta. Vedere [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Una matrice trasposta contiene dati principali della colonna. ciò significa che ogni vettore è contenuto in una colonna.

Se la matrice di destinazione è più grande della matrice di origine, verranno riempiti solo gli elementi in alto a sinistra della matrice di destinazione e i componenti rimanenti della matrice di destinazione verranno impostati su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetMatrixTranspose**](id3dxbaseeffect--setmatrixtranspose.md)
</dt> </dl>

 

 




