---
description: La funzione BERGetHeader decodifica un'intestazione di scelta.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: Funzione BERGetHeader (Netmon.h)
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
ms.openlocfilehash: d6dfd50856202e78177d2ad259b16638f466d9bca236a691c65802ce2758c948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012311"
---
# <a name="bergetheader-function"></a>Funzione BERGetHeader

La **funzione BERGetHeader** decodifica un'intestazione di scelta.

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

Puntatore all'intestazione choice.

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

Puntatore alla lunghezza dei dati restituita.

</dd> <dt>

*ppNext* 
</dt> <dd>

Puntatore al contenuto dell'intestazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, ovvero viene trovata un'intestazione beR choice valida, il valore restituito è **TRUE.**

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




