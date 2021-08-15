---
description: Imposta le informazioni sulla condivisione DDE. Questa operazione viene in genere eseguita dopo la modifica.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: Funzione NDdeShareSetInfo (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: ccfa8cc80f60477e8512ac43f0e93825642dd0603ee398e232bbb67d6979a4c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481701"
---
# <a name="nddesharesetinfo-function"></a>Funzione NDdeShareSetInfo

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Imposta le informazioni sulla condivisione DDE. Questa operazione viene in genere eseguita dopo la modifica.

## <a name="syntax"></a>Sintassi


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ Pollici\]
</dt> <dd>

Nome del server il cui DSDM deve essere modificato.

</dd> <dt>

*lpszShareName* \[ Pollici\]
</dt> <dd>

Nome del nome della condivisione le cui informazioni devono essere modificate. Questo parametro non può essere **NULL.**

</dd> <dt>

*nLevel* \[ Pollici\]
</dt> <dd>

Livello di informazioni. Questo parametro deve essere 2.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Puntatore alla [**struttura NDDESHAREINFO**](nddeshareinfo-str.md) che specifica le informazioni sulla condivisione DDE da archiviare nel DSDM. Attualmente le informazioni sulla condivisione DDE vengono modificate nel suo complesso, in altre informazioni non vengono apportate modifiche parziali. Questo parametro non può essere **NULL.**

</dd> <dt>

*cBufSize* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer *lpBuffer,* in byte.

</dd> <dt>

*sParmNum* \[ Pollici\]
</dt> <dd>

Indice del parametro da modificare. L'implementazione corrente non supporta la modifica parziale. Pertanto, questo parametro deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ NO \_ ERROR.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString.**](nddegeterrorstring.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeShareSetInfoW** (Unicode) e **NDdeShareSetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica delle Dynamic Data Exchange rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareGetInfo**](nddesharegetinfo.md)
</dt> </dl>

 

 




