---
description: Recupera i nomi di tutte le condivisioni DDE di rete considerate attendibili nel contesto del processo chiamante.
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: Funzione NDdeTrustedShareEnum (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeTrustedShareEnum
- NDdeTrustedShareEnumA
- NDdeTrustedShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: caa3f7c20b95243e03c0c6025d1ff32d60443ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348246"
---
# <a name="nddetrustedshareenum-function"></a>NDdeTrustedShareEnum (funzione)

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

Recupera i nomi di tutte le condivisioni DDE di rete considerate attendibili nel contesto del processo chiamante.

## <a name="syntax"></a>Sintassi


```C++
UINT NDdeTrustedShareEnum(
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

*lpszServer* \[ in\]
</dt> <dd>

Nome del server in cui risiede l'DSDM.

</dd> <dt>

*nLevel* \[ in\]
</dt> <dd>

Riservato. Questo parametro deve essere zero.

</dd> <dt>

*lpBuffer* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve l'elenco di condivisioni DDE attendibili. L'elenco di condivisioni DDE attendibili viene restituito come sequenza di stringhe separate da null che terminano con un carattere null doppio alla fine. Questo parametro può essere **NULL**. Se *lpBuffer* è **null**, DSDM restituisce la dimensione del buffer necessaria per memorizzare l'elenco di condivisioni nel campo *lpcbTotalAvailable* .

</dd> <dt>

*cBufSize* \[ in\]
</dt> <dd>

Dimensioni in byte del buffer *lpBuffer* . Questo parametro deve essere zero se *lpBuffer* è **null**.

</dd> <dt>

*lpnEntriesRead* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero totale di condivisioni attendibili enumerate. Questo parametro non può essere **null**.

</dd> <dt>

*lpcbTotalAvailable* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero totale di byte necessari per archiviare l'elenco di condivisioni DDE attendibili. Questo parametro non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md). Se il parametro *lpBuffer* è **null**, restituisce NDDE \_ BUF \_ troppo \_ piccolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeTrustedShareEnumW** (Unicode) e **NDdeTrustedShareEnumA** (ANSI)<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Dynamic Data Exchange di rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> </dl>

 

 




