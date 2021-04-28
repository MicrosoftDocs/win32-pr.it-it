---
description: Metodo ID3DXMATRIXStack::RotateAxisLocal (D3dx9math.h) - Ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario.
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: Metodo ID3DXMATRIXStack::RotateAxisLocal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0bfcfd7301f90dcf49b03e7bbb3fd7e3b0de6c3e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093469"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a>Metodo ID3DXMATRIXStack::RotateAxisLocal (D3dx9math.h)

Ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pV* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore all'asse arbitrario di rotazione. Vedere [**D3DXVECTOR3**](d3dxvector3.md).

</dd> <dt>

*Angolo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Angolo di rotazione intorno all'asse arbitrario, espresso in radianti. Gli angoli vengono misurati in senso antiorario quando si cerca lungo l'asse arbitrario verso l'origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Commenti

Questo metodo aggiunge la rotazione allo stack di matrici con la matrice di rotazione calcolata simile alla seguente:


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Poiché la rotazione viene moltiplicata a sinistra nello stack della matrice, la rotazione è relativa allo spazio delle coordinate locale dell'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateAxis**](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRoll**](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
