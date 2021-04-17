---
title: Proprietà ActiveBasicDevice MaxVolume (PlayToDevice. h)
description: Ottiene il volume massimo supportato dal dispositivo.
ms.assetid: EA0EC323-4A18-4CC1-8FA4-7BD302318863
keywords:
- API di streaming multimediale della proprietà MaxVolume
- API di streaming multimediale della proprietà MaxVolume, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, proprietà MaxVolume
topic_type:
- apiref
api_name:
- ActiveBasicDevice.MaxVolume
- ActiveBasicDevice.get_MaxVolume
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48c25ef6c0e25c35ba07914c00fb063b4e8dc79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479090"
---
# <a name="activebasicdevicemaxvolume-property"></a><span data-ttu-id="01440-106">Proprietà ActiveBasicDevice:: MaxVolume</span><span class="sxs-lookup"><span data-stu-id="01440-106">ActiveBasicDevice::MaxVolume property</span></span>

<span data-ttu-id="01440-107">Ottiene il volume massimo supportato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01440-107">Gets the maximum volume supported by the device.</span></span>

<span data-ttu-id="01440-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="01440-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="01440-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01440-109">Syntax</span></span>


```C++
HRESULT get_MaxVolume(
  [out] boolean *UINT32
);
```



## <a name="property-value"></a><span data-ttu-id="01440-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="01440-110">Property value</span></span>

<span data-ttu-id="01440-111">Puntatore a un oggetto **UInt32** che specifica il volume massimo supportato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01440-111">A pointer to a **UINT32** that specifies the maximum volume supported by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="01440-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01440-112">Requirements</span></span>



| <span data-ttu-id="01440-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="01440-113">Requirement</span></span> | <span data-ttu-id="01440-114">Valore</span><span class="sxs-lookup"><span data-stu-id="01440-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="01440-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01440-115">Minimum supported client</span></span><br/> | <span data-ttu-id="01440-116">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01440-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="01440-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01440-117">Minimum supported server</span></span><br/> | <span data-ttu-id="01440-118">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="01440-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="01440-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01440-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="01440-120"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="01440-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="01440-121">IDL</span><span class="sxs-lookup"><span data-stu-id="01440-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="01440-122"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01440-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="01440-123">DLL</span><span class="sxs-lookup"><span data-stu-id="01440-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01440-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01440-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01440-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01440-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="01440-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01440-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

