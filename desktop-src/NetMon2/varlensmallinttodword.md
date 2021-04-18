---
description: La funzione VarLenSmallIntToDword converte un valore integer di lunghezza variabile, piccolo, in un valore DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Funzione VarLenSmallIntToDword (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310785"
---
# <a name="varlensmallinttodword-function"></a>VarLenSmallIntToDword (funzione)

La funzione **VarLenSmallIntToDword** converte un valore integer di lunghezza variabile, piccolo, in un valore **DWORD**.

## <a name="syntax"></a>Sintassi


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pValue* 
</dt> <dd>

Puntatore al valore integer a lunghezza variabile, piccolo.

</dd> <dt>

*ValueLen* 
</dt> <dd>

Lunghezza (in byte) dell'intero piccolo a lunghezza variabile.

</dd> <dt>

*fIsByteswapped* 
</dt> <dd>

Flag che indica se la lunghezza della variabile Small Integer è scambio di byte.

</dd> <dt>

*lpDword* 
</dt> <dd>

**DWORD** in cui viene convertito il valore integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un puntatore a **DWORD**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




