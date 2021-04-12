---
title: Proprietà ActiveBasicDevice IsSearchSupported (PlayToDevice. h)
description: Ottiene un valore che indica se il dispositivo supporta la ricerca.
ms.assetid: 091D467A-1FF6-4635-BF89-4E62AC9C660A
keywords:
- API di streaming multimediale della proprietà IsSearchSupported
- API di streaming multimediale della proprietà IsSearchSupported, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, proprietà IsSearchSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSearchSupported
- ActiveBasicDevice.get_IsSearchSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff97b20697388b1e3079f6993b97b948fa12091e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400898"
---
# <a name="activebasicdeviceissearchsupported-property"></a><span data-ttu-id="b768c-106">Proprietà ActiveBasicDevice:: IsSearchSupported</span><span class="sxs-lookup"><span data-stu-id="b768c-106">ActiveBasicDevice::IsSearchSupported property</span></span>

<span data-ttu-id="b768c-107">Ottiene un valore che indica se il dispositivo supporta la ricerca.</span><span class="sxs-lookup"><span data-stu-id="b768c-107">Gets a value that indicates if the device supports search.</span></span>

<span data-ttu-id="b768c-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b768c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b768c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b768c-109">Syntax</span></span>


```C++
HRESULT get_IsSearchSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="b768c-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b768c-110">Property value</span></span>

<span data-ttu-id="b768c-111">Puntatore a un **valore booleano** che indica se il dispositivo supporta la ricerca.</span><span class="sxs-lookup"><span data-stu-id="b768c-111">A pointer to a **boolean** that indicates if the device supports search.</span></span>

<span data-ttu-id="b768c-112">**true** se il dispositivo supporta la ricerca; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b768c-112">**true** if the device supports search; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b768c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b768c-113">Requirements</span></span>



| <span data-ttu-id="b768c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b768c-114">Requirement</span></span> | <span data-ttu-id="b768c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b768c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b768c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b768c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b768c-117">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b768c-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b768c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b768c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b768c-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b768c-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b768c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b768c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b768c-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b768c-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="b768c-122">IDL</span><span class="sxs-lookup"><span data-stu-id="b768c-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b768c-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b768c-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="b768c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b768c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b768c-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b768c-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b768c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b768c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b768c-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b768c-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

