---
description: Questa interfaccia incapsula la funzionalità di patch mesh.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: Interfaccia ID3DXPatchMesh (D3DX9Mesh. h)
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
ms.openlocfilehash: f1f13e6abe3a164e8027ddcb6bb33e9f0ca618fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355209"
---
# <a name="id3dxpatchmesh-interface"></a>Interfaccia ID3DXPatchMesh

Questa interfaccia incapsula la funzionalità di patch mesh.

## <a name="members"></a>Membri

L'interfaccia **ID3DXPatchMesh** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPatchMesh** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXPatchMesh** dispone di questi metodi.



| Metodo                                                                           | Descrizione                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**CloneMesh**](id3dxpatchmesh--clonemesh.md)                                   | Crea una nuova mesh della patch con la dichiarazione di vertice specificata.<br/>                      |
| [**GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)                   | Generare un elenco di bordi della rete e le patch che condividono ogni bordo.<br/>                  |
| [**GetControlVerticesPerPatch**](id3dxpatchmesh--getcontrolverticesperpatch.md) | Ottiene il numero di vertici di controllo per patch.<br/>                                       |
| [**GetDeclaration**](id3dxpatchmesh--getdeclaration.md)                         | Ottiene la dichiarazione del vertice.<br/>                                                         |
| [**GetDevice**](id3dxpatchmesh--getdevice.md)                                   | Ottiene il dispositivo che ha creato la mesh.<br/>                                               |
| [**GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)                     | Ottiene i parametri di spostamento della geometria mesh.<br/>                                          |
| [**GetIndexBuffer**](id3dxpatchmesh--getindexbuffer.md)                         | Ottiene il buffer dell'indice mesh.<br/>                                                          |
| [**GetNumPatches**](id3dxpatchmesh--getnumpatches.md)                           | Ottiene il numero di patch nella rete.<br/>                                              |
| [**GetNumVertices**](id3dxpatchmesh--getnumvertices.md)                         | Ottiene il numero di vertici nella rete.<br/>                                             |
| [**GetOptions**](id3dxpatchmesh--getoptions.md)                                 | Ottiene il tipo di patch.<br/>                                                              |
| [**GetPatchInfo**](id3dxpatchmesh--getpatchinfo.md)                             | Ottiene gli attributi della patch.<br/>                                                    |
| [**GetTessSize**](id3dxpatchmesh--gettesssize.md)                               | Ottiene le dimensioni della mesh tassellati, dato un livello a mosaico.<br/>                   |
| [**GetVertexBuffer**](id3dxpatchmesh--getvertexbuffer.md)                       | Ottiene il buffer del vertice mesh.<br/>                                                         |
| [**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)               | Blocca il buffer dell'attributo.<br/>                                                          |
| [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)                       | Blocca il buffer dell'indice.<br/>                                                               |
| [**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)                     | Blocca il buffer dei vertici.<br/>                                                              |
| [**Ottimizzare**](id3dxpatchmesh--optimize.md)                                     | Ottimizza la mesh della patch per un efficiente mosaico.<br/>                                 |
| [**SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)                     | Imposta i parametri di spostamento della geometria mesh.<br/>                                          |
| [**Conteggiarla suddividerla**](id3dxpatchmesh--tessellate.md)                                 | Esegue lo schema a mosaico uniforme in base al livello del mosaico.<br/>                       |
| [**TessellateAdaptive**](id3dxpatchmesh--tessellateadaptive.md)                 | Esegue lo schema a mosaico adattivo basato sul criterio a mosaico adattivo basato su z.<br/> |
| [**UnlockAttributeBuffer**](id3dxpatchmesh--unlockattributebuffer.md)           | Sbloccare il buffer dell'attributo.<br/>                                                         |
| [**UnlockIndexBuffer**](id3dxpatchmesh--unlockindexbuffer.md)                   | Sbloccare il buffer dell'indice.<br/>                                                             |
| [**UnlockVertexBuffer**](id3dxpatchmesh--unlockvertexbuffer.md)                 | Sbloccare il buffer dei vertici.<br/>                                                            |



 

## <a name="remarks"></a>Commenti

Una mesh patch è un reticolo costituito da una serie di patch.

Per ottenere l'interfaccia **ID3DXPatchMesh** , chiamare la funzione [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) .

Il tipo LPD3DXPATCHMESH è definito come puntatore all'interfaccia **ID3DXPatchMesh** , come indicato di seguito:


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
