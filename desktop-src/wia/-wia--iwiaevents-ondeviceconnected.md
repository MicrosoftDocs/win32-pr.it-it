---
description: Evento che si verifica quando viene connesso un nuovo dispositivo hardware Windows Image Acquisition (WIA).
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Evento WIA. OnDeviceConnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231565"
---
# <a name="wiaondeviceconnected-event"></a>Evento WIA. OnDeviceConnected

Evento che si verifica quando viene connesso un nuovo dispositivo hardware Windows Image Acquisition (WIA).

## <a name="syntax"></a>Sintassi


```JScript
Wia.OnDeviceConnected(
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

WIA notifica lo script o l'applicazione ogni volta che un nuovo dispositivo hardware è connesso al computer. Implementare la subroutine **objWia** \_ **OnDeviceConnected ()** per consentire all'applicazione o allo script di rispondere alla connessione del dispositivo.

Ad esempio, potrebbe essere necessario uno script per aggiornare la raccolta di [**dispositivi**](-wia-iwia-devices.md) quando viene installato un nuovo dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




