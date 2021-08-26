---
description: Recupera le informazioni sulla condivisione DDE. Questa operazione viene in genere eseguita per la modifica.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: Funzione NDdeShareGetInfo (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2c622a611b3d917dcf67de2ec6b96070ec0e54e9e53b0cef04c3c9e35b859e40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014751"
---
# <a name="nddesharegetinfo-function"></a>Funzione NDdeShareGetInfo

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Recupera le informazioni sulla condivisione DDE. Questa operazione viene in genere eseguita per la modifica.

## <a name="syntax"></a>Sintassi


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpszServer* \[ Pollici\]
</dt> <dd>

Nome del server in cui risiede DSDM.

</dd> <dt>

*lpszShareName* \[ Pollici\]
</dt> <dd>

Nome della condivisione le cui informazioni devono essere recuperate dal DSDM. Questo parametro non deve essere **NULL.**

</dd> <dt>

*nLevel* \[ Pollici\]
</dt> <dd>

Livello di informazioni. Questo parametro deve essere 2.

</dd> <dt>

*lpBuffer* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve la [**struttura NDDESHAREINFO**](nddeshareinfo-str.md) e i dati associati a cui puntano i relativi membri. Questo parametro può essere **NULL**. Se *lpBuffer* è **NULL,** DSDM calcola il numero di byte necessari per archiviare le informazioni sulla condivisione richieste e restituisce tale valore nel campo *lpnTotalAvailable* insieme all'errore NDDE \_ BUF \_ TOO \_ SMALL.

</dd> <dt>

*cBufSize* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer *lpBuffer,* in byte. Se *lpBuffer* è **NULL,** *cBufSize* deve essere zero.

</dd> <dt>

*lpnTotalAvailable* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero totale di byte necessari per archiviare le informazioni di condivisione richieste. Questo parametro non può essere **NULL.**

</dd> <dt>

*lpnItems* \[ Pollici\]
</dt> <dd>

Puntatore a una maschera di selezione dell'elemento per il recupero parziale delle informazioni sulla condivisione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NDDE \_ NO \_ ERROR.

Se la funzione ha esito negativo, il valore restituito è un codice di errore, che può essere convertito in un messaggio di errore di testo chiamando [**NDdeGetErrorString.**](nddegeterrorstring.md) Se il *parametro lpBuffer* è **NULL,** restituisce NDDE \_ BUF \_ TOO \_ SMALL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **NDdeShareGetInfoW** (Unicode) e **NDdeShareGetInfoA** (ANSI)<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica delle Dynamic Data Exchange rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Funzioni DDE di rete](network-dde-functions.md)
</dt> <dt>

[**NDDESHAREINFO**](nddeshareinfo-str.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> </dl>

 

 




