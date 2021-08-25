---
description: Ottiene l'identificatore del servizio da autenticare con il token dell'endpoint.
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: Metodo IUpdateEndpointAuthToken::ServiceID (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.ServiceID
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: fd7e15059db01062fae290d9c4da46a9ef07683acae9f2e58afe29830817c787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855791"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a>Metodo IUpdateEndpointAuthToken::ServiceID

Ottiene l'identificatore del servizio da autenticare con il token dell'endpoint.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pServiceID* \[ Cambio\]
</dt> <dd>

Identificatore del servizio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo. In caso contrario, restituisce un codice di Windows COM o .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>                   |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server solo con app desktop SP3 \[\]<br/>                |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




