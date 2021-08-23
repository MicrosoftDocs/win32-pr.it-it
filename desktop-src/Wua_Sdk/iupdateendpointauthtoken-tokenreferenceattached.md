---
description: Ottiene il formato XML di un riferimento associato al token.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: Metodo IUpdateEndpointAuthToken::TokenReferenceAttached (UpdateEndpointAuth.h)
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
ms.openlocfilehash: eae5e616e8583e2a1da8f8aa0882ea25160faad3f064734620466a0353736efe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793861"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a>Metodo IUpdateEndpointAuthToken::TokenReferenceAttached

Ottiene il formato XML di un riferimento associato al token.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszTokenReference* \[ Cambio\]
</dt> <dd>

Puntatore al riferimento al token associato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo. In caso contrario, restituisce un codice di errore COM o Windows errore.

## <a name="remarks"></a>Commenti

Un riferimento allegato fa riferimento a un riferimento (ad esempio la firma che usa il token) che si trova nello stesso messaggio in cui si trova il token.

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

 

 




