---
title: Tipi di dati semplici ADSI (IADs. h)
description: Active Directory Service Interfaces (ADSI) definisce e utilizza i tipi di dati semplici seguenti.
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
ms.openlocfilehash: 5530fda2ca1f4fe967eaf376b668a0bedc29c4b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048002"
---
# <a name="adsi-simple-data-types"></a>Tipi di dati semplici ADSI

Active Directory Service Interfaces (ADSI) definisce e utilizza i tipi di dati semplici seguenti.


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

**\_valore booleano ADS**
</dt> <dd>

DWORD

</dd> <dt>

**\_ \_ stringa esatta del case Ads \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**caso ADS, \_ \_ Ignora \_ stringa**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_stringa DN \_ ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_Integer ADS**
</dt> <dd>

DWORD

</dd> <dt>

**ADS \_ grande \_ Integer**
</dt> <dd>

[**\_Integer grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

**\_stringa numerica Ads \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_classe di oggetti ADS \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_stringa stampabile \_ ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_handle di ricerca Ads \_**
</dt> <dd>

HANDLE

</dd> <dt>

**\_ora UTC \_ ADS**
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando ADSI legge un attributo definito come **Integer** nello schema LDAP, gestisce sempre il valore integer come valore a 32 bit e può troncare i dati. Si tratta solo di un problema per i server LDAP che consentono valori integer con dimensione arbitraria. Se l'attributo è un attributo personalizzato definito estendendo lo schema, è possibile evitare questo problema definendo l'attributo personalizzato sotto forma di stringa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl> |



 

