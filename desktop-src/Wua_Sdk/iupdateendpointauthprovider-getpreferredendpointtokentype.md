---
description: Restituisce il tipo preferito di token di autenticazione per l'endpoint del servizio.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: Metodo IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType (UpdateEndpointAuth.h)
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
ms.openlocfilehash: a9b7d15d6d27170106118c720d25567389884c50e27aac202adedf00290236c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994581"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a>Metodo IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType

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

*serviceId* \[ Pollici\]
</dt> <dd>

Identifica il servizio da aggiornare.

</dd> <dt>

*endpointType* \[ Pollici\]
</dt> <dd>

Identifica il tipo di endpoint a cui è necessario connettersi al servizio.

</dd> <dt>

*ulRequestedTypes* \[ Pollici\]
</dt> <dd>

Identifica il set di token ORed supportati dall'endpoint.

</dd> <dt>

*pulPreferredTokenTypes* \[ Cambio\]
</dt> <dd>

Specificare il set ORed di tipi di token di autenticazione preferiti. Impostare su 0 per indicare che non è necessario alcun token di autenticazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo. In caso contrario, restituisce un codice di Windows COM o .

## <a name="remarks"></a>Commenti

Quando viene restituito questo metodo, WUA sceglie un tipo di token tra i tipi preferiti e lo passa al parametro tokenType del [**metodo GetEndpointToken.**](iupdateendpointauthprovider-getendpointtoken.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>                   |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con solo app desktop SP3 \[\]<br/>                |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUpdateEndpointAuthProvider**](iupdateendpointauthprovider.md)
</dt> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




