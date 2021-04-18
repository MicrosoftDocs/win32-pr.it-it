---
description: Il metodo GetPropById dell'oggetto DeviceInfo usa l'ID di una proprietà del dispositivo per restituirne il valore.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: DeviceInfo. GetPropById, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: adbc8b6a29f97066c8dc5b2e45b7ddc5834f2b60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312419"
---
# <a name="deviceinfogetpropbyid-method"></a>DeviceInfo. GetPropById, metodo

Il metodo **GetPropById** dell'oggetto [**DEVICEINFO**](-wia-deviceinfo.md) usa l'ID di una proprietà del dispositivo per restituirne il valore.

## <a name="syntax"></a>Sintassi


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Tipo: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**

Specifica l'ID della proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **Variant**

Questo metodo restituisce il valore della proprietà specificata da *ID*.

## <a name="remarks"></a>Commenti

Usare questo metodo per trovare il valore di una proprietà del dispositivo dal relativo ID. Per un elenco di ID di proprietà, vedere [definizioni di costanti della proprietà WIA](-wia-wia-property-constant-definitions.md). Per informazioni sulle proprietà WIA (Windows Image Acquisition), vedere [costanti della proprietà WIA](-wia-wia-property-constants.md).

Per le applicazioni Microsoft Visual Basic, aggiungere un riferimento a "Windows Image Acquisition 1,01 Type Library". Le seguenti costanti definite in tale file sono valide per questo metodo:

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo del metodo **GetPropById** per recuperare un valore della proprietà.


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




