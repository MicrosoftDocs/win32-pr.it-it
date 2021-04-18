---
title: Proprietà ActiveBasicDevice IsImageSupported (PlayToDevice. h)
description: Ottiene un valore che indica se il dispositivo supporta le immagini.
ms.assetid: FC53B87C-D739-4AD4-9DD3-415AC8692224
keywords:
- API di streaming multimediale della proprietà IsImageSupported
- API di streaming multimediale della proprietà IsImageSupported, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, proprietà IsImageSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsImageSupported
- ActiveBasicDevice.get_IsImageSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2e90f51d2dd59ffec8221787b9ee7c247536abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301026"
---
# <a name="activebasicdeviceisimagesupported-property"></a><span data-ttu-id="da5b6-106">Proprietà ActiveBasicDevice:: IsImageSupported</span><span class="sxs-lookup"><span data-stu-id="da5b6-106">ActiveBasicDevice::IsImageSupported property</span></span>

<span data-ttu-id="da5b6-107">Ottiene un valore che indica se il dispositivo supporta le immagini.</span><span class="sxs-lookup"><span data-stu-id="da5b6-107">Gets a value that indicates if the device supports images.</span></span>

<span data-ttu-id="da5b6-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="da5b6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="da5b6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da5b6-109">Syntax</span></span>


```C++
HRESULT get_IsImageSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="da5b6-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="da5b6-110">Property value</span></span>

<span data-ttu-id="da5b6-111">Puntatore a un **valore booleano** che indica se il dispositivo supporta le immagini.</span><span class="sxs-lookup"><span data-stu-id="da5b6-111">A pointer to a **boolean** that indicates if the device supports images.</span></span>

<span data-ttu-id="da5b6-112">**true** se il dispositivo supporta le immagini; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="da5b6-112">**true** if the device supports images; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="da5b6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da5b6-113">Requirements</span></span>



| <span data-ttu-id="da5b6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="da5b6-114">Requirement</span></span> | <span data-ttu-id="da5b6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="da5b6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="da5b6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da5b6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="da5b6-117">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da5b6-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="da5b6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da5b6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="da5b6-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="da5b6-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="da5b6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da5b6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="da5b6-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="da5b6-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="da5b6-122">IDL</span><span class="sxs-lookup"><span data-stu-id="da5b6-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="da5b6-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="da5b6-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="da5b6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="da5b6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da5b6-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da5b6-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da5b6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da5b6-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="da5b6-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="da5b6-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

