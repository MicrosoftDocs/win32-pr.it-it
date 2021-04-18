---
description: Un buffer mesh è un buffer che contiene i dati relativi a una mesh.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: Interfaccia ID3DX10MeshBuffer (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 42076393c3be5443688ec4db954131935b62f696
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322745"
---
# <a name="id3dx10meshbuffer-interface"></a>Interfaccia ID3DX10MeshBuffer

Un buffer mesh è un buffer che contiene i dati relativi a una mesh. Può contenere uno dei cinque tipi diversi di dati, ovvero i dati dei vertici, i dati di indice, i dati adiacenza, i dati degli attributi o i dati del punto rep. La struttura viene usata per accedere a questi cinque tipi di dati tramite le cinque API seguenti: [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh:: GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh:: GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)o [**ID3DX10Mesh:: GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).

## <a name="members"></a>Membri

L'interfaccia **ID3DX10MeshBuffer** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10MeshBuffer** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX10MeshBuffer** dispone di questi metodi.



| Metodo                                       | Descrizione                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [**GetSize**](id3dx10meshbuffer-getsize.md) | Ottiene le dimensioni in byte del buffer mesh.<br/>                      |
| [**Mappa**](id3dx10meshbuffer-map.md)         | Ottenere un puntatore alla memoria del buffer mesh per modificarne il contenuto.<br/> |
| [**Unmap**](id3dx10meshbuffer-unmap.md)     | Annullare un buffer.<br/>                                                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
