---
description: Ottiene una matrice nontransposed.
ms.assetid: d507c82c-b1a5-4e83-8921-5d45f52faba0
title: 'Metodo ID3DXBaseEffect:: getMatrix (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 17d59700d8752526f3f4c48efeaf7f3e6bd985bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323600"
---
# <a name="id3dxbaseeffectgetmatrix-method"></a>Metodo ID3DXBaseEffect:: getMatrix

Ottiene una matrice nontransposed.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMatrix(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
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

Restituisce una matrice nontransposed. Vedere [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Una matrice nontransposed contiene dati principali della riga; ovvero ogni vettore è contenuto in una riga.

Se la matrice di destinazione è più grande della matrice di origine, verranno riempiti solo i componenti in alto a sinistra della matrice di destinazione e i componenti rimanenti verranno impostati su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**Sematrix**](id3dxbaseeffect--setmatrix.md)
</dt> </dl>

 

 




