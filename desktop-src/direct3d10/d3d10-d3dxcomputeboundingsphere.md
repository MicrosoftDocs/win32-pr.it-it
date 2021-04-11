---
description: Calcola un ambito di delimitazione per la mesh.
ms.assetid: 54f486d2-45e9-4fc1-90a3-97488ed4d900
title: Funzione D3DXComputeBoundingSphere (D3DX10math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0c8e59b4d39652d02ce19f4c1bf6b0617fee7772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235142"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a>Funzione D3DXComputeBoundingSphere (D3DX10math. h)

Calcola un ambito di delimitazione per la mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFirstPosition* \[ in\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Puntatore alla prima posizione.

</dd> <dt>

*NumVertices* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di vertici.

</dd> <dt>

*dwStride* \[ in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Numero di byte tra i vettori di posizione.

</dd> <dt>

*pCenter* \[ in\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , che definisce il centro delle coordinate della sfera di delimitazione restituita.

</dd> <dt>

*pRadius* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Raggio della sfera di delimitazione restituita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10math. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni mesh](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
