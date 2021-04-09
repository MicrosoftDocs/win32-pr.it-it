---
title: Proprietà ActiveBasicDevice IsAudioSupported (PlayToDevice. h)
description: Ottiene un valore che indica se il dispositivo supporta l'audio.
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- API di streaming multimediale della proprietà IsAudioSupported
- API di streaming multimediale della proprietà IsAudioSupported, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, proprietà IsAudioSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66058da9dcdbac0ed1100b0ef21a4ed530d45a68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048739"
---
# <a name="activebasicdeviceisaudiosupported-property"></a><span data-ttu-id="b030b-106">Proprietà ActiveBasicDevice:: IsAudioSupported</span><span class="sxs-lookup"><span data-stu-id="b030b-106">ActiveBasicDevice::IsAudioSupported property</span></span>

<span data-ttu-id="b030b-107">Ottiene un valore che indica se il dispositivo supporta l'audio.</span><span class="sxs-lookup"><span data-stu-id="b030b-107">Gets a value that indicates if the device supports audio.</span></span>

<span data-ttu-id="b030b-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b030b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b030b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b030b-109">Syntax</span></span>


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="b030b-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b030b-110">Property value</span></span>

<span data-ttu-id="b030b-111">Puntatore a un **valore booleano** che indica se il dispositivo supporta l'audio.</span><span class="sxs-lookup"><span data-stu-id="b030b-111">A pointer to a **boolean** that indicates if the device supports audio.</span></span>

<span data-ttu-id="b030b-112">**true** se il dispositivo supporta l'audio; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b030b-112">**true** if the device supports audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b030b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b030b-113">Requirements</span></span>



| <span data-ttu-id="b030b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b030b-114">Requirement</span></span> | <span data-ttu-id="b030b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b030b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b030b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b030b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b030b-117">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b030b-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b030b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b030b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b030b-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b030b-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b030b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b030b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b030b-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b030b-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="b030b-122">IDL</span><span class="sxs-lookup"><span data-stu-id="b030b-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b030b-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b030b-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="b030b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b030b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b030b-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b030b-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b030b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b030b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b030b-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b030b-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

