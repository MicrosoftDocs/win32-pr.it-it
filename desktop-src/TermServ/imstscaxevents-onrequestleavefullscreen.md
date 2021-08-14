---
title: Metodo IMsTscAxEvents OnRequestLeaveFullScreen
description: Chiamato quando il client richiede di uscire dalla modalità schermo intero e la proprietà IMsTscAdvancedSettings put ContainerHandledFullScreen è stata impostata su un valore \_ diverso da zero.
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- Metodo OnRequestLeaveFullScreen Servizi Desktop remoto
- Metodo OnRequestLeaveFullScreen Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnRequestLeaveFullScreen
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestLeaveFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74f82cd71942f559039a175fdfff9319cae5ea35a73d4698760be4642a23c448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757341"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a>Metodo IMsTscAxEvents::OnRequestLeaveFullScreen

Chiamato quando il client richiede di uscire dalla modalità schermo intero e la proprietà [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) è stata impostata su un valore diverso da zero.

## <a name="syntax"></a>Sintassi


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

In modalità schermo intero gestita dal contenitore, il contenitore deve uscire dalla modalità schermo intero standard in risposta a questo evento.

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





