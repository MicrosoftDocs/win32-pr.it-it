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
# <a name="deviceinfocreate-method"></a><span data-ttu-id="242c4-103">Metodo DeviceInfo. Create</span><span class="sxs-lookup"><span data-stu-id="242c4-103">DeviceInfo.Create method</span></span>

<span data-ttu-id="242c4-104">Il metodo **create** dell'oggetto [**deviceInfo**](-wia-deviceinfo.md) esegue una connessione al dispositivo Windows Image Acquisition (WIA) specificato dall'oggetto **deviceInfo** e restituisce un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="242c4-104">The **Create** method of the [**DeviceInfo**](-wia-deviceinfo.md) object makes a connection to the Windows Image Acquisition (WIA) device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="242c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="242c4-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a><span data-ttu-id="242c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="242c4-106">Parameters</span></span>

<span data-ttu-id="242c4-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="242c4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="242c4-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="242c4-108">Return value</span></span>

<span data-ttu-id="242c4-109">Tipo: **IWiaDispatchItem**</span><span class="sxs-lookup"><span data-stu-id="242c4-109">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="242c4-110">Questo metodo restituisce l'oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo creato.</span><span class="sxs-lookup"><span data-stu-id="242c4-110">This method returns the [**Item**](-wia-item.md) object that represents the device that is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="242c4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="242c4-111">Remarks</span></span>

<span data-ttu-id="242c4-112">Usare il metodo **create** per creare una connessione a un dispositivo hardware WIA dopo l'enumerazione della raccolta [**Devices**](-wia-iwia-devices.md) .</span><span class="sxs-lookup"><span data-stu-id="242c4-112">Use the **Create** method to create a connection to a WIA hardware device after enumerating the [**Devices**](-wia-iwia-devices.md) collection.</span></span> <span data-ttu-id="242c4-113">Il metodo restituisce un oggetto [**Item**](-wia-item.md) che rappresenta il dispositivo (un elemento radice).</span><span class="sxs-lookup"><span data-stu-id="242c4-113">The method returns an [**Item**](-wia-item.md) object that represents the device (a root item).</span></span>

## <a name="examples"></a><span data-ttu-id="242c4-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="242c4-114">Examples</span></span>

<span data-ttu-id="242c4-115">Nell'esempio seguente viene illustrato l'utilizzo del metodo **create** .</span><span class="sxs-lookup"><span data-stu-id="242c4-115">The following example demonstrates the use of the **Create** method.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="242c4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="242c4-116">Requirements</span></span>



| <span data-ttu-id="242c4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="242c4-117">Requirement</span></span> | <span data-ttu-id="242c4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="242c4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="242c4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="242c4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="242c4-120">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="242c4-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="242c4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="242c4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="242c4-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="242c4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="242c4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="242c4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="242c4-124"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="242c4-124"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




