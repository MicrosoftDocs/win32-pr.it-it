---
description: Recupera i nomi di tutte le condivisioni DDE di rete attendibili nel contesto del processo chiamante.
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: Funzione NDdeTrustedShareEnum (Nddeapi.h)
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
ms.openlocfilehash: fc8eefd335ad9c54e7dc4aefa5a1027785de1b9c33cd3346c8bb1c8a4872b939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695043"
---
# <a name="nddetrustedshareenum-function"></a>Funzione NDdeTrustedShareEnum

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Recupera i nomi di tutte le condivisioni DDE di rete attendibili nel contesto del processo chiamante.

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

Puntatore a un buffer che riceve l'elenco di condivisioni DDE attendibili. L'elenco di condivisioni DDE attendibili viene restituito come sequenza di stringhe separate da Null che terminano con un carattere Null doppio alla fine. Questo parametro può essere **NULL**. Se *lpBuffer* è **NULL,** DSDM restituisce le dimensioni del buffer necessarie per contenere l'elenco di condivisioni nel campo *lpcbTotalAvailable.*

</dd> <dt>

*cBufSize* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer *lpBuffer,* in byte. Questo parametro deve essere zero se *lpBuffer* è **NULL.**

</dd> <dt>

*lpnEntriesRead* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero totale di condivisioni attendibili enumerate. Questo parametro non può essere **NULL.**

</dd> <dt>

*lpcbTotalAvailable* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero totale di byte necessari per archiviare l'elenco di condivisioni DDE attendibili. Questo parametro non può essere **NULL.**

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
| Nomi Unicode e ANSI<br/>   | **NDdeTrustedShareEnumW** (Unicode) e **NDdeTrustedShareEnumA** (ANSI)<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica Dynamic Data Exchange rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> </dl>

 

 




