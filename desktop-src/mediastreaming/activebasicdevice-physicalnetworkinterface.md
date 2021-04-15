---
title: Proprietà ActiveBasicDevice PhysicalNetworkInterface (PlayToDevice. h)
description: Ottiene l'ID dell'interfaccia di rete fisica.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- API di streaming multimediale della proprietà PhysicalNetworkInterface
- API di streaming multimediale della proprietà PhysicalNetworkInterface, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, proprietà PhysicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479618ed4d22a3d78a351fb88fcb1108a27c618f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477368"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a><span data-ttu-id="71d03-106">ActiveBasicDevice::P proprietà hysicalNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="71d03-106">ActiveBasicDevice::PhysicalNetworkInterface property</span></span>

<span data-ttu-id="71d03-107">Ottiene l'ID dell'interfaccia di rete fisica.</span><span class="sxs-lookup"><span data-stu-id="71d03-107">Gets the id of the physical network interface.</span></span>

<span data-ttu-id="71d03-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="71d03-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d03-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71d03-109">Syntax</span></span>


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="71d03-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="71d03-110">Property value</span></span>

<span data-ttu-id="71d03-111">Puntatore a un **GUID** che specifica l'ID dell'interfaccia di rete fisica.</span><span class="sxs-lookup"><span data-stu-id="71d03-111">A pointer to a **GUID** that specifies the id of the physical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="71d03-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71d03-112">Requirements</span></span>



| <span data-ttu-id="71d03-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="71d03-113">Requirement</span></span> | <span data-ttu-id="71d03-114">Valore</span><span class="sxs-lookup"><span data-stu-id="71d03-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d03-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71d03-115">Minimum supported client</span></span><br/> | <span data-ttu-id="71d03-116">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="71d03-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="71d03-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71d03-117">Minimum supported server</span></span><br/> | <span data-ttu-id="71d03-118">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="71d03-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="71d03-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71d03-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="71d03-120"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="71d03-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="71d03-121">IDL</span><span class="sxs-lookup"><span data-stu-id="71d03-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71d03-122"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71d03-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="71d03-123">DLL</span><span class="sxs-lookup"><span data-stu-id="71d03-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71d03-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71d03-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71d03-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71d03-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="71d03-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="71d03-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

