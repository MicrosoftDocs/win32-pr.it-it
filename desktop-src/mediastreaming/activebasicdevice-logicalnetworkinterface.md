---
title: Proprietà ActiveBasicDevice LogicalNetworkInterface (PlayToDevice. h)
description: Ottiene l'ID dell'interfaccia di rete logica.
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- API di streaming multimediale della proprietà LogicalNetworkInterface
- API di streaming multimediale della proprietà LogicalNetworkInterface, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, proprietà LogicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.LogicalNetworkInterface
- ActiveBasicDevice.get_LogicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95a87f2951ea09a0bba3d56da50b8f77a9d4a980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400549"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a><span data-ttu-id="4345e-106">Proprietà ActiveBasicDevice:: LogicalNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4345e-106">ActiveBasicDevice::LogicalNetworkInterface property</span></span>

<span data-ttu-id="4345e-107">Ottiene l'ID dell'interfaccia di rete logica.</span><span class="sxs-lookup"><span data-stu-id="4345e-107">Gets the id of the logical network interface.</span></span>

<span data-ttu-id="4345e-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4345e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4345e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4345e-109">Syntax</span></span>


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="4345e-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4345e-110">Property value</span></span>

<span data-ttu-id="4345e-111">Puntatore a un **GUID** che specifica l'ID dell'interfaccia di rete logica.</span><span class="sxs-lookup"><span data-stu-id="4345e-111">A pointer to a **GUID** that specifies the id of the logical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4345e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4345e-112">Requirements</span></span>



| <span data-ttu-id="4345e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4345e-113">Requirement</span></span> | <span data-ttu-id="4345e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4345e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4345e-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4345e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4345e-116">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4345e-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4345e-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4345e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4345e-118">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4345e-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4345e-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4345e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4345e-120"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="4345e-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="4345e-121">IDL</span><span class="sxs-lookup"><span data-stu-id="4345e-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4345e-122"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4345e-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="4345e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4345e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4345e-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4345e-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4345e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4345e-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="4345e-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4345e-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

