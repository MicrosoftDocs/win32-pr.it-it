---
description: Per modificare gli oggetti mesh, le applicazioni utilizzano i metodi dell'interfaccia ID3DX10Mesh.
ms.assetid: 1734b8fd-e1a6-4aa4-96a0-8693019a9dac
title: Interfaccia ID3DX10Mesh (D3DX10. h)
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
ms.openlocfilehash: 2ddf0876928f85debded1645b9a22de790917017
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323677"
---
# <a name="id3dx10mesh-interface"></a>Interfaccia ID3DX10Mesh

Per modificare gli oggetti mesh, le applicazioni utilizzano i metodi dell'interfaccia ID3DX10Mesh.

## <a name="members"></a>Membri

L'interfaccia **ID3DX10Mesh** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10Mesh** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX10Mesh** dispone di questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dx10mesh-clonemesh.md)                                               | Crea una nuova mesh e la riempie con i dati di una mesh precedentemente caricata.<br/>                                                                                                                                                                                                                                                |
| [**CommitToDevice**](id3dx10mesh-committodevice.md)                                     | Eseguire il commit di tutte le modifiche apportate a una mesh al dispositivo, in modo che sia possibile eseguire il rendering delle modifiche. Questa operazione deve essere chiamata dopo che i dati di una mesh vengono modificati e prima che ne venga eseguito il rendering. Non è possibile eseguire il rendering di una mesh a meno che non ne venga eseguito il commit nel dispositivo. Vedere la sezione Osservazioni.<br/>                                                                         |
| [**Discard**](id3dx10mesh-discard.md)                                                   | Rimuove i dati mesh dal dispositivo di cui è stato eseguito il commit nel dispositivo (con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md)).<br/>                                                                                                                                                                         |
| [**DrawSubset**](id3dx10mesh-drawsubset.md)                                             | Disegna un subset di una mesh.<br/>                                                                                                                                                                                                                                                                                                 |
| [**DrawSubsetInstanced**](id3dx10mesh-drawsubsetinstanced.md)                           | Creare diverse istanze dello stesso subset di una mesh.<br/>                                                                                                                                                                                                                                                                      |
| [**GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md)       | Genera un elenco di bordi della mesh, oltre a un elenco di visi che condividono ogni bordo.<br/>                                                                                                                                                                                                                                           |
| [**GenerateAttributeBufferFromTable**](id3dx10mesh-generateattributebufferfromtable.md) | Generare un buffer di attributi dai dati nella tabella degli attributi della mesh. Un buffer di attributo è un altro formato per l'archiviazione dei dati nella tabella degli attributi. Sia il buffer dell'attributo che la tabella di attributi sono strutture di dati interne nella rete.<br/>                                                                  |
| [**GenerateGSAdjacency**](id3dx10mesh-generategsadjacency.md)                           | Aggiunge i dati di adiacenza al buffer di indice della mesh. Quando la mesh deve essere inviata a un geometry shader che accetta i dati di adiacenza, è necessario che il buffer di indice della mesh contenga i dati adiacenza.<br/>                                                                                                                       |
| [**GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md)                             | Accedere al buffer adiacenza della mesh.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)                             | Accedere al buffer dell'attributo della mesh.<br/>                                                                                                                                                                                                                                                                                       |
| [**GetAttributeTable**](id3dx10mesh-getattributetable.md)                               | Recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.<br/>                                                                                                                                                                                                         |
| [**GetDeviceIndexBuffer**](id3dx10mesh-getdeviceindexbuffer.md)                         | Accedere al buffer di indice della mesh dopo che è stato eseguito il commit nel dispositivo con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md). Questa operazione è diversa da [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), che restituisce il buffer dell'indice prima che sia stato eseguito il commit nel dispositivo.<br/>     |
| [**GetDeviceVertexBuffer**](id3dx10mesh-getdevicevertexbuffer.md)                       | Accedere al buffer dei vertici della mesh dopo che è stato eseguito il commit nel dispositivo con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md). Questa operazione è diversa da [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), che restituisce il buffer dei vertici prima che sia stato eseguito il commit nel dispositivo.<br/> |
| [**GetFaceCount**](id3dx10mesh-getfacecount.md)                                         | Recupera il numero di visi nella rete.<br/>                                                                                                                                                                                                                                                                                |
| [**GetFlags**](id3dx10mesh-getflags.md)                                                 | Accedere ai flag di creazione della rete.<br/>                                                                                                                                                                                                                                                                                         |
| [**GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)                                     | Recupera i dati in un buffer di indice.<br/>                                                                                                                                                                                                                                                                                    |
| [**GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md)                               | Ottiene il buffer Rep del punto della rete.<br/>                                                                                                                                                                                                                                                                                          |
| [**GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)                                   | Recupera il buffer dei vertici associato alla mesh.<br/>                                                                                                                                                                                                                                                                     |
| [**GetVertexBufferCount**](id3dx10mesh-getvertexbuffercount.md)                         | Ottenere il numero di buffer dei vertici nella rete.<br/>                                                                                                                                                                                                                                                                             |
| [**GetVertexCount**](id3dx10mesh-getvertexcount.md)                                     | Ottenere il numero di vertici nella rete. Una mesh può contenere più buffer di vertice (ad esempio, un buffer di vertice può contenere tutti i dati di posizione, un altro può contenere tutti i dati delle coordinate di trama e così via), tuttavia ogni buffer di vertici conterrà lo stesso numero di elementi.<br/>                                                   |
| [**GetVertexDescription**](id3dx10mesh-getvertexdescription.md)                         | Accedere alla descrizione del vertice passata a [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md). La descrizione del vertice descrive il layout dei buffer dei vertici della mesh.<br/>                                                                                                                                                   |
| [**Intersect**](id3dx10mesh-intersect.md)                                               | Determina se un raggio si interseca con la mesh.<br/>                                                                                                                                                                                                                                                                            |
| [**IntersectSubset**](id3dx10mesh-intersectsubset.md)                                   | Determina se un raggio si interseca con un subset di questa mesh.<br/>                                                                                                                                                                                                                                                                |
| [**Ottimizzare**](id3dx10mesh-optimize.md)                                                 | Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.<br/>                                                                                                                                                                                                                                   |
| [**SetAdjacencyData**](id3dx10mesh-setadjacencydata.md)                                 | Imposta i dati adiacenza della mesh.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeData**](id3dx10mesh-setattributedata.md)                                 | Imposta i dati dell'attributo della mesh.<br/>                                                                                                                                                                                                                                                                                            |
| [**SetAttributeTable**](id3dx10mesh-setattributetable.md)                               | Imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.<br/>                                                                                                                                                                                                                                        |
| [**SetIndexData**](id3dx10mesh-setindexdata.md)                                         | Imposta i dati dell'indice della mesh.<br/>                                                                                                                                                                                                                                                                                                |
| [**SetPointRepData**](id3dx10mesh-setpointrepdata.md)                                   | Imposta i dati della Rep del punto per la mesh.<br/>                                                                                                                                                                                                                                                                                      |
| [**SetVertexData**](id3dx10mesh-setvertexdata.md)                                       | Impostare i dati dei vertici in uno dei buffer dei vertici della mesh.<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Per ottenere l'interfaccia ID3DX10Mesh, chiamare [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
