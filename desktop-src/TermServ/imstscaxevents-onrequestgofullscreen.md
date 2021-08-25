---
title: Metodo IMsTscAxEvents OnRequestGoFullScreen
description: Chiamato quando il client richiede di passare alla modalità schermo intero e il metodo IMsTscAdvancedSettings put ContainerHandledFullScreen viene chiamato per impostare la proprietà ContainerHandledFullScreen su un valore diverso da \_ zero.
ms.assetid: f61520dc-a72a-4205-8761-92aaf08b5f90
ms.tgt_platform: multiple
keywords:
- Metodo OnRequestGoFullScreen Servizi Desktop remoto
- Metodo OnRequestGoFullScreen Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnRequestGoFullScreen
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestGoFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6d689469f635694357890c620866fff5783680f8e9e8d11a1a05c78f6e1e322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770681"
---
# <a name="imstscaxeventsonrequestgofullscreen-method"></a>Metodo IMsTscAxEvents::OnRequestGoFullScreen

Chiamato quando il client richiede di passare alla modalità schermo intero e il metodo [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) viene chiamato per impostare la proprietà **ContainerHandledFullScreen** su un valore diverso da zero.

## <a name="syntax"></a>Sintassi


```C++
void OnRequestGoFullScreen();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

In modalità schermo intero gestita dal contenitore, il contenitore deve accedere alla modalità schermo intero standard in risposta a questo evento.

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

 

 





