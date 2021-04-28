---
description: Metodo ID3DXMATRIXStack::RotateYawPitchRollLocal (D3DX10.h) - Ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario.
ms.assetid: da023816-5176-460d-ab6b-909b89cc46cd
title: Metodo ID3DXMATRIXStack::RotateYawPitchRollLocal (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRollLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 726a6d7092b95f53d17625f68884b92d347de3a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107839"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx10h"></a>Metodo ID3DXMATRIXStack::RotateYawPitchRollLocal (D3DX10.h)

Ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Yaw* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Yaw intorno all'asse y in radianti.

</dd> <dt>

*Pitch* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Passo intorno all'asse x in radianti.

</dd> <dt>

*Roll* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Rotazione intorno all'asse z in radianti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo aggiunge la rotazione allo stack di matrici con la matrice di rotazione calcolata simile alla seguente:


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Poiché la rotazione viene moltiplicata a sinistra nello stack della matrice, la rotazione è relativa allo spazio delle coordinate locale dell'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
