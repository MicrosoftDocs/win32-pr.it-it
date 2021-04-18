---
description: Raccolta di oggetti DeviceInfo che rappresenta tutti i dispositivi installati nel computer.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: Proprietà WIA. Devices
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Devices
- SafeWia.Devices
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d03aa0b7e73d5dfbc6449816f3b64147e51db882
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308247"
---
# <a name="wiadevices-property"></a>Proprietà WIA. Devices

Raccolta di oggetti [**deviceInfo**](-wia-deviceinfo.md) che rappresenta tutti i dispositivi installati nel computer. Di sola lettura.

> [!Note]  
> Questa raccolta è in base 0.

 

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a>Valore proprietà

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'uso della raccolta **Devices** per enumerare i dispositivi in un sistema.


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ! Do something with the DeviceInfo object
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




