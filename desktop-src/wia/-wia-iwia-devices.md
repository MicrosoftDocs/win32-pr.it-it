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
# <a name="wiadevices-property"></a><span data-ttu-id="2fd38-103">Proprietà Wia.Devices</span><span class="sxs-lookup"><span data-stu-id="2fd38-103">Wia.Devices property</span></span>

<span data-ttu-id="2fd38-104">Raccolta di [**oggetti DeviceInfo**](-wia-deviceinfo.md) che rappresenta tutti i dispositivi installati nel computer.</span><span class="sxs-lookup"><span data-stu-id="2fd38-104">Collection of [**DeviceInfo**](-wia-deviceinfo.md) objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="2fd38-105">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2fd38-105">Read-only.</span></span>

> [!Note]  
> <span data-ttu-id="2fd38-106">Questa raccolta è basata su 0.</span><span class="sxs-lookup"><span data-stu-id="2fd38-106">This collection is 0-based.</span></span>

 

<span data-ttu-id="2fd38-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2fd38-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd38-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fd38-108">Syntax</span></span>


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a><span data-ttu-id="2fd38-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2fd38-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="2fd38-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="2fd38-110">Examples</span></span>

<span data-ttu-id="2fd38-111">L'esempio seguente illustra l'uso della raccolta **Devices** per enumerare i dispositivi in un sistema.</span><span class="sxs-lookup"><span data-stu-id="2fd38-111">The following example illustrates the use of the **Devices** collection to enumerate the devices on a system.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2fd38-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fd38-112">Requirements</span></span>



| <span data-ttu-id="2fd38-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fd38-113">Requirement</span></span> | <span data-ttu-id="2fd38-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2fd38-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd38-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fd38-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd38-116">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2fd38-116">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2fd38-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fd38-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd38-118">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2fd38-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2fd38-119">DLL</span><span class="sxs-lookup"><span data-stu-id="2fd38-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fd38-120"><dt>Wiascr.dll (versione 4.90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="2fd38-120"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




