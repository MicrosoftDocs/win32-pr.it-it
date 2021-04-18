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
# <a name="wiadevices-property"></a><span data-ttu-id="a44fb-103">Proprietà WIA. Devices</span><span class="sxs-lookup"><span data-stu-id="a44fb-103">Wia.Devices property</span></span>

<span data-ttu-id="a44fb-104">Raccolta di oggetti [**deviceInfo**](-wia-deviceinfo.md) che rappresenta tutti i dispositivi installati nel computer.</span><span class="sxs-lookup"><span data-stu-id="a44fb-104">Collection of [**DeviceInfo**](-wia-deviceinfo.md) objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="a44fb-105">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a44fb-105">Read-only.</span></span>

> [!Note]  
> <span data-ttu-id="a44fb-106">Questa raccolta è in base 0.</span><span class="sxs-lookup"><span data-stu-id="a44fb-106">This collection is 0-based.</span></span>

 

<span data-ttu-id="a44fb-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a44fb-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a44fb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a44fb-108">Syntax</span></span>


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a><span data-ttu-id="a44fb-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a44fb-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="a44fb-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="a44fb-110">Examples</span></span>

<span data-ttu-id="a44fb-111">Nell'esempio seguente viene illustrato l'uso della raccolta **Devices** per enumerare i dispositivi in un sistema.</span><span class="sxs-lookup"><span data-stu-id="a44fb-111">The following example illustrates the use of the **Devices** collection to enumerate the devices on a system.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a44fb-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a44fb-112">Requirements</span></span>



| <span data-ttu-id="a44fb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a44fb-113">Requirement</span></span> | <span data-ttu-id="a44fb-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a44fb-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a44fb-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a44fb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a44fb-116">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a44fb-116">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a44fb-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a44fb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a44fb-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a44fb-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a44fb-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a44fb-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a44fb-120"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="a44fb-120"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




