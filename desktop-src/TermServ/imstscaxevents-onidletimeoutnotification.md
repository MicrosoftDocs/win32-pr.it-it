---
title: Metodo IMsTscAxEvents OnIdleTimeoutNotification
description: Chiamato quando l'utente non dispone di input del mouse o della tastiera durante il periodo di tempo impostato dal metodo IMsRdpClientAdvancedSettings put \_ MinutesToIdleTimeout.
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnIdleTimeoutNotification
- Metodo OnIdleTimeoutNotification Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnIdleTimeoutNotification
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
ms.openlocfilehash: 3e305b0ed22e733053e33451aa35d3b8f8d6c138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301878"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a>Metodo IMsTscAxEvents:: OnIdleTimeoutNotification

Chiamato quando l'utente non dispone di input del mouse o della tastiera durante il periodo di tempo impostato dal metodo [**IMsRdpClientAdvancedSettings::p UT \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .

## <a name="syntax"></a>Sintassi


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il valore della proprietà [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) è impostato su zero e il sistema non monitora i timeout di inattività. Questo evento si verifica solo se la proprietà è impostata su un valore diverso da zero.

Il valore di [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) viene reimpostato automaticamente ogni volta che si verifica l'evento.

Le applicazioni possono utilizzare [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in situazioni in cui è utile disconnettere un utente. ad esempio, in un chiosco multimediale o in un altro scenario di terminale pubblico.

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

 

 





