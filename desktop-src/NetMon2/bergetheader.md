---
description: La funzione BERGetHeader decodifica un'intestazione Choice.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: Funzione BERGetHeader (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311641"
---
# <a name="bergetheader-function"></a>BERGetHeader (funzione)

La funzione **BERGetHeader** decodifica un'intestazione Choice.

## <a name="syntax"></a>Sintassi


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCurrentPointer* 
</dt> <dd>

Puntatore all'intestazione Choice.

</dd> <dt>

*pTag* 
</dt> <dd>

Puntatore al tag restituito.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Puntatore alla lunghezza dell'intestazione restituita.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Puntatore alla lunghezza dei dati restituiti.

</dd> <dt>

*ppNext* 
</dt> <dd>

Puntatore al contenuto dell'intestazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, ovvero viene trovata un'intestazione Choice BER valida, il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




