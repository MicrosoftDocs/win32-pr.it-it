---
title: Proprietà ActiveBasicDevice IsMuteSupported (PlayToDevice. h)
description: Ottiene un valore che indica se il dispositivo supporta la soppressione dell'audio.
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- API di streaming multimediale della proprietà IsMuteSupported
- API di streaming multimediale della proprietà IsMuteSupported, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, proprietà IsMuteSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcec2e4520bd3b15b715c01e4369da87887355e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477369"
---
# <a name="activebasicdeviceismutesupported-property"></a><span data-ttu-id="a6b5d-106">Proprietà ActiveBasicDevice:: IsMuteSupported</span><span class="sxs-lookup"><span data-stu-id="a6b5d-106">ActiveBasicDevice::IsMuteSupported property</span></span>

<span data-ttu-id="a6b5d-107">Ottiene un valore che indica se il dispositivo supporta la soppressione dell'audio.</span><span class="sxs-lookup"><span data-stu-id="a6b5d-107">Gets a value that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="a6b5d-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a6b5d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6b5d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6b5d-109">Syntax</span></span>


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="a6b5d-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a6b5d-110">Property value</span></span>

<span data-ttu-id="a6b5d-111">Puntatore a un **valore booleano** che indica se il dispositivo supporta la soppressione dell'audio.</span><span class="sxs-lookup"><span data-stu-id="a6b5d-111">A pointer to a **boolean** that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="a6b5d-112">**true** se il dispositivo supporta la soppressione dell'audio; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a6b5d-112">**true** if the device supports muting the audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6b5d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6b5d-113">Requirements</span></span>



| <span data-ttu-id="a6b5d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6b5d-114">Requirement</span></span> | <span data-ttu-id="a6b5d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a6b5d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b5d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6b5d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a6b5d-117">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a6b5d-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a6b5d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6b5d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a6b5d-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6b5d-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a6b5d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6b5d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6b5d-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6b5d-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6b5d-122">IDL</span><span class="sxs-lookup"><span data-stu-id="a6b5d-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6b5d-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6b5d-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="a6b5d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a6b5d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6b5d-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6b5d-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6b5d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6b5d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="a6b5d-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a6b5d-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

