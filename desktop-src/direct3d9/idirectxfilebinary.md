---
description: Le applicazioni usano i metodi dell'interfaccia IDirectXFileBinary per leggere e recuperare informazioni sui dati binari. Deprecato.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: Interfaccia IDirectXFileBinary (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 46e0da3a0cb03d3769e7888706a48fbf00786471afed285ce54c629285ac158c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292410"
---
# <a name="idirectxfilebinary-interface"></a>Interfaccia IDirectXFileBinary

Le applicazioni usano i metodi dell'interfaccia IDirectXFileBinary per leggere e recuperare informazioni sui dati binari. Deprecato.

## <a name="members"></a>Membri

**L'interfaccia IDirectXFileBinary** eredita da [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileBinary** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDirectXFileBinary** include questi metodi.



| Metodo                                                 | Descrizione                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetMimeType**](idirectxfilebinary--getmimetype.md) | Recupera il Multipurpose Internet Mail Extensions (MIME) per i dati binari. Deprecato.<br/> |
| [**GetSize**](idirectxfilebinary--getsize.md)         | Recupera le dimensioni dei dati binari. Deprecato.<br/>                                               |
| [**Leggere**](idirectxfilebinary--read.md)               | Legge i dati binari. Deprecato.<br/>                                                               |



 

## <a name="remarks"></a>Commenti

Il GUID per l'interfaccia IDirectXFileBinary è IID \_ IDirectXFileBinary.

Il tipo LPDIRECTXFileBinary è definito come puntatore a questa interfaccia.


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
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

[Interfacce di file X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




