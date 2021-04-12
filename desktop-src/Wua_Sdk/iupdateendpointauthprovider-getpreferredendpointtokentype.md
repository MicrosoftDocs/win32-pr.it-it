---
description: Restituisce il tipo preferito di token di autenticazione per l'endpoint del servizio.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'Metodo IUpdateEndpointAuthProvider:: GetPreferredEndpointTokenType (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 670835ee3c2dfd01ae46a7cf78395959ea9a26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226227"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a>Metodo IUpdateEndpointAuthProvider:: GetPreferredEndpointTokenType

Restituisce il tipo preferito di token di autenticazione per l'endpoint del servizio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
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

Identifica il tipo di endpoint tneeded per la connessione al servizio.

</dd> <dt>

*ulRequestedTypes* \[ in\]
</dt> <dd>

Identifica il set di token ORed supportati dall'endpoint.

</dd> <dt>

*pulPreferredTokenTypes* \[ out\]
</dt> <dd>

Specificare il set di tipi di token di autenticazione ORed preferiti. (Impostare su 0 per indicare che non è necessario alcun token di autenticazione).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo. In caso contrario, restituisce un codice di errore COM o Windows.

## <a name="remarks"></a>Commenti

Quando viene restituito questo metodo, WUA sceglie un tipo di token dai tipi preferiti e lo passa al parametro tokenType del metodo [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) .

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
</dt> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




