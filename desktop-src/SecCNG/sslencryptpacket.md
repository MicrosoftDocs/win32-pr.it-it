---
description: Crittografa un singolo pacchetto SSL (Single Secure Sockets Layer Protocol).
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: Funzione SslEncryptPacket (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEncryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 74c489cae777b6ca7ac93020fb80ab198622fae97640c09cbd99544c2dafa4e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906663"
---
# <a name="sslencryptpacket-function"></a>Funzione SslEncryptPacket

La **funzione SslEncryptPacket** crittografa [*un singolo pacchetto SSL (Single Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) Protocol).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslEncryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwContentType,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL.

</dd> <dt>

*hKey* \[ in, out\]
</dt> <dd>

Handle per la chiave utilizzata per crittografare il pacchetto.

</dd> <dt>

*pbInput* \[ Pollici\]
</dt> <dd>

Puntatore al buffer che contiene il pacchetto da crittografare.

</dd> <dt>

*cbInput* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbInput.*

</dd> <dt>

*pbOutput* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer per ricevere il pacchetto crittografato.

</dd> <dt>

*cbOutput* \[ Pollici\]
</dt> <dd>

Lunghezza, byte, del buffer *pbOutput.*

</dd> <dt>

*pcbResult* \[ Cambio\]
</dt> <dd>

Numero di byte scritti nel buffer *pbOutput.*

</dd> <dt>

*SequenceNumber* \[ Pollici\]
</dt> <dd>

Numero di sequenza corrispondente a questo pacchetto.

</dd> <dt>

*dwContentType* \[ Pollici\]
</dt> <dd>

Tipo di contenuto che corrisponde a questo pacchetto, che specifica il protocollo di livello superiore utilizzato per elaborare il pacchetto incluso.



| Valore                                                                                                                                                                                                                                           | Significato                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <dt>**CT \_ MODIFICARE \_ LA SPECIFICA DI \_ CRITTOGRAFIA**</dt> <dt>20</dt> </dl> | Indica una modifica nella strategia di crittografia.<br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <dt>**CT \_ AVVISO**</dt> <dt>21</dt> </dl>                                          | Indica che il pacchetto incluso contiene un avviso.<br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <dt>**CT \_ HANDSHAKE**</dt> <dt>22</dt> </dl>                              | Indica che il pacchetto incluso fa parte del protocollo di handshake.<br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt> </dl>            | Indica che il pacchetto contiene dati dell'applicazione.<br/>                  |



 

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

