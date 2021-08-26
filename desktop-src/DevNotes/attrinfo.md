---
description: Contiene i dati dell'attributo per un file.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: Struttura ATTRINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090f2ab58d8bf1eb4e379166086d31389b533712a3df23f987bba1331f990891
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103731"
---
# <a name="attrinfo-structure"></a>Struttura ATTRINFO

Contiene i dati dell'attributo per un file.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**tAttrID**
</dt> <dd>

Tipo di attributo. Vedere [Tipi DI TAG.](tag-types.md)

</dd> <dt>

**dwFlags**
</dt> <dd>

Flag per questo attributo.



| Valore                                                                                                                                                                                                                                           | Significato                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <dt>**ATTRIBUTE \_ AVAILABLE**</dt> <dt>0x00000001</dt> </dl> | L'attributo è disponibile.<br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <dt>**ATTRIBUTE \_ ERRORE**</dt> <dt>0x00000002</dt> </dl>          | La chiamata non è riuscita perché l'attributo non è disponibile.<br/> |



 

</dd> <dt>

**ullAttr**
</dt> <dd>

Un **valore QWORD** (se il tipo di tag è **TAG TYPE \_ \_ QWORD).**

</dd> <dt>

**dwAttr**
</dt> <dd>

Valore **DWORD** (se il tipo di tag è **TAG TYPE \_ \_ DWORD).**

</dd> <dt>

**lpAttr**
</dt> <dd>

Puntatore a una stringa (se il tipo di tag è **TAG \_ TYPE \_ STRINGREF).**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




