---
description: Ottiene il formato XML di un riferimento non associato al token.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'Metodo IUpdateEndpointAuthToken:: TokenReferenceUnattached (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307616"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a>Metodo IUpdateEndpointAuthToken:: TokenReferenceUnattached

Ottiene il formato XML di un riferimento non associato al token.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszTokenReference* \[ out\]
</dt> <dd>

Puntatore al riferimento al token non collegato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se ha esito positivo. In caso contrario, restituisce un codice di errore COM o Windows.

## <a name="remarks"></a>Commenti

Un riferimento non collegato fa riferimento a un Referece, ad esempio signiture che usa il token, che non è presente nel messaggio in cui risiede il token.

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

 

 




