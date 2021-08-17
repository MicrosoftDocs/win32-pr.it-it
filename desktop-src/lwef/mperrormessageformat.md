---
title: Funzione MpErrorMessageFormat (MpClient.h)
description: Restituisce un messaggio di errore formattato in base a un codice di errore.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Funzionalità dell'ambiente di Windows MpErrorMessageFormat
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
ms.openlocfilehash: 124bf9e2c5c2ecc18f286b99f0c3b93695abd3f6a40853fcc47de580edef5db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883508"
---
# <a name="mperrormessageformat-function"></a>Funzione MpErrorMessageFormat

Restituisce un messaggio di errore formattato in base a un codice di errore.

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

*hMpHandle* \[ Pollici\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per l'interfaccia di Malware Protection Manager. Questo handle viene restituito dalla [**funzione MpManagerOpen.**](mpmanageropen.md)

</dd> <dt>

*hrError* \[ Pollici\]
</dt> <dd>

Tipo: **HRESULT**

Codice di errore basato su **HRESULT.**

</dd> <dt>

*pwszErrorDesc* \[ Cambio\]
</dt> <dd>

Tipo: **LPWSTR \***

Restituisce un messaggio di errore formattato in base *a hrError*. Questa stringa deve essere liberata usando [**MpFreeMemory**](mpfreememory.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

Se la funzione ha esito negativo, il valore restituito è un **codice HRESULT non** riuscito.

## <a name="remarks"></a>Commenti

Questa funzione è in grado di formattare i codici di errore di sistema oltre a codici di errore specifici restituiti dalle funzioni di protezione da malware. I **codici di errore HRESULT** specifici delle funzioni di protezione da malware hanno una funzionalità di 0x50. Di seguito è riportato un elenco di un subset dei codici di errore specifici della protezione da malware che possono essere restituiti da varie funzioni di protezione antimalware. Usando la macro **HRESULT \_ FROM MP \_ \_ STATUS**, i codici di errore seguenti possono essere convertiti in **HRESULT**. Per un elenco di altri possibili codici di errore, vedere anche Codici di errore del motore [antimalware](https://support.microsoft.com/kb/939359) di Forefront Client Security.



| Codice di errore                              | Descrizione                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ MP \_ NOENGINE                     | Nessun motore viene caricato nel servizio antimalware per eseguire l'operazione richiesta.                                              |
| MEMORIA \_ NON DISPONIBILE PER L'MP DI \_ \_ ERRORE                   | Il motore antimalware ha rilevato una situazione di memoria insufficiente.                                                               |
| RIMOZIONE \_ DELL'MP \_ DI ERRORE NON \_ RIUSCITA               | L'operazione di rimozione non è riuscita per una minaccia specifica.                                                                              |
| ERRORE \_ DI QUARANTENA MP NON \_ \_ RIUSCITA           | Operazione di quarantena non riuscita per una minaccia specifica.                                                                          |
| ERRORE \_ MP THREAT NON \_ \_ \_ TROVATO           | La minaccia specifica non esiste più nel sistema.                                                                         |
| RIMOZIONE \_ DI GESTIONE ERRORI NON \_ \_ \_ SUPPORTATA       | L'operazione di rimozione per una minaccia specifica all'interno del tipo di contenitore non è supportata.                                          |
| ERROR \_ MP \_ REMOVE IMMUTABLE CONTAINER (RIMUOVI \_ CONTENITORE NON \_ MODIFICABILE) | A causa dei criteri del motore, non è supportata un'operazione di rimozione di una minaccia specifica all'interno di un contenitore bloccato. (Archivi di posta.) |
| ERRORE \_ MP \_ BADDB \_ OLDENGINE             | La richiesta di aggiornamento della firma ha fornito un motore o file di firma meno recenti.                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[Codici di errore del motore antimalware di Forefront Client Security](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





