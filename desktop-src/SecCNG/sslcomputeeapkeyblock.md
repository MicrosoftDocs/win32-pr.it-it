---
description: Calcola il blocco di chiavi usato dal protocollo EAP (Extensible Authentication Protocol).
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: Funzione SslComputeEapKeyBlock (Sslprovider.h)
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
ms.openlocfilehash: 48f657f565c239f797fd67b108ce3b18b692dfabc0248e1005465e9123ac492d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907172"
---
# <a name="sslcomputeeapkeyblock-function"></a>Funzione SslComputeEapKeyBlock

La **funzione SslComputeEapKeyBlock** calcola il blocco di chiavi usato da Extensible Authentication Protocol (EAP).

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

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle [*dell'istanza del*](/windows/desktop/SecGloss/s-gly) provider Secure Sockets Layer protocollo SSL (Secure Sockets Layer Protocol).

</dd> <dt>

*hMasterKey* \[ Pollici\]
</dt> <dd>

Handle [*dell'oggetto chiave master.*](/windows/desktop/SecGloss/m-gly)

</dd> <dt>

*pbRandoms* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer che contiene una concatenazione dei valori casuali client e \_ server \_ casuali della sessione SSL.

</dd> <dt>

*cbRandoms* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbRandoms.*

</dd> <dt>

*pbOutput* \[ out, facoltativo\]
</dt> <dd>

Indirizzo di un buffer che riceve il BLOB della chiave. Il *parametro cbOutput* contiene le dimensioni di questo buffer. Se questo parametro è **NULL,** questa funzione inserirà le dimensioni richieste, in byte, nel **valore DWORD** a cui punta *il parametro pcbResult.*

</dd> <dt>

*cbOutput* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, del buffer *pbOutput.*

</dd> <dt>

*pcbResult* \[ Cambio\]
</dt> <dd>

Puntatore a un **valore DWORD** che specifica la lunghezza, in byte, dell'hash scritto nel buffer *pbOutput.*

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Impostare su **NCRYPT \_ SSL SERVER \_ \_ FLAG** per indicare che si tratta di una chiamata al server.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.



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



 

