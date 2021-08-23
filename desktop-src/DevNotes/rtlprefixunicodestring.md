---
description: Confronta due stringhe Unicode per determinare se una stringa è un prefisso dell'altra.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: Funzione RtlPrefixUnicodeString (Ntddk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 28997f3bc85dedb9a18139cec13b9a76a8dd975e4ff57f1380053178bfaab328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076005"
---
# <a name="rtlprefixunicodestring-function"></a>Funzione RtlPrefixUnicodeString

Confronta due stringhe Unicode per determinare se una stringa è un prefisso dell'altra.

## <a name="syntax"></a>Sintassi


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stringa1* \[ Pollici\]
</dt> <dd>

Puntatore alla prima stringa, che potrebbe essere un prefisso della stringa Unicode memorizzata nel buffer in *String2.*

</dd> <dt>

*Stringa2* \[ Pollici\]
</dt> <dd>

Puntatore alla seconda stringa.

</dd> <dt>

*CaseInSensitive* \[ Pollici\]
</dt> <dd>

Se **TRUE,** la distinzione tra maiuscole e minuscole deve essere ignorata quando si esegue il confronto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TRUE** se *String1* è un prefisso di *String2.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                    |
| Piattaforma di destinazione<br/>          | <dl> <dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Intestazione<br/>                   | <dl> <dt>Ntddk.h (includere Ntddk.h)</dt> </dl>                                    |
| Libreria<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RtlCompareUnicodeString**](rtlcompareunicodestring.md)
</dt> </dl>

 

 




