---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileDataReference per supportare gli oggetti riferimento ai dati.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: Interfaccia IDirectXFileDataReference (DXFile. h)
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
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132426"
---
# <a name="idirectxfiledatareference-interface"></a>Interfaccia IDirectXFileDataReference

Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileDataReference per supportare gli oggetti riferimento ai dati. Un oggetto riferimento ai dati fa riferimento a un oggetto dati definito in precedenza nel file. In questo modo è possibile utilizzare lo stesso oggetto più volte senza ripeterlo nel file. Deprecato.

## <a name="members"></a>Membri

L'interfaccia **IDirectXFileDataReference** eredita da [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileDataReference** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDirectXFileDataReference** dispone di questi metodi.



| Metodo                                                | Descrizione                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [**Risolvi**](idirectxfiledatareference--resolve.md) | Risolve i riferimenti ai dati. Deprecato.<br/> |



 

## <a name="remarks"></a>Commenti

Dopo aver determinato che un oggetto è un oggetto riferimento ai dati, usare il metodo [**IDirectXFileDataReference:: Resolve**](idirectxfiledatareference--resolve.md) per recuperare l'oggetto a cui si fa riferimento definito in precedenza nel file. Per informazioni su come identificare un oggetto riferimento ai dati, vedere l'interfaccia [**IDirectXFileData**](idirectxfiledata.md) .

Il GUID per l'interfaccia IDirectXFileDataReference è IID \_ IDirectXFileDataReference.

Il tipo LPDIRECTXFILEDataReference è definito come puntatore a questa interfaccia.


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[Interfacce di file X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




