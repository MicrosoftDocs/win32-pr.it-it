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
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877241"
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

Tipo di attributo. Vedere [tipi di tag](tag-types.md).

</dd> <dt>

**dwFlags**
</dt> <dd>

Flag per questo attributo.



| Valore                                                                                                                                                                                                                                           | Significato                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <dt>**Attributo \_**</dt> <dt>0x00000001</dt> disponibili </dl> | L'attributo è disponibile.<br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <dt>**Attributo \_ 0x00000002 non riuscito**</dt> <dt></dt> </dl>          | La chiamata non è riuscita perché l'attributo non è disponibile.<br/> |



 

</dd> <dt>

**ullAttr**
</dt> <dd>

Valore **QWORD** (se il tipo di tag è **il \_ tipo \_ di tag QWORD**).

</dd> <dt>

**dwAttr**
</dt> <dd>

Valore **DWORD** (se il tipo di tag è **il \_ tipo \_ di tag DWORD**).

</dd> <dt>

**lpAttr**
</dt> <dd>

Puntatore a una stringa (se il tipo di tag è **il \_ tipo \_ di tag STRINGREF**).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




