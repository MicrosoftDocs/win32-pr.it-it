---
description: La funzione HTMLValueToUnicode converte una stringa in formato Unicode del CP HTML \_ in una stringa Unicode.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: Funzione HTMLValueToUnicode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750066"
---
# <a name="htmlvaluetounicode-function"></a>HTMLValueToUnicode (funzione)

La funzione **HTMLValueToUnicode** converte una stringa in formato Unicode del CP HTML \_ in una stringa Unicode.

## <a name="syntax"></a>Sintassi


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pValue* \[ in uscita\]
</dt> <dd>

In input, puntatore alla stringa HTML fornita da MCSVC.

Nell'output, puntatore alla stringa Unicode convertita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce l'equivalente Unicode della stringa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




