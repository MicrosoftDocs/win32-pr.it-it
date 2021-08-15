---
description: Ottiene il tipo di token dell'endpoint, ad esempio WS-Security token SAML (Security Assertion Markup Language) 1.1.
ms.assetid: 1C6FFAD7-DC80-4957-96B4-FA0D954786DD
title: Metodo IUpdateEndpointAuthToken::TokenType (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: a4479adc05eba8160098bd60c349645c4e30853abc693396f18f69ec722a06d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815292"
---
# <a name="iupdateendpointauthtokentokentype-method"></a>Metodo IUpdateEndpointAuthToken::TokenType

Ottiene il tipo di token dell'endpoint, ad esempio WS-Security token SAML (Security Assertion Markup Language) 1.1.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TokenType(
  [out] UpdateEndpointAuthTokenType *pTokenType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTokenType* \[ Cambio\]
</dt> <dd>

Tipo del token dell'endpoint.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo. In caso contrario, restituisce un codice di Windows COM o .

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

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




