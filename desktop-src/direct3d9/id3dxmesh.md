---
description: Per modificare gli oggetti mesh, le applicazioni utilizzano i metodi dell'interfaccia ID3DXMesh.
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: Interfaccia ID3DXMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355714"
---
# <a name="id3dxmesh-interface"></a>Interfaccia ID3DXMesh

Per modificare gli oggetti mesh, le applicazioni utilizzano i metodi dell'interfaccia ID3DXMesh.

## <a name="members"></a>Membri

L'interfaccia **ID3DXMesh** eredita da [**ID3DXBaseMesh**](id3dxbasemesh.md). **ID3DXMesh** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXMesh** dispone di questi metodi.



| Metodo                                                            | Descrizione                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)     | Blocca il buffer mesh che contiene i dati dell'attributo mesh e restituisce un puntatore.<br/>                                   |
| [**Ottimizzare**](id3dxmesh--optimize.md)                           | Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.<br/>                                     |
| [**OptimizeInplace**](id3dxmesh--optimizeinplace.md)             | Genera una mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno. Questo metodo riordina la mesh esistente.<br/> |
| [**SetAttributeTable**](id3dxmesh--setattributetable.md)         | Imposta la tabella degli attributi per una mesh e il numero di voci archiviate nella tabella.<br/>                                          |
| [**UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md) | Sblocca un buffer dell'attributo.<br/>                                                                                                |



 

## <a name="remarks"></a>Commenti

Per ottenere l'interfaccia **ID3DXMesh** , chiamare la funzione [**D3DXCreateMesh**](d3dxcreatemesh.md) o [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) .

Questa interfaccia eredita funzionalità aggiuntive dall'interfaccia [**ID3DXBaseMesh**](id3dxbasemesh.md) .

Il tipo LPD3DXMESH è definito come puntatore all'interfaccia **ID3DXMesh** .


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Funzioni mesh](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




