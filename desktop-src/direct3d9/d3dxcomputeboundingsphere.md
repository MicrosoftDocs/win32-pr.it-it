---
description: 'Funzione D3DXComputeBoundingSphere (D3DX9Mesh.h): calcola una sfera di delimitazione per la mesh.'
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: Funzione D3DXComputeBoundingSphere (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c0eee5def85163e75f90a8eeb6a063876e19c49b4997abb38d387a2f05c0a8fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857421"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a>Funzione D3DXComputeBoundingSphere (D3DX9Mesh.h)

Calcola una sfera di delimitazione per la mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
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

Numero di byte tra i vettori di posizione. Usare [**GetNumBytesPerVertex,**](id3dxbasemesh--getnumbytespervertex.md) [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)o [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) per ottenere lo stride del vertice.

</dd> <dt>

*pCenter* \[ Cambio\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

[**Struttura D3DXVECTOR3,**](d3dxvector3.md) che definisce il centro delle coordinate della sfera di delimitazione restituita.

</dd> <dt>

*pRadius* \[ Cambio\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Raggio della sfera di delimitazione restituita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
