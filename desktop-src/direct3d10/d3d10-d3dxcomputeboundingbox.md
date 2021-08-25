---
description: "Funzione D3DXComputeBoundingBox (D3DX10math.h): calcola un rettangolo di selezione orientato all'asse delle coordinate."
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: Funzione D3DXComputeBoundingBox (D3DX10math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 30660e13dc726d9a1f5a1cd396b80298add58cc07d99bccd32709cba001311f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028721"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a>Funzione D3DXComputeBoundingBox (D3DX10math.h)

Calcola un rettangolo di selezione orientato all'asse delle coordinate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFirstPosition* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore alla prima posizione.

</dd> <dt>

*NumVertices* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di vertici.

</dd> <dt>

*dwStride* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero o numero di byte tra i vertici.

</dd> <dt>

*pMin* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a [**una struttura D3DXVECTOR3**](d3d10-d3dxvector3.md) che descrive l'angolo inferiore sinistro restituito del rettangolo di selezione.

</dd> <dt>

*pMax* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Puntatore a [**una struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che descrive l'angolo superiore destro restituito del rettangolo di selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10math.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
