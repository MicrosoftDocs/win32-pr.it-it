---
title: Funzione MpErrorMessageFormat (MpClient. h)
description: Restituisce un messaggio di errore formattato basato su un codice di errore.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpErrorMessageFormat
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a3499b3be885b29135d22b470da4143cfb23ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964797"
---
# <a name="mperrormessageformat-function"></a>MpErrorMessageFormat (funzione)

Restituisce un messaggio di errore formattato basato su un codice di errore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMpHandle* \[ in\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per l'interfaccia di malware Protection Manager. Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*hrError* \[ in\]
</dt> <dd>

Tipo: **HRESULT**

Codice di errore basato su **HRESULT**.

</dd> <dt>

*pwszErrorDesc* \[ out\]
</dt> <dd>

Tipo: **LPWSTR \** _

Restituisce un messaggio di errore formattato basato su _hrError *. Questa stringa deve essere liberata usando [**MpFreeMemory**](mpfreememory.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.

## <a name="remarks"></a>Commenti

Questa funzione è in grado di formattare i codici di errore di sistema oltre a codici di errore specifici restituiti dalle funzioni di malware Protection. I codici di errore **HRESULT** specifici per le funzioni di malware Protection hanno una struttura di 0x50. Di seguito è riportato un elenco di un subset di codici di errore specifici di malware Protection che possono essere restituiti da varie funzioni di malware Protection. Utilizzando la macro **HRESULT \_ dallo \_ \_ stato MP**, i codici di errore seguenti possono essere convertiti in **HRESULT**. Vedere anche [codici di errore del motore anti-malware di Forefront Client Security](https://support.microsoft.com/kb/939359) per un elenco di altri possibili codici di errore.



| Codice di errore                              | Descrizione                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ MP \_ noengine                     | Nessun motore è caricato nel servizio antimalware per eseguire l'operazione richiesta.                                              |
| ERRORE \_ MP \_ Nessuna \_ memoria                   | Il motore antimalware ha rilevato una situazione di memoria insufficiente.                                                               |
| ERRORE \_ \_ rimozione MP \_ non riuscita               | Operazione di rimozione non riuscita per una minaccia specifica.                                                                              |
| ERRORE \_ \_ quarantena MP \_ non riuscita           | Operazione di quarantena non riuscita per una minaccia specifica.                                                                          |
| rischio di errore \_ MP \_ \_ non \_ trovato           | La minaccia specifica non esiste più nel sistema.                                                                         |
| ERRORE \_ di \_ rimozione MP \_ non \_ supportata       | L'operazione di rimozione per una minaccia specifica all'interno del tipo di contenitore non è supportata.                                          |
| ERRORE \_ MP \_ rimozione del \_ contenitore non modificabile \_ | A causa dei criteri del motore, un'operazione di rimozione di una minaccia specifica all'interno di un contenitore bloccato non è supportata. (Archivi di posta elettronica). |
| ERRORE \_ MP \_ BADDB \_ OLDENGINE             | La richiesta di aggiornamento della firma ha fornito un motore o uno o più file di firma meno recenti.                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[Codici di errore del motore anti-malware di Forefront Client Security](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





