---
description: Il metodo GetPropById dell'oggetto DeviceInfo usa l'ID di una proprietà del dispositivo per restituirne il valore.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: Metodo DeviceInfo.GetPropById
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
ms.openlocfilehash: c996989661703c4a9c7416cd63904c376fdb7fcca3071d4558551bdd78470d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208787"
---
# <a name="deviceinfogetpropbyid-method"></a>Metodo DeviceInfo.GetPropById

Il **metodo GetPropById** dell'oggetto [**DeviceInfo**](-wia-deviceinfo.md) usa l'ID di una proprietà del dispositivo per restituirne il valore.

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

Tipo: **VARIANT**

Questo metodo restituisce il valore della proprietà specificata da *Id*.

## <a name="remarks"></a>Commenti

Usare questo metodo per trovare il valore di una proprietà del dispositivo dal relativo ID. Per un elenco di ID di proprietà, vedere [Definizioni delle costanti delle proprietà WIA.](-wia-wia-property-constant-definitions.md) Per informazioni sulle Windows di acquisizione di immagini (WIA) stesse, vedere Costanti delle [proprietà WIA.](-wia-wia-property-constants.md)

Per le Visual Basic Microsoft, aggiungere un riferimento a "Windows image acquisition 1.01 Type Library". Le costanti seguenti definite nel file sono valide per questo metodo:

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

L'esempio seguente illustra l'uso **del metodo GetPropById** per recuperare il valore di una proprietà.


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




