---
title: Metodo IMsTscAxEvents OnRequestGoFullScreen
description: Chiamato quando il client richiede di passare alla modalità a schermo intero e \_ viene chiamato il metodo IMsTscAdvancedSettings put ContainerHandledFullScreen per impostare la proprietà ContainerHandledFullScreen su un valore diverso da zero.
ms.assetid: f61520dc-a72a-4205-8761-92aaf08b5f90
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnRequestGoFullScreen
- Metodo OnRequestGoFullScreen Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnRequestGoFullScreen
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
ms.openlocfilehash: c865cd27b447743f781b8563956e7fb2d7f5d703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400733"
---
# <a name="imstscaxeventsonrequestgofullscreen-method"></a>Metodo IMsTscAxEvents:: OnRequestGoFullScreen

Chiamato quando il client richiede di passare alla modalità a schermo intero e viene chiamato il metodo [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) per impostare la proprietà **ContainerHandledFullScreen** su un valore diverso da zero.

## <a name="syntax"></a>Sintassi


```C++
void OnRequestGoFullScreen();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

In modalità a schermo intero gestita dal contenitore il contenitore deve immettere la modalità standard a schermo intero in risposta a questo evento.

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

 

 





