---
description: Calcola il blocco di chiavi utilizzato da Extensible Authentication Protocol (EAP).
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: Funzione SslComputeEapKeyBlock (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: d46c1284b208975126067ff295507b51def9133b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310767"
---
# <a name="sslcomputeeapkeyblock-function"></a>SslComputeEapKeyBlock (funzione)

La funzione **SslComputeEapKeyBlock** calcola il blocco di chiave utilizzato da Extensible Authentication Protocol (EAP).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ in\]
</dt> <dd>

Handle dell'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

</dd> <dt>

*hMasterKey* \[ in\]
</dt> <dd>

Handle dell'oggetto [*chiave master*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*pbRandoms* \[ in\]
</dt> <dd>

Puntatore a un buffer che contiene una concatenazione dei valori casuali del client \_ e del server \_ casuale della sessione SSL.

</dd> <dt>

*cbRandoms* \[ in\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbRandoms* .

</dd> <dt>

*pbOutput* \[ out, facoltativo\]
</dt> <dd>

Indirizzo di un buffer che riceve il BLOB della chiave. Il parametro *cbOutput* contiene la dimensione del buffer. Se questo parametro è **null**, questa funzione inserisce la dimensione richiesta, in byte, nel **valore DWORD** a cui fa riferimento il parametro *pcbResult* .

</dd> <dt>

*cbOutput* \[ in\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbOutput* .

</dd> <dt>

*pcbResult* \[ out\]
</dt> <dd>

Puntatore a un valore **DWORD** che specifica la lunghezza, in byte, dell'hash scritto nel buffer *pbOutput* .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Impostare su **NCRYPT \_ SSL \_ server \_ flag** per indicare che si tratta di una chiamata al server.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.



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



 

