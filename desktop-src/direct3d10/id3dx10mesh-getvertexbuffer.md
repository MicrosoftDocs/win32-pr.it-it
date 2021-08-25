---
description: 'Metodo ID3DX10Mesh::GetVertexBuffer: recupera il vertex buffer associato alla mesh.'
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: Metodo ID3DX10Mesh::GetVertexBuffer (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 804ece9ca82fbdd8dc5778b888fecc4ca8fbc04b8fc45976b857b417343f4b32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069976"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a>Metodo ID3DX10Mesh::GetVertexBuffer

Recupera il buffer dei vertici associato alla mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iBuffer* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Buffer dei vertici da ottenere. Si tratta di un valore di indice.

</dd> <dt>

*ppVertexBuffer* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Buffer dei vertici. Vedere [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
