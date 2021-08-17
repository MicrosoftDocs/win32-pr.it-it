---
title: Metodo IMsTscAxEvents OnUserNameAcquired
description: Chiamato quando il nome utente è stato acquisito dal controllo .
ms.assetid: 0653B28B-2D46-429F-8A36-5656786C0B26
ms.tgt_platform: multiple
keywords:
- Metodo OnUserNameAcquired Servizi Desktop remoto
- Metodo OnUserNameAcquired Servizi Desktop remoto , interfaccia IMsTscAxEvents
- Metodo OnUserNameAcquired dell'Servizi Desktop remoto IMsTscAxEvents
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnUserNameAcquired
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f05b63d59ebe0610b28198d264caf0fb7d3cd87f9ee664f804dc38eb2996abd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757154"
---
# <a name="imstscaxeventsonusernameacquired-method"></a>Metodo IMsTscAxEvents::OnUserNameAcquired

Chiamato quando il nome utente è stato acquisito dal controllo .

## <a name="syntax"></a>Sintassi


```C++
void OnUserNameAcquired(
   BSTR bstrUserName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrUserName* 
</dt> <dd>

Nome utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





