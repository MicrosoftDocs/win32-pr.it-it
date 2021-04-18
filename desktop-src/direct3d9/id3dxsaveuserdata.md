---
description: Questa interfaccia viene implementata dall'applicazione per salvare eventuali dati utente aggiuntivi incorporati nei file con estensione x.
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: Interfaccia ID3DXSaveUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 77529a5a7b260dd27dc4af1752c88f55117bc974
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322549"
---
# <a name="id3dxsaveuserdata-interface"></a>Interfaccia ID3DXSaveUserData

Questa interfaccia viene implementata dall'applicazione per salvare eventuali dati utente aggiuntivi incorporati nei file con estensione x. Un'istanza di questa interfaccia viene passata a [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)e D3DX chiama il metodo appropriato su questa interfaccia ogni volta che vengono rilevati i dati appropriati. Per ogni oggetto frame nel file con estensione x, ad esempio, viene chiamato [**ID3DXSaveUserData:: AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) e vengono passati i dati figlio.

## <a name="members"></a>Membri

L'interfaccia **ID3DXSaveUserData** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSaveUserData** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXSaveUserData** dispone di questi metodi.



| Metodo                                                                              | Descrizione                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md)                   | Aggiungere i dati figlio al frame.<br/>                            |
| [**AddMeshChildData**](id3dxsaveuserdata--addmeshchilddata.md)                     | Aggiungere i dati figlio alla rete.<br/>                             |
| [**AddTopLevelDataObjectsPost**](id3dxsaveuserdata--addtopleveldataobjectspost.md) | Aggiungere un oggetto di primo livello dopo la gerarchia dei frame.<br/>       |
| [**AddTopLevelDataObjectsPre**](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | Aggiungere un oggetto di primo livello prima della gerarchia dei frame.<br/>      |
| [**RegisterTemplates**](id3dxsaveuserdata--registertemplates.md)                   | Callback che consente all'utente di registrare un modello di file con estensione x.<br/> |
| [**SaveTemplates**](id3dxsaveuserdata--savetemplates.md)                           | Callback che consente all'utente di salvare un modello di file con estensione x.<br/>     |



 

## <a name="remarks"></a>Commenti

Il tipo LPD3DXSAVEUSERDATA è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
