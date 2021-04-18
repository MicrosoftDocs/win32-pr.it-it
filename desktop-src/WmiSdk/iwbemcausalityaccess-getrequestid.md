---
description: Il metodo GetRequestId restituisce un valore GUID (Globally Unique Identifier) per una richiesta. Un GUID è un numero univoco a 128 bit.
ms.assetid: c8df15cf-ab48-491f-ac18-1dad567bbc0b
ms.tgt_platform: multiple
title: 'Metodo IWbemCausalityAccess:: GetRequestId (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.GetRequestId
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 075be627b26d99a8b4f03c5a4a962b41f153c8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315204"
---
# <a name="iwbemcausalityaccessgetrequestid-method"></a>Metodo IWbemCausalityAccess:: GetRequestId

Il metodo **GetRequestiD** restituisce un valore GUID (Globally Unique Identifier) per una richiesta. Un GUID è un numero univoco a 128 bit.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRequestId(
  [out] REQUESTID *pId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PID* \[ out\]
</dt> <dd>

Valore GUID che identifica in modo univoco una richiesta. Ad esempio, 5b2fc63a-8af4-44cb-960c-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemint. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWbemCausalityAccess**](iwbemcausalityaccess.md)
</dt> </dl>

 

 




