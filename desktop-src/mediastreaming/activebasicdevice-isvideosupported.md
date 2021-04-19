---
title: Proprietà ActiveBasicDevice IsVideoSupported (PlayToDevice. h)
description: Ottiene un valore che indica se il dispositivo supporta il video.
ms.assetid: E8D33A04-748D-42F8-878F-35D973A6B559
keywords:
- API di streaming multimediale della proprietà IsVideoSupported
- API di streaming multimediale della proprietà IsVideoSupported, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, proprietà IsVideoSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsVideoSupported
- ActiveBasicDevice.get_IsVideoSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be369b34355b199cd47518065724242b9a422e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302588"
---
# <a name="activebasicdeviceisvideosupported-property"></a><span data-ttu-id="baac2-106">Proprietà ActiveBasicDevice:: IsVideoSupported</span><span class="sxs-lookup"><span data-stu-id="baac2-106">ActiveBasicDevice::IsVideoSupported property</span></span>

<span data-ttu-id="baac2-107">Ottiene un valore che indica se il dispositivo supporta il video.</span><span class="sxs-lookup"><span data-stu-id="baac2-107">Gets a value that indicates if the device supports video.</span></span>

<span data-ttu-id="baac2-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="baac2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="baac2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="baac2-109">Syntax</span></span>


```C++
HRESULT get_IsVideoSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="baac2-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="baac2-110">Property value</span></span>

<span data-ttu-id="baac2-111">Puntatore a un **valore booleano** che indica se il dispositivo supporta il video.</span><span class="sxs-lookup"><span data-stu-id="baac2-111">A pointer to a **boolean** that indicates if the device supports video.</span></span>

<span data-ttu-id="baac2-112">**true** se il dispositivo supporta il video; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="baac2-112">**true** if the device supports video; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="baac2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="baac2-113">Requirements</span></span>



| <span data-ttu-id="baac2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="baac2-114">Requirement</span></span> | <span data-ttu-id="baac2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="baac2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="baac2-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="baac2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="baac2-117">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="baac2-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="baac2-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="baac2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="baac2-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="baac2-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="baac2-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="baac2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="baac2-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="baac2-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="baac2-122">IDL</span><span class="sxs-lookup"><span data-stu-id="baac2-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="baac2-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="baac2-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="baac2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="baac2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="baac2-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baac2-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baac2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="baac2-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="baac2-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="baac2-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

