---
title: Proprietà ActiveBasicDevice IsSetNextSourceSupported (PlayToDevice. h)
description: Ottiene un valore che indica se l'impostazione dell'origine successiva è supportata.
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- API di streaming multimediale della proprietà IsSetNextSourceSupported
- API di streaming multimediale della proprietà IsSetNextSourceSupported, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, proprietà IsSetNextSourceSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b84190336678e677ad3f0436d7233a49d4587574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302528"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a><span data-ttu-id="c06fe-106">Proprietà ActiveBasicDevice:: IsSetNextSourceSupported</span><span class="sxs-lookup"><span data-stu-id="c06fe-106">ActiveBasicDevice::IsSetNextSourceSupported property</span></span>

<span data-ttu-id="c06fe-107">Ottiene un valore che indica se l'impostazione dell'origine successiva è supportata.</span><span class="sxs-lookup"><span data-stu-id="c06fe-107">Gets a value that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="c06fe-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c06fe-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c06fe-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c06fe-109">Syntax</span></span>


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="c06fe-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c06fe-110">Property value</span></span>

<span data-ttu-id="c06fe-111">Puntatore a un **valore booleano** che indica se l'impostazione dell'origine successiva è supportata.</span><span class="sxs-lookup"><span data-stu-id="c06fe-111">A pointer to a **boolean** that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="c06fe-112">**true** se l'impostazione dell'origine successiva è supportata. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="c06fe-112">**true** if setting the next source is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c06fe-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c06fe-113">Requirements</span></span>



| <span data-ttu-id="c06fe-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c06fe-114">Requirement</span></span> | <span data-ttu-id="c06fe-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c06fe-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c06fe-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c06fe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c06fe-117">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c06fe-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c06fe-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c06fe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c06fe-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c06fe-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c06fe-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c06fe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c06fe-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c06fe-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="c06fe-122">IDL</span><span class="sxs-lookup"><span data-stu-id="c06fe-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c06fe-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c06fe-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="c06fe-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c06fe-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c06fe-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c06fe-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c06fe-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c06fe-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="c06fe-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c06fe-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

