---
description: Confronta due stringhe Unicode.
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: Funzione RtlCompareUnicodeString (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877701"
---
# <a name="rtlcompareunicodestring-function"></a>RtlCompareUnicodeString (funzione)

Confronta due stringhe Unicode.

## <a name="syntax"></a>Sintassi


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*String1* \[ in\]
</dt> <dd>

Puntatore alla prima stringa.

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

Valore con segno che fornisce i risultati del confronto:



| Codice restituito                                                                               | Descrizione                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**Zero**</dt> </dl>       | *String1* è uguale a *string2*.<br/>          |
| <dl> <dt>**< zero**</dt> </dl>  | *String1* è minore di *string2*.<br/>    |
| <dl> <dt>**> zero**</dt> </dl> | *String1* è maggiore di *string2*.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                    |
| Piattaforma di destinazione<br/>          | <dl> <dt>[Universale](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Intestazione<br/>                   | <dl> <dt>WDM. h (include WDM. h, ntddk. h o Ntifs. h)</dt> </dl>                   |
| Libreria<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RtlCompareString**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[**RtlEqualString**](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
