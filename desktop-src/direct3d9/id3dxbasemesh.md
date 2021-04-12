---
description: Le applicazioni utilizzano i metodi dell'interfaccia ID3DXBaseMesh per modificare ed eseguire query sugli oggetti mesh e mesh progressivi.
ms.assetid: ec4ccd77-e370-470c-9325-3d794a8f7f16
title: Interfaccia ID3DXBaseMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58029639852b30f5de357bb2643583615c45485c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355029"
---
# <a name="id3dxbasemesh-interface"></a>Interfaccia ID3DXBaseMesh

Le applicazioni utilizzano i metodi dell'interfaccia **ID3DXBaseMesh** per modificare ed eseguire query sugli oggetti mesh e mesh progressivi.

## <a name="members"></a>Membri

L'interfaccia **ID3DXBaseMesh** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXBaseMesh** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXBaseMesh** dispone di questi metodi.



| Metodo                                                                            | Descrizione                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxbasemesh--clonemesh.md)                                     | Clona una mesh usando un dichiaratore.<br/>                                                                                                                                                                          |
| [**CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)                               | Clona una mesh usando un codice FVF (Flexible Vertex Format).<br/>                                                                                                                                                   |
| [**ConvertAdjacencyToPointReps**](id3dxbasemesh--convertadjacencytopointreps.md) | Converte le informazioni adiacenza mesh in una matrice di rappresentanti punto.<br/>                                                                                                                                  |
| [**ConvertPointRepsToAdjacency**](id3dxbasemesh--convertpointrepstoadjacency.md) | Converte i dati rappresentativi del punto in informazioni adiacenza mesh.<br/>                                                                                                                                          |
| [**DrawSubset**](id3dxbasemesh--drawsubset.md)                                   | Disegna un subset di una mesh.<br/>                                                                                                                                                                                  |
| [**GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)                     | Genera un elenco di bordi della mesh, oltre a un elenco di visi che condividono ogni bordo.<br/>                                                                                                                            |
| [**GetAttributeTable**](id3dxbasemesh--getattributetable.md)                     | Recupera una tabella di attributi per una mesh o il numero di voci archiviate in una tabella di attributi per una mesh.<br/>                                                                                          |
| [**GetDeclaration**](id3dxbasemesh--getdeclaration.md)                           | Recupera una dichiarazione che descrive i vertici nella mesh.<br/>                                                                                                                                               |
| [**GetDevice**](id3dxbasemesh--getdevice.md)                                     | Recupera il dispositivo associato alla mesh.<br/>                                                                                                                                                             |
| [**GetFVF**](id3dxbasemesh--getfvf.md)                                           | Ottiene il valore del vertice della funzione fissa.<br/>                                                                                                                                                                      |
| [**GetIndexBuffer**](id3dxbasemesh--getindexbuffer.md)                           | Recupera i dati in un buffer di indice.<br/>                                                                                                                                                                     |
| [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md)               | Ottiene il numero di byte per vertice.<br/>                                                                                                                                                                       |
| [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)                                 | Recupera il numero di visi nella rete.<br/>                                                                                                                                                                 |
| [**GetNumVertices**](id3dxbasemesh--getnumvertices.md)                           | Recupera il numero di vertici nella rete.<br/>                                                                                                                                                              |
| [**GetOptions**](id3dxbasemesh--getoptions.md)                                   | Recupera le opzioni di mesh abilitate per questa mesh al momento della creazione.<br/>                                                                                                                                         |
| [**GetVertexBuffer**](id3dxbasemesh--getvertexbuffer.md)                         | Recupera il buffer dei vertici associato alla mesh.<br/>                                                                                                                                                      |
| [**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)                         | Blocca un buffer di indice e ottiene un puntatore alla memoria del buffer dell'indice.<br/>                                                                                                                                    |
| [**LockVertexBuffer**](id3dxbasemesh--lockvertexbuffer.md)                       | Blocca un buffer dei vertici e ottiene un puntatore alla memoria del buffer del vertice.<br/>                                                                                                                                   |
| [**UnlockIndexBuffer**](id3dxbasemesh--unlockindexbuffer.md)                     | Sblocca un buffer di indice.<br/>                                                                                                                                                                                   |
| [**UnlockVertexBuffer**](id3dxbasemesh--unlockvertexbuffer.md)                   | Sblocca un buffer del vertice.<br/>                                                                                                                                                                                   |
| [**UpdateSemantics**](id3dxbasemesh--updatesemantics.md)                         | Questo metodo consente all'utente di modificare la dichiarazione mesh senza modificare il layout dei dati del buffer del vertice. La chiamata è valida solo se il vecchio e il nuovo formato di dichiarazione hanno le stesse dimensioni del vertice.<br/> |



 

## <a name="remarks"></a>Commenti

Una mesh è un oggetto costituito da un set di visi poligonali. Una mesh definisce un set di vertici e un set di visi (i visi vengono definiti in termini di vertici e normali della mesh).

Il tipo LPD3DXBASEMESH è definito come puntatore all'interfaccia **ID3DXBaseMesh** .


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
