---
description: Il metodo IsChildOf determina se una richiesta è figlio di una richiesta specificata (pId).
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: Metodo IWbemCausalityAccess::IsChildOf (Wbemint.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 509508d5e1a273dc681cf3c9f645ead1037408d6ecfe5ed666186ba6e2a2c0d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318293"
---
# <a name="iwbemcausalityaccessischildof-method"></a>Metodo IWbemCausalityAccess::IsChildOf

Il **metodo IsChildOf** determina se una richiesta è figlio di una richiesta specificata (pId). Una richiesta padre può avere più richieste figlio. Ogni richiesta è identificata da un GUID (Globally Unique Identifier) e può avere una richiesta padre o può essere una richiesta principale. Un GUID è un numero univoco a 128 bit.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pId* \[ Pollici\]
</dt> <dd>

Valore GUID che identifica in modo univoco una richiesta. Ad esempio, 5b2fc63a-8af4-44cb-960c-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce esito positivo se la richiesta specificata è un elemento figlio della richiesta che chiama il **metodo IsChildOf.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemint.h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWbemCausalityAccess**](iwbemcausalityaccess.md)
</dt> </dl>

 

 




