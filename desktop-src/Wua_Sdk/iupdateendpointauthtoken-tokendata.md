---
description: Ottiene i dati XML (inviati in rete) che rappresenta il token.
ms.assetid: 52EC991A-0499-4182-AC4F-512BAFB4F896
title: 'Metodo IUpdateEndpointAuthToken:: TokenData (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenData
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: e75df7f5b13eaf36854cf7ed9abc5988b02462ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307620"
---
# <a name="iupdateendpointauthtokentokendata-method"></a>Metodo IUpdateEndpointAuthToken:: TokenData

Ottiene i dati XML (inviati in rete) che rappresenta il token.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TokenData(
  [out] BSTR *pszTokenData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszTokenData* \[ out\]
</dt> <dd>

Dati XML (inviati in rete) che rappresentano il token. Ad esempio, i dati per un token WS-Security SAML (Security Assertion Markup Language) 1,1 sono il codice SAML aggiunto alla richiesta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se ha esito positivo. In caso contrario, restituisce un codice di errore COM o Windows.

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

 

 




