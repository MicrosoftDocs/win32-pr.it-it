---
title: Metodo IMsTscAxEvents OnRequestLeaveFullScreen
description: Chiamato quando il client richiede di uscire dalla modalità a schermo intero e la proprietà IMsTscAdvancedSettings put \_ ContainerHandledFullScreen è stata impostata su un valore diverso da zero.
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnRequestLeaveFullScreen
- Metodo OnRequestLeaveFullScreen Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnRequestLeaveFullScreen
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
ms.openlocfilehash: e814d6153e32fdf4fa498a6630fc9ca2908510e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742095"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a>Metodo IMsTscAxEvents:: OnRequestLeaveFullScreen

Chiamato quando il client richiede di uscire dalla modalità a schermo intero e la proprietà [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) è stata impostata su un valore diverso da zero.

## <a name="syntax"></a>Sintassi


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

In modalità a schermo intero gestita dal contenitore il contenitore deve lasciare la modalità standard a schermo intero in risposta a questo evento.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





