---
title: Metodo IRemoteDesktopClientEvents OnTouchPointerCursorMoved
description: Chiamato quando il cursore del puntatore tocco è stato spostato e la proprietà EventsEnabled è impostata su true.
ms.assetid: 55A6AC99-0723-4215-9428-D2DAAC77A74A
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnTouchPointerCursorMoved
- Metodo OnTouchPointerCursorMoved Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, metodo OnTouchPointerCursorMoved
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnTouchPointerCursorMoved
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae347e19942bf0c82112e5cec6a3fb4fe131349f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301624"
---
# <a name="iremotedesktopclienteventsontouchpointercursormoved-method"></a>Metodo IRemoteDesktopClientEvents:: OnTouchPointerCursorMoved

Chiamato quando il cursore del puntatore tocco è stato spostato e la proprietà [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) è impostata su true.

## <a name="syntax"></a>Sintassi


```C++
void OnTouchPointerCursorMoved(
  [in] long x,
  [in] long y
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* \[ in\]
</dt> <dd></dd> <dt>

*y* \[ in\]
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

 

