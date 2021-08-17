---
description: "Interfaccia ID3DXSaveUserData: questa interfaccia viene implementata dall'applicazione per salvare eventuali dati utente aggiuntivi incorporati nei file con estensione x."
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: Interfaccia ID3DXSaveUserData (D3dx9anim.h)
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
ms.openlocfilehash: e5b0f02a4fb114f46930076f46ea7c416850a0e81f7369d4aab63a2de5ed6d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801137"
---
# <a name="id3dxsaveuserdata-interface"></a>Interfaccia ID3DXSaveUserData

Questa interfaccia viene implementata dall'applicazione per salvare eventuali dati utente aggiuntivi incorporati nei file con estensione x. Un'istanza di questa interfaccia viene passata a [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)e D3DX chiama il metodo appropriato su questa interfaccia ogni volta che vengono rilevati i dati appropriati. Ad esempio, per ogni oggetto frame nel file con estensione x viene chiamato [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) e vengono passati i dati figlio.

## <a name="members"></a>Membri

**L'interfaccia ID3DXSaveUserData** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXSaveUserData** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXSaveUserData** include questi metodi.



| Metodo                                                                              | Descrizione                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md)                   | Aggiungere dati figlio al frame.<br/>                            |
| [**AddMeshChildData**](id3dxsaveuserdata--addmeshchilddata.md)                     | Aggiungere dati figlio alla mesh.<br/>                             |
| [**AddTopLevelDataObjectsPost**](id3dxsaveuserdata--addtopleveldataobjectspost.md) | Aggiungere un oggetto di primo livello dopo la gerarchia dei frame.<br/>       |
| [**AddTopLevelDataObjectsPre**](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | Aggiungere un oggetto di primo livello prima della gerarchia dei frame.<br/>      |
| [**RegisterTemplates**](id3dxsaveuserdata--registertemplates.md)                   | Callback che consente all'utente di registrare un modello di file con estensione x.<br/> |
| [**Salva modelli**](id3dxsaveuserdata--savetemplates.md)                           | Callback che consente all'utente di salvare un modello di file con estensione x.<br/>     |



 

## <a name="remarks"></a>Commenti

Il tipo LPD3DXSAVEUSERDATA è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
