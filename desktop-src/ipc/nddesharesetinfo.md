---
description: Imposta le informazioni sulla condivisione DDE. Questa operazione viene in genere eseguita dopo la modifica.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: Funzione NDdeShareSetInfo (nddeapi. h)
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
ms.openlocfilehash: cee7660a58e8f2747a800650b79db20f95504f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305709"
---
# <a name="nddesharesetinfo-function"></a>NDdeShareSetInfo (funzione)

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

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

*lpszServer* \[ in\]
</dt> <dd>

Nome del server di cui è necessario modificare il DSDM.

</dd> <dt>

*lpszShareName* \[ in\]
</dt> <dd>

Nome del nome della condivisione di cui è necessario modificare le informazioni. Questo parametro non può essere **null**.

</dd> <dt>

*nLevel* \[ in\]
</dt> <dd>

Livello di informazioni. Questo parametro deve essere 2.

</dd> <dt>

*lpBuffer* \[in\]
</dt> <dd>

Puntatore alla struttura [**NDDESHAREINFO**](nddeshareinfo-str.md) che specifica le informazioni sulla condivisione DDE da archiviare in DSDM. Attualmente, le informazioni sulla condivisione DDE vengono modificate nel suo complesso, ovvero non vengono apportate modifiche parziali. Questo parametro non può essere **null**.

</dd> <dt>

*cBufSize* \[ in\]
</dt> <dd>

Dimensioni in byte del buffer *lpBuffer* .

</dd> <dt>

*sParmNum* \[ in\]
</dt> <dd>

Indice del parametro da modificare. L'implementazione corrente non supporta la modifica parziale; Pertanto, questo parametro deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ senza \_ errori.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString**](nddegeterrorstring.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeShareSetInfoW** (Unicode) e **NDdeShareSetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Dynamic Data Exchange di rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareGetInfo**](nddesharegetinfo.md)
</dt> </dl>

 

 




