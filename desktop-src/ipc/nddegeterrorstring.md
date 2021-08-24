---
description: Converte un codice di errore restituito da una funzione DDE di rete in una stringa di errore che spiega il codice di errore restituito.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: Funzione NDdeGetErrorString (Nddeapi.h)
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
ms.openlocfilehash: 728ccd283f0f65caafd6f23781bd75f18e9c796ad2fb147f00ab6350c53bfd2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557041"
---
# <a name="nddegeterrorstring-function"></a>Funzione NDdeGetErrorString

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Converte un codice di errore restituito da una funzione DDE di rete in una stringa di errore che spiega il codice di errore restituito.

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

*uErrorCode* \[ Pollici\]
</dt> <dd>

Codice di errore da convertire in una stringa di errore.

</dd> <dt>

*lpszErrorString* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve la stringa di errore tradotta. Questo parametro non può essere **NULL.** Se le dimensioni del buffer non sono sufficienti per archiviare la stringa di errore completa, la stringa viene troncata.

</dd> <dt>

*cBufSize* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer per la ricezione della stringa di errore, in **TCHAR.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è zero.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero. Se il buffer *lpszErrorString* non è sufficientemente grande da accettare la stringa di errore completa e la stringa viene troncata, la funzione restituisce il valore NDDE \_ INTERNAL \_ ERROR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeGetErrorStringW** (Unicode) e **NDdeGetErrorStringA** (ANSI)<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica delle Dynamic Data Exchange rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> </dl>

 

 




