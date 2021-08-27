---
title: Metodo IMsTscAxEvents OnIdleTimeoutNotification
description: Chiamato quando l'utente non ha immesso mouse o tastiera durante il periodo di tempo impostato dal metodo IMsRdpClientAdvancedSettings put \_ MinutesToIdleTimeout.
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- Metodo OnIdleTimeoutNotification Servizi Desktop remoto
- Metodo OnIdleTimeoutNotification Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnIdleTimeoutNotification
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356414d03a6b102f37f93205e0dbb8c3261cffbbb5b71a58cdb3f80acda09212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125121"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a>Metodo IMsTscAxEvents::OnIdleTimeoutNotification

Chiamato quando l'utente non ha immesso mouse o tastiera durante il periodo di tempo impostato dal metodo [**IMsRdpClientAdvancedSettings::p ut \_ MinutesToIdleTimeout.**](imsrdpclientadvancedsettings-minutestoidletimeout.md)

## <a name="syntax"></a>Sintassi


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il valore della [**proprietà MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) è impostato su zero e il sistema non monitora i timeout di inattività. Questo evento si verifica solo se la proprietà è impostata su un valore diverso da zero.

Il valore [**minutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) viene reimpostato automaticamente ogni volta che si verifica l'evento.

Le applicazioni possono [**usare MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in situazioni in cui è utile disconnettere un utente. ad esempio in uno scenario in modalità tutto schermo o in un altro terminale pubblico.

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

 

 





