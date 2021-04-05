---
description: La funzione BERGetInteger decodifica un valore integer con codifica BER.
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: Funzione BERGetInteger (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883670"
---
# <a name="bergetinteger-function"></a>BERGetInteger (funzione)

La funzione **BERGetInteger** decodifica un valore integer con codifica BER.

## <a name="syntax"></a>Sintassi


```C++
BOOL BERGetInteger(
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

Puntatore all'integer decodificato.

</dd> <dt>

*ppValuePointer* 
</dt> <dd>

Puntatore al puntatore al valore restituito.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Puntatore alla lunghezza dell'intestazione restituita.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Puntatore alla lunghezza dei dati.

</dd> <dt>

*ppNext* 
</dt> <dd>

Puntatore al puntatore alla voce BER successiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, ovvero se viene trovato e convertito un intero con codifica BER valido, il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Parser. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




