---
description: Raccolta di oggetti DeviceInfo che rappresenta tutti i dispositivi installati nel computer.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: Proprietà Wia.Devices
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
ms.openlocfilehash: b4d98bfe1552156071efde0b46899ad058e75aec
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841313"
---
# <a name="wiadevices-property"></a>Proprietà Wia.Devices

Raccolta di [**oggetti DeviceInfo**](-wia-deviceinfo.md) che rappresenta tutti i dispositivi installati nel computer. Di sola lettura.

> [!Note]  
> Questa raccolta è basata su 0.

 

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a>Valore proprietà

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso della raccolta **Devices** per enumerare i dispositivi in un sistema.


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
| Client minimo supportato<br/> | Solo app desktop di Windows 2000 Professional e Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




