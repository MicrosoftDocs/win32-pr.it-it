---
description: Confronta due stringhe Unicode per determinare se una stringa è un prefisso dell'altro.
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: Funzione RtlPrefixUnicodeString (ntddk. h)
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
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483133"
---
# <a name="rtlprefixunicodestring-function"></a>RtlPrefixUnicodeString (funzione)

Confronta due stringhe Unicode per determinare se una stringa è un prefisso dell'altro.

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

*String1* \[ in\]
</dt> <dd>

Puntatore alla prima stringa, che può essere un prefisso della stringa Unicode memorizzata nel buffer in *string2*.

</dd> <dt>

*String2* \[ in\]
</dt> <dd>

Puntatore alla seconda stringa.

</dd> <dt>

*CaseInSensitive* \[ in\]
</dt> <dd>

Se **true**, la distinzione tra maiuscole e minuscole deve essere ignorata durante il confronto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**True** se *String1* è un prefisso di *string2*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                    |
| Piattaforma di destinazione<br/>          | <dl> <dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Intestazione<br/>                   | <dl> <dt>Ntddk. h (include ntddk. h)</dt> </dl>                                    |
| Libreria<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RtlCompareUnicodeString**](rtlcompareunicodestring.md)
</dt> </dl>

 

 




