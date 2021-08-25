---
description: Questa interfaccia incapsula la funzionalità patch mesh.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: Interfaccia ID3DXPatchMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44899ccee6f13aa25b01e284df5a892196d657610c3f89d546fc0b646eeaa069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856281"
---
# <a name="id3dxpatchmesh-interface"></a>Interfaccia ID3DXPatchMesh

Questa interfaccia incapsula la funzionalità patch mesh.

## <a name="members"></a>Membri

**L'interfaccia ID3DXPatchMesh** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXPatchMesh** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXPatchMesh** include questi metodi.



| Metodo                                                                           | Descrizione                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxpatchmesh--clonemesh.md)                                   | Crea una nuova mesh di patch con la dichiarazione di vertice specificata.<br/>                      |
| [**GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)                   | Generare un elenco di bordi di mesh e le patch che condividono ogni bordo.<br/>                  |
| [**GetControlVerticesPerPatch**](id3dxpatchmesh--getcontrolverticesperpatch.md) | Ottiene il numero di vertici di controllo per patch.<br/>                                       |
| [**GetDeclaration**](id3dxpatchmesh--getdeclaration.md)                         | Ottiene la dichiarazione del vertice.<br/>                                                         |
| [**GetDevice**](id3dxpatchmesh--getdevice.md)                                   | Ottiene il dispositivo che ha creato la mesh.<br/>                                               |
| [**GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)                     | Ottiene i parametri di spostamento della geometria mesh.<br/>                                          |
| [**GetIndexBuffer**](id3dxpatchmesh--getindexbuffer.md)                         | Ottiene la rete index buffer.<br/>                                                          |
| [**GetNumPatches**](id3dxpatchmesh--getnumpatches.md)                           | Ottiene il numero di patch nella mesh.<br/>                                              |
| [**GetNumVertices**](id3dxpatchmesh--getnumvertices.md)                         | Ottiene il numero di vertici nella mesh.<br/>                                             |
| [**GetOptions**](id3dxpatchmesh--getoptions.md)                                 | Ottiene il tipo di patch.<br/>                                                              |
| [**GetPatchInfo**](id3dxpatchmesh--getpatchinfo.md)                             | Ottiene gli attributi della patch.<br/>                                                    |
| [**GetTessSize**](id3dxpatchmesh--gettesssize.md)                               | Ottiene le dimensioni della mesh a tessellazione, dato un livello a trama.<br/>                   |
| [**GetVertexBuffer**](id3dxpatchmesh--getvertexbuffer.md)                       | Ottiene il buffer dei vertici della mesh.<br/>                                                         |
| [**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)               | Blocca il buffer dell'attributo.<br/>                                                          |
| [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)                       | Bloccare il index buffer.<br/>                                                               |
| [**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)                     | Bloccare il buffer dei vertici.<br/>                                                              |
| [**Ottimizzazione**](id3dxpatchmesh--optimize.md)                                     | Ottimizza la mesh di patch per un'efficiente applicazione a più elementi.<br/>                                 |
| [**SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)                     | Imposta i parametri di spostamento della geometria mesh.<br/>                                          |
| [**A tessellate**](id3dxpatchmesh--tessellate.md)                                 | Esegue un'operazione a più livelli uniforme in base al livello a più livelli.<br/>                       |
| [**TessellateAdaptive**](id3dxpatchmesh--tessellateadaptive.md)                 | Esegue il tessellamento adattivo in base al criterio a tessellazione adattiva basato su z.<br/> |
| [**UnlockAttributeBuffer**](id3dxpatchmesh--unlockattributebuffer.md)           | Sbloccare il buffer dell'attributo.<br/>                                                         |
| [**UnlockIndexBuffer**](id3dxpatchmesh--unlockindexbuffer.md)                   | Sbloccare il index buffer.<br/>                                                             |
| [**UnlockVertexBuffer**](id3dxpatchmesh--unlockvertexbuffer.md)                 | Sbloccare il buffer dei vertici.<br/>                                                            |



 

## <a name="remarks"></a>Commenti

Una mesh di patch è una mesh costituita da una serie di patch.

Per ottenere **l'interfaccia ID3DXPatchMesh,** chiamare [**la funzione D3DXCreatePatchMesh.**](d3dxcreatepatchmesh.md)

Il tipo LPD3DXPATCHMESH viene definito come puntatore **all'interfaccia ID3DXPatchMesh,** come indicato di seguito:


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
