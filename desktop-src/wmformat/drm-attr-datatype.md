---
title: DRM_ATTR_DATATYPE enumerazione (Wmdrmsdk.h)
description: L'enumerazione \_ DRM ATTR \_ DATATYPE definisce i tipi di dati usati per gli attributi e le proprietà DRM.
ms.assetid: ccad16e2-475d-4cc7-b773-f17038d2754a
keywords:
- DRM_ATTR_DATATYPE enumerazione Windows Media Format
- enumeration windows Media Format
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
ms.openlocfilehash: 09f55c3d218aa86c33f699d4cb762e752a0bf4e1029e8ca42eee797aaf8ac721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110531"
---
# <a name="drm_attr_datatype-enumeration"></a>Enumerazione DRM \_ ATTR \_ DATATYPE

**L'enumerazione \_ DRM ATTR \_ DATATYPE** definisce i tipi di dati usati per gli attributi e le proprietà DRM.

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

<span id="DRM_TYPE_DWORD"></span><span id="drm_type_dword"></span>**TIPO \_ \_ DRM DWORD**
</dt> <dd>

La proprietà è un valore **DWORD** a 4 byte.

</dd> <dt>

<span id="DRM_TYPE_STRING"></span><span id="drm_type_string"></span>**STRINGA DI \_ TIPO \_ DRM**
</dt> <dd>

La proprietà è una stringa Unicode con terminazione Null.

</dd> <dt>

<span id="DRM_TYPE_BINARY"></span><span id="drm_type_binary"></span>**TIPO \_ BINARIO DRM \_**
</dt> <dd>

La proprietà è una matrice di byte.

</dd> <dt>

<span id="DRM_TYPE_BOOL"></span><span id="drm_type_bool"></span>**TIPO DRM \_ \_ BOOL**
</dt> <dd>

La proprietà è un valore booleano a 4 byte.

</dd> <dt>

<span id="DRM_TYPE_QWORD"></span><span id="drm_type_qword"></span>**DRM \_ TYPE \_ QWORD**
</dt> <dd>

La proprietà è un valore **QWORD** a 8 byte.

</dd> <dt>

<span id="DRM_TYPE_WORD"></span><span id="drm_type_word"></span>**DRM \_ TYPE \_ WORD**
</dt> <dd>

La proprietà è un valore **WORD** a 2 byte.

</dd> <dt>

<span id="DRM_TYPE_GUID"></span><span id="drm_type_guid"></span>**GUID TIPO \_ \_ DRM**
</dt> <dd>

La proprietà è un valore GUID a 128 bit (6 byte).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> </dl>

 

 





