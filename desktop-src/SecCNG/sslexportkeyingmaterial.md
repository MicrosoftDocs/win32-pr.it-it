---
description: Esporta il materiale delle chiavi in base allo standard RFC 5705.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: Funzione SslExportKeyingMaterial (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 906a7535b297f309c0c8471843ce07f43a110a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760106"
---
# <a name="sslexportkeyingmaterial-function"></a>SslExportKeyingMaterial (funzione)

Esporta il materiale delle chiavi in base allo [standard RFC 5705](https://tools.ietf.org/html/rfc5705). Questa funzione usa la funzione TLS pseudocasuale per produrre un buffer di byte del materiale per le chiavi. Accetta un riferimento all'master secret, l'etichetta ASCII distinguere, i valori casuali del client e del server e, facoltativamente, i dati del contesto dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ in\]
</dt> <dd>

Handle dell'istanza del provider di protocollo TLS.

</dd> <dt>

*hMasterKey* \[ in\]
</dt> <dd>

Handle dell'oggetto chiave master che verrà usato per creare il materiale per le chiavi in br esportato.

</dd> <dt>

*sLabel* \[ in\]
</dt> <dd>

stringa di etichetta ASCII con terminazione null. Schannel rimuoverà il carattere NUL di terminazione prima di passarlo alla funzione pseudocasuale.

</dd> <dt>

*pbRandoms* \[ in\]
</dt> <dd>

Puntatore a un buffer che contiene una concatenazione dei valori casuali del *client \_* e del *server \_ casuale* della connessione TLS.

</dd> <dt>

*cbRandoms* \[ in\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbRandoms* .

</dd> <dt>

*pbContextValue* \[ in, facoltativo\]
</dt> <dd>

Puntatore a un buffer che contiene il contesto dell'applicazione. Se *pbContextValue* è **null**, *cbContextValue* deve essere zero.

</dd> <dt>

*cbContextValue* \[ in\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbContextValue* .

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Indirizzo di un buffer che riceve il materiale delle chiavi esportate. Il parametro *cbOutput* contiene la dimensione del buffer. Questo valore non può essere **null**.

</dd> <dt>

*cbOutput* \[ in\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbOutput* . Deve essere maggiore di zero.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Non usato. Deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl> | Uno degli handle forniti non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




