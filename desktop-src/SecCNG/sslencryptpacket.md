---
description: Crittografa un singolo pacchetto SSL (Secure Sockets Layer Protocol).
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: Funzione SslEncryptPacket (Sslprovider. h)
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
ms.openlocfilehash: e839b37e839fd09d5df5f9902474b7ce7c4c74a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319386"
---
# <a name="sslencryptpacket-function"></a>SslEncryptPacket (funzione)

La funzione **SslEncryptPacket** crittografa un singolo pacchetto SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

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

*hSslProvider* \[ in\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL.

</dd> <dt>

*HKEY* \[ in uscita\]
</dt> <dd>

Handle per la chiave utilizzata per crittografare il pacchetto.

</dd> <dt>

*pbInput* \[ in\]
</dt> <dd>

Puntatore al buffer che contiene il pacchetto da crittografare.

</dd> <dt>

*cbInput* \[ in\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbInput* .

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Puntatore a un buffer per ricevere il pacchetto crittografato.

</dd> <dt>

*cbOutput* \[ in\]
</dt> <dd>

Lunghezza, byte, del buffer *pbOutput* .

</dd> <dt>

*pcbResult* \[ out\]
</dt> <dd>

Numero di byte scritti nel buffer *pbOutput* .

</dd> <dt>

*SequenceNumber* \[ in\]
</dt> <dd>

Numero di sequenza che corrisponde a questo pacchetto.

</dd> <dt>

*dwContentType* \[ in\]
</dt> <dd>

Tipo di contenuto che corrisponde a questo pacchetto, che specifica il protocollo di livello superiore usato per elaborare il pacchetto incluso.



| Valore                                                                                                                                                                                                                                           | Significato                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <dt>**CT \_ MODIFICARE \_ la \_ specifica di crittografia**</dt> <dt>20</dt> </dl> | Indica una modifica della strategia di crittografia.<br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <dt>**CT \_ AVVISO**</dt> <dt>21</dt> </dl>                                          | Indica che il pacchetto racchiuso contiene un avviso.<br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <dt>**CT \_ HANDSHAKe**</dt> <dt>22</dt> </dl>                              | Indica che il pacchetto racchiuso fa parte del protocollo di handshake.<br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt> </dl>            | Indica che il pacchetto contiene i dati dell'applicazione.<br/>                  |



 

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

