---
description: "Funzione D3DXComputeBoundingBox (D3DX9Mesh.h): calcola un rettangolo di selezione orientato all'asse delle coordinate."
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: Funzione D3DXComputeBoundingBox (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03eb722e68b58ec48a3bf607ab72d67004ad30a0c765b19c1b84ae29577c773b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299953"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a>Funzione D3DXComputeBoundingBox (D3DX9Mesh.h)

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

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

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

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che descrive l'angolo inferiore sinistro restituito del rettangolo di selezione. Vedere la sezione Osservazioni.

</dd> <dt>

*pMax* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che descrive l'angolo superiore destro restituito del rettangolo di selezione. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
