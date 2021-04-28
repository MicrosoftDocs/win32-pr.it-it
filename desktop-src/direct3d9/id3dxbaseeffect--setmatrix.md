---
description: 'Metodo ID3DXBaseEffect::SetMatrix: imposta una matrice non trasposta.'
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: Metodo ID3DXBaseEffect::SetMatrix (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7af7dc0daa3dcd29e7b15c4fe435b9626ea41746
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097499"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a>Metodo ID3DXBaseEffect::SetMatrix

Imposta una matrice non trasposta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
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

Puntatore a una matrice non trasposta. Vedere [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Una matrice non trasposta contiene dati principali di riga. In altre parole, ogni vettore è contenuto in una riga.

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

[**GetMatrix**](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




