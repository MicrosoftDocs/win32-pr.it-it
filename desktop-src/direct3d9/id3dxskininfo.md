---
description: Le applicazioni usano i metodi dell'interfaccia ID3DXSkinInfo per modificare le matrici ossee, che vengono usate per l'animazione dei dati del vertice. Questa interfaccia non è più strettamente legata a ID3DXMesh e può essere usata per interfacciare qualsiasi set di dati dei vertici.
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: Interfaccia ID3DXSkinInfo (D3DX9Mesh. h)
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
ms.openlocfilehash: afb93a0513bef7de1b0815b8b1f50179e2cba41d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322434"
---
# <a name="id3dxskininfo-interface"></a>Interfaccia ID3DXSkinInfo

Le applicazioni usano i metodi dell'interfaccia ID3DXSkinInfo per modificare le matrici ossee, che vengono usate per l'animazione dei dati del vertice. Questa interfaccia non è più strettamente legata a [**ID3DXMesh**](id3dxmesh.md) e può essere usata per interfacciare qualsiasi set di dati dei vertici.

## <a name="members"></a>Membri

L'interfaccia **ID3DXSkinInfo** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSkinInfo** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXSkinInfo** dispone di questi metodi.



| Metodo                                                                              | Descrizione                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clone**](id3dxskininfo--clone.md)                                               | Clona un oggetto info di interfaccia.<br/>                                                                                                                                                          |
| [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)                 | Accetta una mesh e restituisce una nuova mesh con pesi di Blend per vertice e una tabella delle combinazioni di osso. La tabella descrive le ossa che influiscono sui subset della mesh.<br/>                   |
| [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)   | Acquisisce una mesh e restituisce una nuova mesh con pesi di Blend per vertice, indici e una tabella combinata Bone. La tabella descrive le tavolozze ossee che influiscono sui subset della mesh.<br/> |
| [**FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md) | Recupera l'indice dell'influenza ossea che interessa un singolo vertice.<br/>                                                                                                                |
| [**GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)                         | Ottiene i vertici e i pesi influenzati da un osso.<br/>                                                                                                                               |
| [**Getbonename**](id3dxskininfo--getbonename.md)                                   | Ottiene il nome dell'osso, dall'indice di osso.<br/>                                                                                                                                            |
| [**GetBoneOffsetMatrix**](id3dxskininfo--getboneoffsetmatrix.md)                   | Ottiene la matrice di offset dell'osso.<br/>                                                                                                                                                        |
| [**GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)             | Recupera il fattore di fusione e il vertice interessati da un'influenza dell'osso specificata.<br/>                                                                                                       |
| [**GetDeclaration**](id3dxskininfo--getdeclaration.md)                             | Ottiene la dichiarazione del vertice.<br/>                                                                                                                                                        |
| [**GetFVF**](id3dxskininfo--getfvf.md)                                             | Ottiene il valore del vertice della funzione fissa.<br/>                                                                                                                                               |
| [**GetMaxFaceInfluences**](id3dxskininfo--getmaxfaceinfluences.md)                 | Ottiene le influenze massime della faccia in una mesh triangolare con il buffer di indice specificato.<br/>                                                                                                |
| [**GetMaxVertexInfluences**](id3dxskininfo--getmaxvertexinfluences.md)             | Ottiene il numero massimo di influenze per qualsiasi vertice nella mesh.<br/>                                                                                                                   |
| [**GetMinBoneInfluence**](id3dxskininfo--getminboneinfluence.md)                   | Ottiene l'influenza dell'osso minima. I valori più piccoli di quelli che vengono ignorati.<br/>                                                                                                    |
| [**GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md)                 | Ottiene il numero di influenze per un osso.<br/>                                                                                                                                           |
| [**GetNumBones**](id3dxskininfo--getnumbones.md)                                   | Ottiene il numero di ossa.<br/>                                                                                                                                                           |
| [**Modificare il mapping**](id3dxskininfo--remap.md)                                               | Aggiorna le informazioni sull'influenza ossea in modo che corrispondano ai vertici dopo essere stati riordinati. Questo metodo deve essere chiamato se il buffer dei vertici di destinazione è stato riordinato esternamente.<br/>              |
| [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)                         | Imposta il valore di influenza per un osso.<br/>                                                                                                                                                |
| [**Sebonename**](id3dxskininfo--setbonename.md)                                   | Imposta il nome dell'osso.<br/>                                                                                                                                                                 |
| [**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)                   | Imposta la matrice di offset dell'osso.<br/>                                                                                                                                                        |
| [**SetBoneVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)             | Imposta un valore di influenza di un osso in un singolo vertice.<br/>                                                                                                                               |
| [**Dichiarazione di**](id3dxskininfo--setdeclaration.md)                             | Imposta la dichiarazione del vertice.<br/>                                                                                                                                                        |
| [**SetFVF**](id3dxskininfo--setfvf.md)                                             | Imposta il tipo FVF (Flexible Vertex Format).<br/>                                                                                                                                         |
| [**SetMinBoneInfluence**](id3dxskininfo--setminboneinfluence.md)                   | Imposta l'influenza dell'osso minima. I valori più piccoli di quelli che vengono ignorati.<br/>                                                                                                    |
| [**UpdateSkinnedMesh**](id3dxskininfo--updateskinnedmesh.md)                       | Applica il skining del software ai vertici di destinazione in base alle matrici correnti.<br/>                                                                                                     |



 

## <a name="remarks"></a>Commenti

Creare un'interfaccia **ID3DXSkinInfo** con [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)o [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).

Il tipo LPD3DXSKININFO è definito come puntatore all'interfaccia **ID3DXSkinInfo** .


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
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

 

 
