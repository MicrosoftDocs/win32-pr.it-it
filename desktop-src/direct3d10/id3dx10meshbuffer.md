---
description: Un buffer mesh è un buffer che contiene i dati relativi a una mesh.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: Interfaccia ID3DX10MeshBuffer (D3DX10.h)
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
ms.openlocfilehash: a2aeabcd6dd3cc711636d0e275f76ab48537953671559e244cf341e270783fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540155"
---
# <a name="id3dx10meshbuffer-interface"></a>Interfaccia ID3DX10MeshBuffer

Un buffer mesh è un buffer che contiene i dati relativi a una mesh. Può contenere uno dei cinque diversi tipi di dati: dati dei vertici, dati dell'indice, dati di adicenza, dati di attributi o dati di punti. La struttura viene usata per accedere a queste cinque parti di dati tramite le cinque API [**seguenti: ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh::GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh::GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)o [**ID3DX10Mesh::GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).

## <a name="members"></a>Membri

**L'interfaccia ID3DX10MeshBuffer** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10MeshBuffer** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX10MeshBuffer** include questi metodi.



| Metodo                                       | Descrizione                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [**GetSize**](id3dx10meshbuffer-getsize.md) | Ottiene le dimensioni del buffer mesh, in byte.<br/>                      |
| [**Mappa**](id3dx10meshbuffer-map.md)         | Ottenere un puntatore alla memoria buffer mesh per modificarne il contenuto.<br/> |
| [**Unmap**](id3dx10meshbuffer-unmap.md)     | Annullare il mapping di un buffer.<br/>                                                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
