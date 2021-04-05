---
description: Richiedere un token per l'endpoint del servizio usando le credenziali specificate.
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'Metodo IUpdateEndpointAuthProvider:: GetEndpointToken (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752079"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a>Metodo IUpdateEndpointAuthProvider:: GetEndpointToken

Richiedere un token per l'endpoint del servizio usando le credenziali specificate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ServiceID* \[ in\]
</dt> <dd>

Identifica il servizio da aggiornare.

</dd> <dt>

*EndpointType* \[ in\]
</dt> <dd>

Identifica il tipo di endpoint implementato dal servizio.

</dd> <dt>

*proxySettings* \[ in\]
</dt> <dd>

Impostazioni da utilizzare per la connessione a un server proxy. Per ulteriori informazioni, vedere la struttura [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) .

</dd> <dt>

*hUserToken* \[ in\]
</dt> <dd></dd> <dt>

*TokenType* \[ in\]
</dt> <dd>

Identifica il tipo di token di autenticazione utilizzato per l'autenticazione.

</dd> <dt>

*fRefreshOnline* \[ in\]
</dt> <dd>

Indica che WUA Weather richiede un nuovo token. True indica che è richiesto un nuovo token. False indica che è richiesto un token nuovo o memorizzato nella cache. Per ulteriori informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*ppEndpointToken* \[ out\]
</dt> <dd>

Specificare il token dell'endpoint da utilizzare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo. In caso contrario, restituisce un codice di errore COM o Windows.

## <a name="remarks"></a>Commenti

WUA imposta in genere il parametro fRefreshOnline su false quando il metodo viene chiamato per la prima volta, quindi se si verifica un errore di connessione WUA imposta tale parametro su true quando il metodo viene chiamato nuovamente. Tuttavia, l'implementazione di questo metodo può richiedere un nuovo token da un servizio token di sicurezza (STS) o fornire un token memorizzato nella cache in qualsiasi momento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>                   |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>                |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUpdateEndpointAuthProvider**](iupdateendpointauthprovider.md)
</dt> </dl>

 

 




