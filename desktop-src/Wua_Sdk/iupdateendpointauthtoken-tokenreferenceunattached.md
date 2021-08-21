---
description: Ottiene il formato XML di un riferimento non associato al token.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: Metodo IUpdateEndpointAuthToken::TokenReferenceUnattached (UpdateEndpointAuth.h)
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
ms.openlocfilehash: 2dada627d6e2b8832f4317c47e54a9c4417e14b821f6cd84bce44d9f53c99aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049249"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a>Metodo IUpdateEndpointAuthToken::TokenReferenceUnattached

Ottiene il formato XML di un riferimento non associato al token.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszTokenReference* \[ Cambio\]
</dt> <dd>

Puntatore al riferimento al token non associato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo. In caso contrario, restituisce un codice di errore COM o Windows errore.

## <a name="remarks"></a>Commenti

Un riferimento non associato fa riferimento a un riferimento ,ad esempio la firma che usa il token, che non si trova nel messaggio in cui si trova il token.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>                   |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con app desktop SP3 \[\]<br/>                |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




