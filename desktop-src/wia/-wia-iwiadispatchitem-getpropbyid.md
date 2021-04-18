---
description: Il metodo GetPropById dell'oggetto Item usa l'ID di una proprietà Item per restituirne il valore.
ms.assetid: 00f7a91c-fd55-4016-a932-f710045a14b8
title: Item. GetPropById, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 54eb329d51005893b89a9fd28f160ff616e682df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312409"
---
# <a name="itemgetpropbyid-method"></a>Item. GetPropById, metodo

Il metodo **GetPropById** dell'oggetto [**Item**](-wia-item.md) usa l'ID di una proprietà Item per restituirne il valore.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Item.GetPropById(
  Id
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Tipo: **[WiaItemPropertyId](-wia-wiaitempropertyid.md)**

Specifica l'ID della proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **Variant**

Questo metodo restituisce il valore della proprietà specificata da *ID*.

## <a name="remarks"></a>Commenti

Utilizzare questo metodo per trovare il valore di una proprietà Item dal relativo ID. Per un elenco di ID di proprietà, vedere [definizioni di costanti della proprietà WIA](-wia-wia-property-constant-definitions.md). Per informazioni sulle proprietà stesse, vedere [costanti della proprietà WIA](-wia-wia-property-constants.md).

Per le applicazioni Microsoft Visual Basic, aggiungere un riferimento a "Windows Image Acquisition 1,01 Type Library". Le costanti seguenti definite in tale file sono valide solo per gli elementi radice (elementi del dispositivo):

``` syntax
const FirmwareVersion = 1026
const ConnectStatus = 1027
const DeviceTime = 1028
const PicturesTaken = 2050
const PicturesRemaining = 2051
const ExposureMode = 2052
const ExposureCompensation = 2053
const ExposureTime = 2054
const FNumber = 2055
const FlashMode = 2056
const FocusMode = 2057
const FocusManualDist = 2058
const ZoomPosition = 2059
const PanPosition = 2060
const TiltPostion = 2061
const TimerMode = 2062
const TimerValue = 2063
const PowerMode = 2064
const BatteryStatus = 2065
const Dimension = 2070
const HorizontalBedSize = 3074
const VerticalBedSize = 3075
const HorizontalSheetFeedSize = 3076
const VerticalSheetFeedSize = 3077
const SheetFeederRegistration = 3078
const HorizontalBedRegistration = 3079
const VerticalBedRegistraion = 3080
const PlatenColor = 3081
const PadColor = 3082
const FilterSelect = 3083
const DitherSelect = 3084
const DitherPatternData = 3085
const DocumentHandlingCapabilities = 3086
const DocumentHandlingStatus = 3087
const DocumentHandlingSelect = 3088
const DocumentHandlingCapacity = 3089
const HorizontalOpticalResolution = 3090
const VerticalOpticalResolution = 3091
const EndorserCharacters = 3092
const EndorserString = 3093
const ScanAheadPages = 3094
const MaxScanTime = 3095
const Pages = 3096
const PageSize = 3097
const PageWidth = 3098
const PageHeight = 3099
const Preview = 3100
const TransparencyAdapter = 3101
const TransparecnyAdapterSelect = 3102
```

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo del metodo **GetPropById** per recuperare un valore della proprietà.


```JScript
<SCRIPT LANGUAGE="VBScript">
const DeviceType = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    objRootItem=objDeviceInfo.Create()
    objSelectedItems=objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItem
    PropValue = objItem.GetPropById(DeviceType)
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4,90 o successiva)</dt> </dl> |



 

 




