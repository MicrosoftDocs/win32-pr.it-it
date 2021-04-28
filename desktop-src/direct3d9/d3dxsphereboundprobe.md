---
description: 'Funzione D3DXSphereBoundProbe (D3DX9Mesh.h): determina se un raggio interseca il volume del rettangolo di selezione di una sfera.'
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: Funzione D3DXSphereBoundProbe (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2d3ea263d7ad8bc50b936fd1010c352c0c01783
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093849"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a>Funzione D3DXSphereBoundProbe (D3DX9Mesh.h)

Determina se un raggio interseca il volume del rettangolo di selezione di una sfera.

## <a name="syntax"></a>Sintassi


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCenter* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica la coordinata centrale della sfera.

</dd> <dt>

*Raggio* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Raggio della sfera.

</dd> <dt>

*pRayPosition* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica la coordinata di origine del raggio.

</dd> <dt>

*pRayDirection* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che specifica la direzione del raggio. Questo vettore non deve essere (0,0,0), ma non deve essere normalizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Restituisce **TRUE** se il raggio interseca il volume del rettangolo di selezione della sfera. In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

**D3DXSphereBoundProbe** determina se il raggio interseca il volume del rettangolo di selezione della sfera, non solo la superficie della sfera.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
