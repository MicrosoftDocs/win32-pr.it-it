---
description: La funzione VarLenSmallIntToDword converte un small integer a lunghezza variabile in un valore DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Funzione VarLenSmallIntToDword (Netmon.h)
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
ms.openlocfilehash: ffec440adc903ddb9a5157e8e5f36037e092f0c4bf0cd52da79b0839220366ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962731"
---
# <a name="varlensmallinttodword-function"></a>Funzione VarLenSmallIntToDword

La **funzione VarLenSmallIntToDword** converte un small integer a lunghezza variabile in **un valore DWORD**.

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

Puntatore all'intero piccolo a lunghezza variabile.

</dd> <dt>

*ValueLen* 
</dt> <dd>

Lunghezza (in byte) dell'intero piccolo a lunghezza variabile.

</dd> <dt>

*fIsByteswapped* 
</dt> <dd>

Flag che indica se l'intero piccolo a lunghezza variabile viene scambiato con byte.

</dd> <dt>

*lpDword* 
</dt> <dd>

Valore **DWORD in** cui viene convertito l'intero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un puntatore al **valore DWORD**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




