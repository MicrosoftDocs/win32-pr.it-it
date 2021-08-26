---
description: Recupera l'elenco di condivisioni DDE disponibili.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: Funzione NDdeShareEnum (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareEnum
- NDdeShareEnumA
- NDdeShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: e6b101a7ba45e28175a8d6ee0730e704a6f519142f94e4fc2273d1d76dcfe1cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014741"
---
# <a name="nddeshareenum-function"></a>Funzione NDdeShareEnum

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Recupera l'elenco di condivisioni DDE disponibili.

## <a name="syntax"></a>Sintassi


```C++
UINT NDdeShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ Pollici\]
</dt> <dd>

Nome del server in cui risiede DSDM.

</dd> <dt>

*nLevel* \[ Pollici\]
</dt> <dd>

Riservato. Questo parametro deve essere zero.

</dd> <dt>

*lpBuffer* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve l'elenco di condivisioni DDE. L'elenco di condivisioni DDE viene archiviato come sequenza di stringhe separate da Null che terminano con un carattere null doppio alla fine. Questo parametro può essere **NULL**. Se *lpBuffer* è **NULL,** DSDM restituisce le dimensioni del buffer necessarie per contenere l'elenco di condivisioni nel *parametro lpcbTotalAvailable.*

</dd> <dt>

*cBufSize* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer *lpBuffer,* in byte. Questo parametro deve essere zero se *lpBuffer* è **NULL.**

</dd> <dt>

*lpnEntriesRead* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero totale di condivisioni enumerate. Questo parametro non può essere **NULL.**

</dd> <dt>

*lpcbTotalAvailable* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero totale di byte necessari nel buffer per archiviare l'elenco di condivisioni DDE. Questo parametro non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ NO \_ ERROR.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md). Se il *parametro lpBuffer* è **NULL,** restituisce NDDE \_ BUF \_ TOO \_ SMALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeShareEnumW** (Unicode) e **NDdeShareEnumA** (ANSI)<br/>                  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica Dynamic Data Exchange rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> </dl>

 

 




