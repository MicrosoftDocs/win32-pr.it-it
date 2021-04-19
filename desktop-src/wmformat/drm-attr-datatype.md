---
title: Enumerazione DRM_ATTR_DATATYPE (wmdrmsdk. h)
description: L' \_ \_ enumerazione di tipo di dati DRM attr definisce i tipi di dati utilizzati per le proprietà e gli attributi DRM.
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- Formato Windows Media enumerazione DRM_ATTR_DATATYPE
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ATTR_DATATYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e684ba1c09a86c65a13adbd189bb185f65598b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332289"
---
# <a name="drm_attr_datatype-enumeration"></a>\_ \_ Enumerazione DataType attr DRM

L'enumerazione di **\_ \_ tipo di dati DRM attr** definisce i tipi di dati utilizzati per le proprietà e gli attributi DRM.

## <a name="syntax"></a>Sintassi


```C++
typedef enum DRM_ATTR_DATATYPE { 
  DRM_TYPE_DWORD   = 0,
  DRM_TYPE_STRING  = 1,
  DRM_TYPE_BINARY  = 2,
  DRM_TYPE_BOOL    = 3,
  DRM_TYPE_QWORD   = 4,
  DRM_TYPE_WORD    = 5,
  DRM_TYPE_GUID    = 6
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**tipo di DRM \_ \_ DWORD**
</dt> <dd>

La proprietà è un valore **DWORD** a 4 byte.

</dd> <dt>

<span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**\_stringa di tipo DRM \_**
</dt> <dd>

La proprietà è una stringa Unicode con terminazione null.

</dd> <dt>

<span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**\_Binary di tipo DRM \_**
</dt> <dd>

La proprietà è una matrice di byte.

</dd> <dt>

<span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**\_tipo DRM \_ bool**
</dt> <dd>

La proprietà è un valore booleano a 4 byte.

</dd> <dt>

<span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**\_QWORD di tipo DRM \_**
</dt> <dd>

La proprietà è un valore **QWORD** a 8 byte.

</dd> <dt>

<span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**\_parola di tipo DRM \_**
</dt> <dd>

La proprietà è un valore **Word** a 2 byte.

</dd> <dt>

<span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**\_GUID di tipo DRM \_**
</dt> <dd>

La proprietà è un valore GUID a 128 bit (6 byte).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> </dl>

 

 





