---
description: Le applicazioni usano i metodi dell'interfaccia IDirectXFileDataReference per supportare gli oggetti riferimento ai dati.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: Interfaccia IDirectXFileDataReference (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4507bed7a5f3f461c80b8eed1e5c07c15cfd34b7aab7a02c3e803a43a88ae132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095631"
---
# <a name="idirectxfiledatareference-interface"></a>Interfaccia IDirectXFileDataReference

Le applicazioni usano i metodi dell'interfaccia IDirectXFileDataReference per supportare gli oggetti riferimento ai dati. Un oggetto riferimento ai dati fa riferimento a un oggetto dati definito in precedenza nel file. In questo modo è possibile usare lo stesso oggetto più volte senza ripeterlo nel file. Deprecato.

## <a name="members"></a>Membri

**L'interfaccia IDirectXFileDataReference** eredita da [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileDataReference** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili **nell'interfaccia IDirectXFileDataReference.**



| Metodo                                                | Descrizione                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [**Risolvi**](idirectxfiledatareference--resolve.md) | Risolve i riferimenti ai dati. Deprecato.<br/> |



 

## <a name="remarks"></a>Commenti

Dopo aver determinato che un oggetto è un oggetto riferimento ai dati, usare il metodo [**IDirectXFileDataReference::Resolve**](idirectxfiledatareference--resolve.md) per recuperare l'oggetto a cui si fa riferimento definito in precedenza nel file. Per informazioni su come identificare un oggetto riferimento ai dati, vedere [**l'interfaccia IDirectXFileData.**](idirectxfiledata.md)

Il GUID per l'interfaccia IDirectXFileDataReference è IID \_ IDirectXFileDataReference.

Il tipo LPDIRECTXFILEDataReference è definito come puntatore a questa interfaccia.


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[X Interfacce di file](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




