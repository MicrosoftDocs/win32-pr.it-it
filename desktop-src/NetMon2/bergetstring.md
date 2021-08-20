---
description: La funzione BERGetString decodifica una stringa con codifica BER.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: Funzione BERGetString (Netmon.h)
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
ms.openlocfilehash: 4a44acd1246dd73f8c99a34dd429ff93345912d5a106583dcdd865b4a803d70e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796317"
---
# <a name="bergetstring-function"></a>Funzione BERGetString

La **funzione BERGetString** decodifica una stringa con codifica BER.

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

Se la funzione ha esito positivo, ovvero se viene decodificata una stringa valida con codifica BER, il valore restituito è **TRUE.**

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




