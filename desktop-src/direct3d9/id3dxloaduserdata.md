---
description: "Interfaccia ID3DXLoadUserData: questa interfaccia viene implementata dall'applicazione per salvare eventuali dati utente aggiuntivi incorporati nei file con estensione x."
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: Interfaccia ID3DXLoadUserData (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ede66e7250a1dec095bd03a72ea69e58afb59a60b43647fd49adfc958689cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748121"
---
# <a name="id3dxloaduserdata-interface"></a>Interfaccia ID3DXLoadUserData

Questa interfaccia viene implementata dall'applicazione per salvare eventuali dati utente aggiuntivi incorporati nei file con estensione x. Un'istanza di questa interfaccia viene passata a [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)e D3DX chiama il metodo appropriato su questa interfaccia ogni volta che vengono rilevati i dati appropriati. Ad esempio, per ogni oggetto frame nel file con estensione x viene chiamato [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) e vengono passati i dati figlio.

## <a name="members"></a>Membri

**L'interfaccia ID3DXLoadUserData** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXLoadUserData** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXLoadUserData** include questi metodi.



| Metodo                                                              | Descrizione                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) | Caricare i dati figlio del frame da un file con estensione x.<br/> |
| [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md)   | Caricare i dati figlio mesh da un file con estensione x.<br/>  |
| [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md)     | Caricare i dati di primo livello da un file con estensione x.<br/>   |



 

## <a name="remarks"></a>Commenti

Il tipo LPD3DXLOADUSERDATA è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
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

 

 
