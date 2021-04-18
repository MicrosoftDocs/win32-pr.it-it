---
description: Il metodo SetQOSApplicationID imposta l'identificatore QOS per l'applicazione.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'Metodo ITQOSApplicationID:: SetQOSApplicationID (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7893c8038fd7a47fc1978a20e5aba5cc8293d9a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333662"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a>Metodo ITQOSApplicationID:: SetQOSApplicationID

\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **SetQOSApplicationID** imposta l'identificatore QoS per l'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pApplicationID* \[ in\]
</dt> <dd>

Identificatore univoco del processo dell'applicazione.

</dd> <dt>

*pApplicationGUID* \[ in\]
</dt> <dd>

GUID dell'applicazione.

</dd> <dt>

*pSubIDs* \[ in\]
</dt> <dd>

Sub-IDs associato alla chiamata corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITQOSApplicationID**](itqosapplicationid.md)
</dt> </dl>

 

 




