---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileBinary per leggere e recuperare informazioni sui dati binari. Deprecato.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: Interfaccia IDirectXFileBinary (DXFile. h)
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
ms.openlocfilehash: b6707e4e685289f16b85ab85c2cce13dcd1da962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234980"
---
# <a name="idirectxfilebinary-interface"></a>Interfaccia IDirectXFileBinary

Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileBinary per leggere e recuperare informazioni sui dati binari. Deprecato.

## <a name="members"></a>Membri

L'interfaccia **IDirectXFileBinary** eredita da [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileBinary** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDirectXFileBinary** dispone di questi metodi.



| Metodo                                                 | Descrizione                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetMimeType**](idirectxfilebinary--getmimetype.md) | Recupera il tipo di Multipurpose Internet Mail Extensions (MIME) per i dati binari. Deprecato.<br/> |
| [**GetSize**](idirectxfilebinary--getsize.md)         | Recupera le dimensioni dei dati binari. Deprecato.<br/>                                               |
| [**Lettura**](idirectxfilebinary--read.md)               | Legge i dati binari. Deprecato.<br/>                                                               |



 

## <a name="remarks"></a>Commenti

Il GUID per l'interfaccia IDirectXFileBinary è IID \_ IDirectXFileBinary.

Il tipo LPDIRECTXFileBinary è definito come puntatore a questa interfaccia.


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
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

 

 




