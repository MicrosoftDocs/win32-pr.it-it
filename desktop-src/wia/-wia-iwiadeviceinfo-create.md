---
description: Il metodo create dell'oggetto DeviceInfo esegue una connessione al dispositivo Windows Image Acquisition (WIA) specificato dall'oggetto DeviceInfo e restituisce un oggetto Item che rappresenta il dispositivo.
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: Metodo DeviceInfo. Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1efc36ea8794de4b64c9af616320b09d547f6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308244"
---
# <a name="deviceinfocreate-method"></a>Metodo DeviceInfo. Create

Il metodo **create** dell'oggetto [**deviceInfo**](-wia-deviceinfo.md) esegue una connessione al dispositivo Windows Image Acquisition (WIA) specificato dall'oggetto **deviceInfo** e restituisce un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo.

## <a name="syntax"></a>Sintassi


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **IWiaDispatchItem**

Questo metodo restituisce l'oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo creato.

## <a name="remarks"></a>Commenti

Usare il metodo **create** per creare una connessione a un dispositivo hardware WIA dopo l'enumerazione della raccolta [**Devices**](-wia-iwia-devices.md) . Il metodo restituisce un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo (un elemento radice).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo del metodo **create** .


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




