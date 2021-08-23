---
description: Ottiene il numero di vertici nella mesh.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: Metodo ID3DX10Mesh::GetVertexCount (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00fd0cd84aedb32e2da567a92ffc421f41394a991872f9216b06a4f28f895183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566891"
---
# <a name="id3dx10meshgetvertexcount-method"></a>Metodo ID3DX10Mesh::GetVertexCount

Ottiene il numero di vertici nella mesh. Una mesh può contenere più vertex buffer(ad esempio, un buffer vertice può contenere tutti i dati di posizione, un altro può contenere tutti i dati delle coordinate di trama e così via), tuttavia ogni buffer dei vertici conterrà lo stesso numero di elementi.

## <a name="syntax"></a>Sintassi


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Numero di vertici nella mesh.

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

 

 
