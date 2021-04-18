---
description: Ottenere il numero di vertici nella rete.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'Metodo ID3DX10Mesh:: GetVertexCount (D3DX10. h)'
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
ms.openlocfilehash: 189be6ff6872cfb85c2f336c29dedef2e435382e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323144"
---
# <a name="id3dx10meshgetvertexcount-method"></a>Metodo ID3DX10Mesh:: GetVertexCount

Ottenere il numero di vertici nella rete. Una mesh può contenere più buffer di vertice (ad esempio, un buffer di vertice può contenere tutti i dati di posizione, un altro può contenere tutti i dati delle coordinate di trama e così via), tuttavia ogni buffer di vertici conterrà lo stesso numero di elementi.

## <a name="syntax"></a>Sintassi


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di vertici nella rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
