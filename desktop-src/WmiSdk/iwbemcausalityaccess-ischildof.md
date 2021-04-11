---
description: Il metodo IsChildOf determina se una richiesta è un elemento figlio di una richiesta specificata (pId).
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'Metodo IWbemCausalityAccess:: IsChildOf (Wbemint. h)'
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
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232623"
---
# <a name="iwbemcausalityaccessischildof-method"></a>Metodo IWbemCausalityAccess:: IsChildOf

Il metodo **IsChildOf** determina se una richiesta è un elemento figlio di una richiesta specificata (PID). Una richiesta padre può avere più richieste figlio. Ogni richiesta viene identificata da un identificatore univoco globale (GUID) e può disporre di una richiesta padre oppure può essere una richiesta top. Un GUID è un numero univoco a 128 bit.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PID* \[ in\]
</dt> <dd>

Valore GUID che identifica in modo univoco una richiesta. Ad esempio, 5b2fc63a-8af4-44cb-960c-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce esito positivo se la richiesta specificata è un elemento figlio della richiesta che chiama il metodo **IsChildOf** .

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

 

 




