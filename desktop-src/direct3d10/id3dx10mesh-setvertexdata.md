---
description: Impostare i dati dei vertici in uno dei buffer dei vertici della mesh.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: Metodo ID3DX10Mesh::SetVertexData (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59dc5292d5d5dfc269f97f2a8d19ce9a19ea95ceefda47eaf89ac77f81838f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990331"
---
# <a name="id3dx10meshsetvertexdata-method"></a>Metodo ID3DX10Mesh::SetVertexData

Impostare i dati dei vertici in uno dei buffer dei vertici della mesh.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iBuffer* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Buffer dei vertici da riempire con pData.

</dd> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Tipo: **const \* void**

Dati del vertice da impostare.

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

 

 
