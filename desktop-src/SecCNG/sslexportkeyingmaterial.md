---
description: Esporta il materiale di keying in base allo standard RFC 5705.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: Funzione SslExportKeyingMaterial (Sslprovider.h)
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
ms.openlocfilehash: 39aaebba64f92794e179af95a5a175e2603fccc40410989cfcd427c6a7a1a88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906619"
---
# <a name="sslexportkeyingmaterial-function"></a>Funzione SslExportKeyingMaterial

Esporta il materiale di keying in base [allo standard RFC 5705.](https://tools.ietf.org/html/rfc5705) Questa funzione usa la funzione pseudocasuale TLS per produrre un buffer di byte di materiale per la chiave. Accetta un riferimento all'master secret, all'etichetta ASCII disambiguazione, ai valori casuali del client e del server e, facoltativamente, ai dati del contesto dell'applicazione.

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

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle dell'istanza del provider del protocollo TLS.

</dd> <dt>

*hMasterKey* \[ Pollici\]
</dt> <dd>

Handle dell'oggetto chiave master che verrà usato per creare il materiale della chiave in br esportato.

</dd> <dt>

*Etichetta s* \[ Pollici\]
</dt> <dd>

Stringa di etichetta ASCII con terminazione NUL. Schannel rimuoverà il carattere NUL di terminazione prima di passarlo alla funzione pseudocasuale.

</dd> <dt>

*pbRandoms* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer che contiene una concatenazione dei valori *\_ casuali client* e *server \_ casuali* della connessione TLS.

</dd> <dt>

*cbRandoms* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbRandoms.*

</dd> <dt>

*pbContextValue* \[ in, facoltativo\]
</dt> <dd>

Puntatore a un buffer che contiene il contesto dell'applicazione. Se *pbContextValue* è **NULL,** *cbContextValue* deve essere zero.

</dd> <dt>

*cbContextValue* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbContextValue.*

</dd> <dt>

*pbOutput* \[ Cambio\]
</dt> <dd>

Indirizzo di un buffer che riceve il materiale di keying esportato. Il *parametro cbOutput* contiene le dimensioni di questo buffer. Questo valore non può essere **NULL.**

</dd> <dt>

*cbOutput* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbOutput.* Deve essere maggiore di zero.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Non usato. Deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati, i seguenti.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl> | Uno degli handle forniti non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




