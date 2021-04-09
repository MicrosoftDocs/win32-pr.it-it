---
description: La funzione BERGetString decodifica una stringa con codifica BER.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: Funzione BERGetString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881449"
---
# <a name="bergetstring-function"></a>BERGetString (funzione)

La funzione **BERGetString** decodifica una stringa con codifica BER.

## <a name="syntax"></a>Sintassi


```C++
BOOL BERGetString(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCurrentPointer* 
</dt> <dd>

Puntatore alla stringa decodificata.

</dd> <dt>

*ppValuePointer* 
</dt> <dd>

Puntatore al puntatore della stringa decodificata.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Puntatore alla lunghezza dell'intestazione restituita.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Puntatore alla lunghezza della stringa.

</dd> <dt>

*ppNext* 
</dt> <dd>

Puntatore al puntatore della voce BER successiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo (ovvero se una stringa con codifica BER valida è decodificata), il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




