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
# <a name="itemgetpropbyid-method"></a><span data-ttu-id="85862-103">Item. GetPropById, metodo</span><span class="sxs-lookup"><span data-stu-id="85862-103">Item.GetPropById method</span></span>

<span data-ttu-id="85862-104">Il metodo **GetPropById** dell'oggetto [**Item**](-wia-item.md) usa l'ID di una proprietà Item per restituirne il valore.</span><span class="sxs-lookup"><span data-stu-id="85862-104">The **GetPropById** method of the [**Item**](-wia-item.md) object uses the ID of an item property to return its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="85862-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85862-105">Syntax</span></span>


```JScript
retVal = Item.GetPropById(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="85862-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85862-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85862-107">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85862-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85862-108">Tipo: **[WiaItemPropertyId](-wia-wiaitempropertyid.md)**</span><span class="sxs-lookup"><span data-stu-id="85862-108">Type: **[WiaItemPropertyId](-wia-wiaitempropertyid.md)**</span></span>

<span data-ttu-id="85862-109">Specifica l'ID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="85862-109">Specifies the ID of the property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85862-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85862-110">Return value</span></span>

<span data-ttu-id="85862-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="85862-111">Type: **VARIANT**</span></span>

<span data-ttu-id="85862-112">Questo metodo restituisce il valore della proprietà specificata da *ID*.</span><span class="sxs-lookup"><span data-stu-id="85862-112">This method returns the value of the property specified by *Id*.</span></span>

## <a name="remarks"></a><span data-ttu-id="85862-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="85862-113">Remarks</span></span>

<span data-ttu-id="85862-114">Utilizzare questo metodo per trovare il valore di una proprietà Item dal relativo ID.</span><span class="sxs-lookup"><span data-stu-id="85862-114">Use this method to find the value of an item property from its ID.</span></span> <span data-ttu-id="85862-115">Per un elenco di ID di proprietà, vedere [definizioni di costanti della proprietà WIA](-wia-wia-property-constant-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="85862-115">For a list of property IDs, see [WIA Property Constant Definitions](-wia-wia-property-constant-definitions.md).</span></span> <span data-ttu-id="85862-116">Per informazioni sulle proprietà stesse, vedere [costanti della proprietà WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="85862-116">For information about the properties themselves, see [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

<span data-ttu-id="85862-117">Per le applicazioni Microsoft Visual Basic, aggiungere un riferimento a "Windows Image Acquisition 1,01 Type Library".</span><span class="sxs-lookup"><span data-stu-id="85862-117">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span> <span data-ttu-id="85862-118">Le costanti seguenti definite in tale file sono valide solo per gli elementi radice (elementi del dispositivo):</span><span class="sxs-lookup"><span data-stu-id="85862-118">The following constants defined in that file are valid only for root items (device items):</span></span>

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

## <a name="examples"></a><span data-ttu-id="85862-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="85862-119">Examples</span></span>

<span data-ttu-id="85862-120">Nell'esempio seguente viene illustrato l'utilizzo del metodo **GetPropById** per recuperare un valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="85862-120">The following example demonstrates the use of the **GetPropById** method to retrieve a property value.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="85862-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85862-121">Requirements</span></span>



| <span data-ttu-id="85862-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="85862-122">Requirement</span></span> | <span data-ttu-id="85862-123">Valore</span><span class="sxs-lookup"><span data-stu-id="85862-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85862-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85862-124">Minimum supported client</span></span><br/> | <span data-ttu-id="85862-125">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="85862-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85862-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85862-126">Minimum supported server</span></span><br/> | <span data-ttu-id="85862-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="85862-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="85862-128">DLL</span><span class="sxs-lookup"><span data-stu-id="85862-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85862-129"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="85862-129"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




