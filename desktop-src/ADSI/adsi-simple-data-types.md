---
title: Tipi di dati semplici ADSI (Iads.h)
description: Active Directory Service Interfaces (ADSI) definisce e usa i tipi di dati semplici seguenti.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422fc0e20195e576f3ade8b39948992d61a376b58fd22f399ca1009db79cbdb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023699"
---
# <a name="adsi-simple-data-types"></a>Tipi di dati semplici ADSI

Active Directory Service Interfaces (ADSI) definisce e usa i tipi di dati semplici seguenti.


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

**ADS \_ BOOLEAN**
</dt> <dd>

DWORD

</dd> <dt>

**STRINGA ESATTA \_ \_ MAIUSCOLE/MINUSCOLE \_ DI ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ CASE \_ IGNORE \_ STRING**
</dt> <dd>

LPWSTR

</dd> <dt>

**STRINGA \_ DN DI SERVIZI \_ DI ACTIVE DIRECTORY**
</dt> <dd>

LPWSTR

</dd> <dt>

**ADS \_ INTEGER**
</dt> <dd>

DWORD

</dd> <dt>

**ADS \_ LARGE \_ INTEGER**
</dt> <dd>

[**LARGE \_ INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

**STRINGA NUMERICA \_ \_ ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**CLASSE DI \_ OGGETTI \_ ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**STRINGA \_ STAMPABILE DI \_ ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**HANDLE DI RICERCA DI ADS \_ \_**
</dt> <dd>

HANDLE

</dd> <dt>

**ORA UTC DI ADS \_ \_**
</dt> <dd>

[**Systemtime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando ADSI legge un attributo definito come **INTEGER** nello schema LDAP, gestirà sempre l'intero come valore a 32 bit e potrebbe troncare i dati. Questo è solo un problema per i server LDAP che consentono valori interi di dimensioni arbitrarie. Se l'attributo è un attributo personalizzato definito estendendo lo schema, questo problema può essere evitato definendo l'attributo personalizzato come stringa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl> |



 

