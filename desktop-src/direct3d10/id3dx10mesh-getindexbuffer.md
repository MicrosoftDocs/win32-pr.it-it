---
description: 'Metodo ID3DX10Mesh::GetIndexBuffer: recupera i dati in un index buffer.'
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: Metodo ID3DX10Mesh::GetIndexBuffer (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 03babe487bfd28048f726590ce567ac191c6cd3cf737daecc4853afaa53e535d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046919"
---
# <a name="id3dx10meshgetindexbuffer-method"></a>Metodo ID3DX10Mesh::GetIndexBuffer

Recupera i dati in un index buffer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppIndexBuffer* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Indirizzo di un puntatore a un'interfaccia ID3DX10MeshBuffer, che rappresenta il index buffer associato alla mesh.

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

 

 




