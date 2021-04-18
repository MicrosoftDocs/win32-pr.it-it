---
title: Enumerazione WMDM_TAG_DATATYPE
description: Il \_ \_ tipo di enumerazione WMDM Tag DataType definisce un tipo di dati.
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- Enumerazione WMDM_TAG_DATATYPE Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_TAG_DATATYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad04f0d220809f6bd13d8ae29cc36d52ff6e599
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325009"
---
# <a name="wmdm_tag_datatype-enumeration"></a>\_ \_ Enumerazione DataType Tag WMDM

Il tipo di enumerazione **WMDM \_ tag \_ DataType** definisce un tipo di dati.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWMDM_TAG_DATATYPE { 
  WMDM_TYPE_DWORD,
  WMDM_TYPE_STRING,
  WMDM_TYPE_BINARY,
  WMDM_TYPE_BOOL,
  WMDM_TYPE_QWORD,
  WMDM_TYPE_WORD,
  WMDM_TYPE_GUID,
  WMDM_TYPE_DATE
} WMDM_TAG_DATATYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**WMDM \_ tipo \_ DWORD**
</dt> <dd>

Specifica un valore **DWORD** a 4 byte.

</dd> <dt>

<span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**\_stringa di tipo WMDM \_**
</dt> <dd>

Specifica una stringa Unicode con terminazione null (2 byte per carattere).

</dd> <dt>

<span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**\_binario di tipo WMDM \_**
</dt> <dd>

Specifica una matrice di byte.

</dd> <dt>

<span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**\_tipo WMDM \_ bool**
</dt> <dd>

Specifica un valore booleano a 4 byte.

</dd> <dt>

<span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**WMDM \_ tipo \_ QWORD**
</dt> <dd>

Specifica un valore **QWORD** a 8 byte.

</dd> <dt>

<span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM \_ digitare \_ Word**
</dt> <dd>

Specifica un valore **Word** a 2 byte.

</dd> <dt>

<span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**\_GUID di tipo WMDM \_**
</dt> <dd>

Specifica un GUID a 128 bit (16 byte).

</dd> <dt>

<span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**WMDM \_ tipo di \_ dati**
</dt> <dd>

Specifica una data.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





