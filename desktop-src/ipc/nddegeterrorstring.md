---
description: Converte un codice di errore restituito da una funzione DDE di rete in una stringa di errore che descrive il codice di errore restituito.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: Funzione NDdeGetErrorString (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8e043c8281d3ad049346ac7ce68991eb6bd08af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049347"
---
# <a name="nddegeterrorstring-function"></a>NDdeGetErrorString (funzione)

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

Converte un codice di errore restituito da una funzione DDE di rete in una stringa di errore che descrive il codice di errore restituito.

## <a name="syntax"></a>Sintassi


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*codice uerrorcode* \[ in\]
</dt> <dd>

Codice di errore da convertire in una stringa di errore.

</dd> <dt>

*lpszErrorString* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve la stringa di errore tradotta. Questo parametro non può essere **null**. Se il buffer non è sufficientemente grande da archiviare la stringa di errore completa, la stringa viene troncata.

</dd> <dt>

*cBufSize* \[ in\]
</dt> <dd>

Dimensione del buffer in cui ricevere la stringa di errore, in **TCHARs**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è zero.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero. Se il buffer *lpszErrorString* non è sufficientemente grande da accettare la stringa di errore completa e la stringa viene troncata, la funzione restituisce il valore \_ errore interno di NDDE \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeGetErrorStringW** (Unicode) e **NDdeGetErrorStringA** (ANSI)<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Dynamic Data Exchange di rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> </dl>

 

 




