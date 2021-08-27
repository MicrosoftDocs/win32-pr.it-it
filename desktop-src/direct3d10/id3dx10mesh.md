---
description: Le applicazioni usano i metodi dell'interfaccia ID3DX10Mesh per modificare gli oggetti mesh.
ms.assetid: 1734b8fd-e1a6-4aa4-96a0-8693019a9dac
title: Interfaccia ID3DX10Mesh (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2506191db941eee0a046d52f64aaeeb0f642f11dd35e42d6b49c4b5f5f457d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096651"
---
# <a name="id3dx10mesh-interface"></a>Interfaccia ID3DX10Mesh

Le applicazioni usano i metodi dell'interfaccia ID3DX10Mesh per modificare gli oggetti mesh.

## <a name="members"></a>Membri

**L'interfaccia ID3DX10Mesh** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10Mesh** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX10Mesh** include questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dx10mesh-clonemesh.md)                                               | Crea una nuova mesh e la riempie con i dati di una mesh caricata in precedenza.<br/>                                                                                                                                                                                                                                                |
| [**CommitToDevice**](id3dx10mesh-committodevice.md)                                     | Eseguire il commit di tutte le modifiche apportate a una mesh nel dispositivo in modo che sia possibile eseguire il rendering delle modifiche. Questo metodo deve essere chiamato dopo che i dati di una mesh sono stati modificati e prima che ne venga eseguito il rendering. Non è possibile eseguire il rendering di una mesh a meno che non ne venga eseguito il commit nel dispositivo. Vedere la sezione Osservazioni.<br/>                                                                         |
| [**Scartare**](id3dx10mesh-discard.md)                                                   | Rimuove i dati mesh dal dispositivo di cui è stato eseguito il commit (con [**ID3DX10Mesh::CommitToDevice).**](id3dx10mesh-committodevice.md)<br/>                                                                                                                                                                         |
| [**DrawSubset**](id3dx10mesh-drawsubset.md)                                             | Disegna un subset di una mesh.<br/>                                                                                                                                                                                                                                                                                                 |
| [**DrawSubsetInstanced**](id3dx10mesh-drawsubsetinstanced.md)                           | Disegnare diverse istanze dello stesso subset di una mesh.<br/>                                                                                                                                                                                                                                                                      |
| [**GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md)       | Generare un elenco di bordi di mesh, nonché un elenco di visi che condividono ogni bordo.<br/>                                                                                                                                                                                                                                           |
| [**GenerateAttributeBufferFromTable**](id3dx10mesh-generateattributebufferfromtable.md) | Generare un buffer dell'attributo dai dati nella tabella degli attributi della mesh. Un buffer di attributi è un altro formato per l'archiviazione dei dati nella tabella degli attributi. Sia il buffer dell'attributo che la tabella degli attributi sono strutture di dati interne nella mesh.<br/>                                                                  |
| [**GenerateGSAdjacency**](id3dx10mesh-generategsadjacency.md)                           | Aggiunge i dati di adizia alla rete index buffer. Quando la mesh deve essere inviata a un geometry shader che accetta dati di adizia, è necessario che l'index buffer della mesh contenga dati di adienza.<br/>                                                                                                                       |
| [**GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md)                             | Accedere al buffer di adienze della mesh.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)                             | Accedere al buffer degli attributi della mesh.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeTable**](id3dx10mesh-getattributetable.md)                               | Recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.<br/>                                                                                                                                                                                                         |
| [**GetDeviceIndexBuffer**](id3dx10mesh-getdeviceindexbuffer.md)                         | Accedere alla rete index buffer dopo che è stato eseguito il commit nel dispositivo con [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md). Questo è diverso da [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), che restituisce il index buffer prima che ne sia stato eseguito il commit nel dispositivo.<br/>     |
| [**GetDeviceVertexBuffer**](id3dx10mesh-getdevicevertexbuffer.md)                       | Accedere al buffer dei vertici della mesh dopo che è stato eseguito il commit nel dispositivo con [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md). Questa operazione è diversa da [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), che restituisce il buffer dei vertici prima che ne sia stato eseguito il commit nel dispositivo.<br/> |
| [**GetFaceCount**](id3dx10mesh-getfacecount.md)                                         | Recupera il numero di visi nella mesh.<br/>                                                                                                                                                                                                                                                                                |
| [**GetFlags**](id3dx10mesh-getflags.md)                                                 | Accedere ai flag di creazione della mesh.<br/>                                                                                                                                                                                                                                                                                         |
| [**GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)                                     | Recupera i dati in un index buffer.<br/>                                                                                                                                                                                                                                                                                    |
| [**GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md)                               | Ottenere il buffer del punto della mesh.<br/>                                                                                                                                                                                                                                                                                          |
| [**GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)                                   | Recupera il buffer dei vertici associato alla mesh.<br/>                                                                                                                                                                                                                                                                     |
| [**GetVertexBufferCount**](id3dx10mesh-getvertexbuffercount.md)                         | Ottiene il numero di buffer dei vertici nella mesh.<br/>                                                                                                                                                                                                                                                                             |
| [**GetVertexCount**](id3dx10mesh-getvertexcount.md)                                     | Ottenere il numero di vertici nella mesh. Una mesh può contenere più buffer dei vertici(ad esempio, un buffer dei vertici può contenere tutti i dati di posizione, un altro può contenere tutti i dati delle coordinate di trama e così via), tuttavia ogni buffer dei vertici conterrà lo stesso numero di elementi.<br/>                                                   |
| [**GetVertexDescription**](id3dx10mesh-getvertexdescription.md)                         | Accedere alla descrizione del vertice passata in [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md). La descrizione del vertice descrive il layout dei buffer dei vertici della mesh.<br/>                                                                                                                                                   |
| [**Intersect**](id3dx10mesh-intersect.md)                                               | Determina se un raggio si interseca con questa mesh.<br/>                                                                                                                                                                                                                                                                            |
| [**IntersectSubset**](id3dx10mesh-intersectsubset.md)                                   | Determina se un raggio si interseca con un subset di questa mesh.<br/>                                                                                                                                                                                                                                                                |
| [**Ottimizzazione**](id3dx10mesh-optimize.md)                                                 | Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni di disegno.<br/>                                                                                                                                                                                                                                   |
| [**SetAdjacencyData**](id3dx10mesh-setadjacencydata.md)                                 | Impostare i dati di adizia della mesh.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeData**](id3dx10mesh-setattributedata.md)                                 | Impostare i dati dell'attributo della mesh.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeTable**](id3dx10mesh-setattributetable.md)                               | Imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.<br/>                                                                                                                                                                                                                                        |
| [**SetIndexData**](id3dx10mesh-setindexdata.md)                                         | Impostare i dati dell'indice della mesh.<br/>                                                                                                                                                                                                                                                                                                |
| [**SetPointRepData**](id3dx10mesh-setpointrepdata.md)                                   | Impostare i dati del punto per la mesh.<br/>                                                                                                                                                                                                                                                                                      |
| [**SetVertexData**](id3dx10mesh-setvertexdata.md)                                       | Impostare i dati dei vertici in uno dei buffer dei vertici della mesh.<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Per ottenere l'interfaccia ID3DX10Mesh, chiamare [**D3DX10CreateMesh.**](d3d10-d3dx10createmesh.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
