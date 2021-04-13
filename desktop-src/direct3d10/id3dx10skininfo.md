---
description: ID3DX10SkinInfo consente di ottimizzare, elaborare e impostare manualmente la relazione tra le ossa e i vertici nelle mesh (vedere animazione scheletrica su Wikipedia).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: Interfaccia ID3DX10SkinInfo (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354929"
---
# <a name="id3dx10skininfo-interface"></a>Interfaccia ID3DX10SkinInfo

ID3DX10SkinInfo consente di ottimizzare, elaborare e impostare manualmente la relazione tra le ossa e i vertici nelle mesh (vedere [animazione scheletrica su Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)). È particolarmente utile per la creazione di file con estensione x esportati da app DCC (ad esempio 3DS Max e Maya) più intuitivi e per il miglioramento della velocità di rendering delle mesh con skin in modalità di rendering software.

## <a name="members"></a>Membri

L'interfaccia **ID3DX10SkinInfo** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10SkinInfo** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX10SkinInfo** dispone di questi metodi.



| Metodo                                                                   | Descrizione                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddBoneInfluences**](id3dx10skininfo-addboneinfluences.md)           | Consentire a un osso esistente di influenzare un gruppo di vertici e definire la quantità di influenza dell'osso su ogni vertice.<br/>     |
| [**AddBones**](id3dx10skininfo-addbones.md)                             | Allocare spazio per più ossa.<br/>                                                                                          |
| [**AddVertices**](id3dx10skininfo-addvertices.md)                       | Allocare spazio per altri vertici.<br/>                                                                                 |
| [**ClearBoneInfluences**](id3dx10skininfo-clearboneinfluences.md)       | Cancellare l'elenco di vertici di un osso che influenza.<br/>                                                                     |
| [**Compact**](id3dx10skininfo-compact.md)                               | Limitare il numero di ossa che possono influenzare un vertice e/o limitare la quantità di influenza che può avere un osso su un vertice.<br/> |
| [**DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md)         | Eseguire il skining del software su una matrice di vertici.<br/>                                                                           |
| [**FindBoneInfluenceIndex**](id3dx10skininfo-findboneinfluenceindex.md) | Trovare l'indice che indica la posizione in cui un vertice specificato si trova in un elenco di vertici influenzato di un dato osso.<br/>                    |
| [**GetBoneInfluence**](id3dx10skininfo-getboneinfluence.md)             | Ottenere la quantità di influenza di un dato osso su un vertice specificato.<br/>                                                       |
| [**GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md)   | Ottiene il numero di vertici influenzati da un determinato osso.<br/>                                                                |
| [**GetBoneInfluences**](id3dx10skininfo-getboneinfluences.md)           | Ottiene un elenco di vertici influenzati da un dato osso e un elenco della quantità di influenza che l'osso ha su ogni vertice.<br/> |
| [**GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md)     | Ottenere il numero di vertici a cui un osso può influenzare al massimo.<br/>                                                              |
| [**GetNumBones**](id3dx10skininfo-getnumbones.md)                       | Ottenere il numero di Bones in ID3DX10SkinInfo.<br/>                                                                             |
| [**GetNumVertices**](id3dx10skininfo-getnumvertices.md)                 | Ottenere il numero di vertici in ID3DX10SkinInfo.<br/>                                                                          |
| [**RemapBones**](id3dx10skininfo-remapbones.md)                         | Modificare le ossa che influenzano i vertici.<br/>                                                                            |
| [**RemapVertices**](id3dx10skininfo-remapvertices.md)                   | Modificare i vertici influenzati da quali ossa.<br/>                                                                    |
| [**RemoveBone**](id3dx10skininfo-removebone.md)                         | Rimuovere un osso.<br/>                                                                                                          |
| [**SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md)             | Imposta la quantità di influenza di un dato osso su un vertice specificato.<br/>                                                       |



 

## <a name="remarks"></a>Commenti

Creare un'interfaccia ID3DX10SkinInfo con [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh** o **D3DX10CreateSkinInfoFVF**.

Il tipo LPD3DX10SKININFO è definito come puntatore all'interfaccia **ID3DX10SkinInfo** .


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
