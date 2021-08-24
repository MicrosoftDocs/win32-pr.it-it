---
description: Le applicazioni usano i metodi dell'interfaccia ID3DXSkinInfo per modificare le matrici di osso, che vengono usate per eseguire l'interfaccia dei dati dei vertici per l'animazione. Questa interfaccia non è più strettamente associata a ID3DXMesh e può essere usata per eseguire la skin di qualsiasi set di dati sui vertici.
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: Interfaccia ID3DXSkinInfo (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d7bfeddb5cb34bb9b5d0372f424c40248f06e55fa7263e1e884e71fb82dafcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727761"
---
# <a name="id3dxskininfo-interface"></a>Interfaccia ID3DXSkinInfo

Le applicazioni usano i metodi dell'interfaccia ID3DXSkinInfo per modificare le matrici di osso, che vengono usate per eseguire l'interfaccia dei dati dei vertici per l'animazione. Questa interfaccia non è più strettamente associata a [**ID3DXMesh**](id3dxmesh.md) e può essere usata per eseguire l'interfaccia di qualsiasi set di dati sui vertici.

## <a name="members"></a>Membri

**L'interfaccia ID3DXSkinInfo** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXSkinInfo** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXSkinInfo** include questi metodi.



| Metodo                                                                              | Descrizione                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clone**](id3dxskininfo--clone.md)                                               | Clona un oggetto informazioni sull'interfaccia.<br/>                                                                                                                                                          |
| [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)                 | Accetta una mesh e restituisce una nuova mesh con pesi di fusione per vertice e una tabella di combinazione di osso. La tabella descrive gli elementi che influiscono sui subset della mesh.<br/>                   |
| [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)   | Accetta una mesh e restituisce una nuova mesh con pesi di fusione per vertice, indici e una tabella di combinazione di osso. La tabella descrive quali palette di osso influiscono sui subset della mesh.<br/> |
| [**FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md) | Recupera l'indice dell'influenza ossea che interessa un singolo vertice.<br/>                                                                                                                |
| [**GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)                         | Ottiene i vertici e i pesi influenzati da un'osso.<br/>                                                                                                                               |
| [**GetBoneName**](id3dxskininfo--getbonename.md)                                   | Ottiene il nome dell'osso dall'indice dell'osso.<br/>                                                                                                                                            |
| [**GetBoneOffsetMatrix**](id3dxskininfo--getboneoffsetmatrix.md)                   | Ottiene la matrice di offset dell'osso.<br/>                                                                                                                                                        |
| [**GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)             | Recupera il fattore di blend e il vertice interessati da un'influenza ossea specificata.<br/>                                                                                                       |
| [**GetDeclaration**](id3dxskininfo--getdeclaration.md)                             | Ottiene la dichiarazione del vertice.<br/>                                                                                                                                                        |
| [**GetFVF**](id3dxskininfo--getfvf.md)                                             | Ottiene il valore del vertice della funzione fissa.<br/>                                                                                                                                               |
| [**GetMaxFaceInfluences**](id3dxskininfo--getmaxfaceinfluences.md)                 | Ottiene il numero massimo di influenze del viso in una mesh triangolare con l'oggetto index buffer.<br/>                                                                                                |
| [**GetMaxVertexInfluences**](id3dxskininfo--getmaxvertexinfluences.md)             | Ottiene il numero massimo di influenze per qualsiasi vertice nella mesh.<br/>                                                                                                                   |
| [**GetMinBoneInfluence**](id3dxskininfo--getminboneinfluence.md)                   | Ottiene l'influenza minima dell'osso. I valori di influenza inferiori a questo vengono ignorati.<br/>                                                                                                    |
| [**GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md)                 | Ottiene il numero di influenze per un osso.<br/>                                                                                                                                           |
| [**GetNumBones**](id3dxskininfo--getnumbones.md)                                   | Ottiene il numero di esche.<br/>                                                                                                                                                           |
| [**Rimappare**](id3dxskininfo--remap.md)                                               | Aggiorna le informazioni sull'influenza dell'osso in modo che corrispondano ai vertici dopo che sono stati riordinati. Questo metodo deve essere chiamato se il vertex buffer di destinazione è stato riordinato esternamente.<br/>              |
| [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)                         | Imposta il valore di influenza per un'osso.<br/>                                                                                                                                                |
| [**SetBoneName**](id3dxskininfo--setbonename.md)                                   | Imposta il nome dell'osso.<br/>                                                                                                                                                                 |
| [**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)                   | Imposta la matrice di offset dell'osso.<br/>                                                                                                                                                        |
| [**SetBoneVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)             | Imposta un valore di influenza di un osso su un singolo vertice.<br/>                                                                                                                               |
| [**SetDeclaration**](id3dxskininfo--setdeclaration.md)                             | Imposta la dichiarazione del vertice.<br/>                                                                                                                                                        |
| [**SetFVF**](id3dxskininfo--setfvf.md)                                             | Imposta il tipo FVF (Flexible Vertex Format).<br/>                                                                                                                                         |
| [**SetMinBoneInfluence**](id3dxskininfo--setminboneinfluence.md)                   | Imposta l'influenza minima dell'osso. I valori di influenza inferiori a questo vengono ignorati.<br/>                                                                                                    |
| [**UpdateSkinnedMesh**](id3dxskininfo--updateskinnedmesh.md)                       | Applica l'interfaccia software ai vertici di destinazione in base alle matrici correnti.<br/>                                                                                                     |



 

## <a name="remarks"></a>Commenti

Creare **un'interfaccia ID3DXSkinInfo** con [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)o [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).

Il tipo LPD3DXSKININFO è definito come puntatore **all'interfaccia ID3DXSkinInfo.**


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
