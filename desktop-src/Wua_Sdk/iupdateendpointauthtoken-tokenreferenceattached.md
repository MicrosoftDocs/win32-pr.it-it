---
description: Ottiene il formato XML di un riferimento associato al token.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: 'Metodo IUpdateEndpointAuthToken:: TokenReferenceAttached (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 9582c54c42e2416d5d7a98e85eba3151fd6769a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307618"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a>Metodo IUpdateEndpointAuthToken:: TokenReferenceAttached

Ottiene il formato XML di un riferimento associato al token.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszTokenReference* \[ out\]
</dt> <dd>

Puntatore al riferimento al token collegato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se ha esito positivo. In caso contrario, restituisce un codice di errore COM o Windows.

## <a name="remarks"></a>Commenti

Un riferimento collegato fa riferimento a un Referece, ad esempio signiture che usa il token, che si trova nello stesso messaggio in cui risiede il token.

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

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




