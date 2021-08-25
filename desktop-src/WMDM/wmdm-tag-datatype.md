---
title: WMDM_TAG_DATATYPE enumerazione
description: Il tipo di enumerazione WMDM \_ TAG \_ DATATYPE definisce un tipo di dati.
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- WMDM_TAG_DATATYPE enumerazione windows Media Device Manager
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
ms.openlocfilehash: bd725e6d8a0e1baef8a6dfc98cb5d3056f5d67b2d7babd07c919692d96248881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862671"
---
# <a name="wmdm_tag_datatype-enumeration"></a>Enumerazione \_ \_ DATATYPE TAG WMDM

Il **tipo di enumerazione WMDM TAG \_ \_ DATATYPE** definisce un tipo di dati.

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

<span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**DWORD \_ DI TIPO \_ WMDM**
</dt> <dd>

Specifica un valore **DWORD** a 4 byte.

</dd> <dt>

<span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**STRINGA DI TIPO \_ \_ WMDM**
</dt> <dd>

Specifica una stringa Unicode con terminazione Null (2 byte per carattere).

</dd> <dt>

<span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**FILE BINARIO \_ DI TIPO WMDM \_**
</dt> <dd>

Specifica una matrice di byte.

</dd> <dt>

<span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**TIPO WMDM \_ \_ BOOL**
</dt> <dd>

Specifica un valore booleano a 4 byte.

</dd> <dt>

<span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**QWORD \_ DI TIPO \_ WMDM**
</dt> <dd>

Specifica un valore **QWORD** a 8 byte.

</dd> <dt>

<span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**WMDM \_ TYPE \_ WORD**
</dt> <dd>

Specifica un valore **WORD** a 2 byte.

</dd> <dt>

<span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**GUID DI TIPO WMDM \_ \_**
</dt> <dd>

Specifica un GUID a 128 bit (16 byte).

</dd> <dt>

<span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**DATA TIPO \_ \_ WMDM**
</dt> <dd>

Specifica una data.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





