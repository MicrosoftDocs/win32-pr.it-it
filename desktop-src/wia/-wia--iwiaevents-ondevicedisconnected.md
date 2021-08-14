---
description: Evento che si verifica quando un nuovo Windows hardware WIA (Image Acquisition) viene disconnesso.
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Evento Wia.OnDeviceDisconnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b9d61d196e3a9a7471b9a1fb1ab86c3ba918427ccc5dd5060ffaabdf28f80871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442157"
---
# <a name="wiaondevicedisconnected-event"></a>Evento Wia.OnDeviceDisconnected

Evento che si verifica quando un nuovo Windows hardware WIA (Image Acquisition) viene disconnesso.

## <a name="syntax"></a>Sintassi


```JScript
Wia.OnDeviceDisconnected(
  Id
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Id* 
</dt> <dd>

Stringa contenente l'ID del dispositivo connesso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

WiA invia una notifica allo script o all'applicazione ogni volta che un dispositivo hardware viene disconnesso dal computer. Implementare **la subroutine objWia** \_ **OnDeviceDisconnected()** per consentire allo script o all'applicazione di rispondere alla disconnessione del dispositivo.

Ad esempio, è possibile che uno script abiliti la raccolta [**Dispositivi**](-wia-iwia-devices.md) quando un dispositivo viene rimosso dal computer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




