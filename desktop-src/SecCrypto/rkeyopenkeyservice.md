---
description: La funzione RKeyOpenKeyService non è supportata.
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: Funzione RKeyOpenKeyService (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ce905594d1ed088eb72dc59a1fa6beec576384ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314692"
---
# <a name="rkeyopenkeyservice-function"></a>RKeyOpenKeyService (funzione)

La funzione **RKeyOpenKeyService** non è supportata.

**Windows Server 2003:** La funzione **RKeyOpenKeyService** stabilisce una connessione a un computer remoto e apre un handle del servizio Key. L'handle del servizio chiave può essere successivamente usato dalla funzione [**RKeyPFXInstall**](rkeypfxinstall.md) . Si noti che questo comportamento è stato modificato con Windows Server 2003 con Service Pack 1 (SP1).

## <a name="syntax"></a>Sintassi


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszMachineName* \[ in\]
</dt> <dd>

Puntatore long a una stringa con terminazione null che rappresenta il computer in cui verrà aperto l'handle del servizio di chiave.

</dd> <dt>

*TipoProprietario* \[ in\]
</dt> <dd>

[**KEYSVC \_**](keysvc-type.md) Valore di tipo che rappresenta il tipo di chiave. L'unico valore supportato è **KeySvcMachine**.

</dd> <dt>

*pwszOwnerName* \[ in\]
</dt> <dd>

Riservato. Impostare questo valore su **null**.

</dd> <dt>

*pAuthentication* \[ in\]
</dt> <dd>

Puntatore a un **void** che rappresenta le impostazioni di autenticazione. Questo puntatore può puntare a un valore pari a zero o al valore seguente.



| Valore                                                                                                                                                                                                                                                           | Significato                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <dt>**RKEYSVC \_ Connetti \_ \_ solo sicuro**</dt><dt></dt> </dl> | Il client richiede l'autenticazione reciproca. Se viene specificato questo valore, il fallback a NTLM avrà esito negativo.<br/> |



 

</dd> <dt>

*mantenuta* \[ in uscita\]
</dt> <dd>

Riservato. Impostare questo valore su **null**.

</dd> <dt>

*phKeySvcCli* \[ out\]
</dt> <dd>

Puntatore a un [**\_ handle KEYSVCC**](keysvcc-handle.md) che riceve l'handle di servizio della chiave aperta. Al termine dell'utilizzo dell'handle, liberare la risorsa chiamando la funzione [**RKeyCloseKeyService**](rkeyclosekeyservice.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è \_ OK.

Se la funzione ha esito negativo, il valore restituito è un **ULONG** che indica l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




