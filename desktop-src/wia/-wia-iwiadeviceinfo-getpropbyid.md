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
# <a name="deviceinfogetpropbyid-method"></a><span data-ttu-id="f8aa8-103">DeviceInfo. GetPropById, metodo</span><span class="sxs-lookup"><span data-stu-id="f8aa8-103">DeviceInfo.GetPropById method</span></span>

<span data-ttu-id="f8aa8-104">Il metodo **GetPropById** dell'oggetto [**DEVICEINFO**](-wia-deviceinfo.md) usa l'ID di una proprietà del dispositivo per restituirne il valore.</span><span class="sxs-lookup"><span data-stu-id="f8aa8-104">The **GetPropById** method of the [**DeviceInfo**](-wia-deviceinfo.md) object uses a device property's ID to return its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8aa8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8aa8-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="f8aa8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8aa8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8aa8-107">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8aa8-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8aa8-108">Tipo: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**</span><span class="sxs-lookup"><span data-stu-id="f8aa8-108">Type: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**</span></span>

<span data-ttu-id="f8aa8-109">Specifica l'ID della proprietà.</span><span class="sxs-lookup"><span data-stu-id="f8aa8-109">Specifies the ID of the property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8aa8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8aa8-110">Return value</span></span>

<span data-ttu-id="f8aa8-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="f8aa8-111">Type: **VARIANT**</span></span>

<span data-ttu-id="f8aa8-112">Questo metodo restituisce il valore della proprietà specificata da *ID*.</span><span class="sxs-lookup"><span data-stu-id="f8aa8-112">This method returns the value of the property specified by *Id*.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8aa8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8aa8-113">Remarks</span></span>

<span data-ttu-id="f8aa8-114">Usare questo metodo per trovare il valore di una proprietà del dispositivo dal relativo ID.</span><span class="sxs-lookup"><span data-stu-id="f8aa8-114">Use this method to find the value of a device property from its ID.</span></span> <span data-ttu-id="f8aa8-115">Per un elenco di ID di proprietà, vedere [definizioni di costanti della proprietà WIA](-wia-wia-property-constant-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="f8aa8-115">For a list of property IDs, see [WIA Property Constant Definitions](-wia-wia-property-constant-definitions.md).</span></span> <span data-ttu-id="f8aa8-116">Per informazioni sulle proprietà WIA (Windows Image Acquisition), vedere [costanti della proprietà WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f8aa8-116">For information about Windows Image Acquisition (WIA) properties themselves, see [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

<span data-ttu-id="f8aa8-117">Per le applicazioni Microsoft Visual Basic, aggiungere un riferimento a "Windows Image Acquisition 1,01 Type Library".</span><span class="sxs-lookup"><span data-stu-id="f8aa8-117">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span> <span data-ttu-id="f8aa8-118">Le seguenti costanti definite in tale file sono valide per questo metodo:</span><span class="sxs-lookup"><span data-stu-id="f8aa8-118">This following constants defined in that file are valid for this method:</span></span>

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

## <a name="examples"></a><span data-ttu-id="f8aa8-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="f8aa8-119">Examples</span></span>

<span data-ttu-id="f8aa8-120">Nell'esempio seguente viene illustrato l'utilizzo del metodo **GetPropById** per recuperare un valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="f8aa8-120">The following example demonstrates the use of the **GetPropById** method to retrieve a property value.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f8aa8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8aa8-121">Requirements</span></span>



| <span data-ttu-id="f8aa8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8aa8-122">Requirement</span></span> | <span data-ttu-id="f8aa8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f8aa8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8aa8-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8aa8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f8aa8-125">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f8aa8-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8aa8-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8aa8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f8aa8-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8aa8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f8aa8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f8aa8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8aa8-129"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="f8aa8-129"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




