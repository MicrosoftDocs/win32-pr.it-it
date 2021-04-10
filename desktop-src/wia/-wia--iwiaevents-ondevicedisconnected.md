---
description: Evento che si verifica quando un nuovo dispositivo hardware di acquisizione immagini Windows (WIA) viene disconnesso.
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Evento WIA. OnDeviceDisconnected
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
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231564"
---
# <a name="wiaondevicedisconnected-event"></a>Evento WIA. OnDeviceDisconnected

Evento che si verifica quando un nuovo dispositivo hardware di acquisizione immagini Windows (WIA) viene disconnesso.

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

Stringa che contiene l'ID del dispositivo connesso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

WIA notifica lo script o l'applicazione ogni volta che un dispositivo hardware è disconnesso dal computer. Implementare la subroutine **objWia** \_ **OnDeviceDisconnected ()** per consentire all'applicazione o allo script di rispondere alla disconnessione del dispositivo.

Ad esempio, potrebbe essere necessario uno script per aggiornare la raccolta di [**dispositivi**](-wia-iwia-devices.md) quando un dispositivo viene rimosso dal computer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




