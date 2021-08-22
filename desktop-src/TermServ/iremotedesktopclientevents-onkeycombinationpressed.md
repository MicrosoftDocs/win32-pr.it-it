---
title: Metodo IRemoteDesktopClientEvents OnKeyCombinationPressed
description: Chiamato quando vengono premute combinazioni di tasti speciali nella sessione remota.
ms.assetid: 0A4EAD6C-5DA9-4ED3-BA79-92AE5AE81C9F
ms.tgt_platform: multiple
keywords:
- Metodo OnKeyCombinationPressed Servizi Desktop remoto
- Metodo OnKeyCombinationPressed Servizi Desktop remoto , interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto , metodo OnKeyCombinationPressed
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnKeyCombinationPressed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e175bc0d65126c11cbcb97d0b73accd48ff92b02e38cca6e3ac35ebcce1ae961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515101"
---
# <a name="iremotedesktopclienteventsonkeycombinationpressed-method"></a>Metodo IRemoteDesktopClientEvents::OnKeyCombinationPressed

Chiamato quando vengono premute combinazioni di tasti speciali nella sessione remota.

## <a name="syntax"></a>Sintassi


```C++
void OnKeyCombinationPressed(
  [in] long keyCombination
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*keyCombination* \[ Pollici\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                           |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                 |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





