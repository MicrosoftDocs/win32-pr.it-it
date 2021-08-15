---
description: Evento che si verifica quando un nuovo Windows hardware WIA (Image Acquisition) è connesso.
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Evento Wia.OnDeviceConnected
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
ms.openlocfilehash: d878cc663cc9f7ea1422e2dc2cad10e652296a48ef597cf699fe5eb3af99e49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209548"
---
# <a name="wiaondeviceconnected-event"></a>Evento Wia.OnDeviceConnected

Evento che si verifica quando un nuovo Windows hardware WIA (Image Acquisition) è connesso.

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

Stringa contenente l'ID del dispositivo connesso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="remarks"></a>Commenti

WiA invia una notifica allo script o all'applicazione ogni volta che un nuovo dispositivo hardware è connesso al computer. Implementare **la subroutine objWia** \_ **OnDeviceConnected()** per consentire allo script o all'applicazione di rispondere alla connessione del dispositivo.

Ad esempio, è possibile che uno script abiliti la raccolta [**Dispositivi**](-wia-iwia-devices.md) quando viene installato un nuovo dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




