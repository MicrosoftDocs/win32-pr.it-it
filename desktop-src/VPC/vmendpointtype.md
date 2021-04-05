---
title: Enumerazione VMEndpointType (VPCCOMInterfaces. h)
description: Specifica il tipo di endpoint.
ms.assetid: b48bd860-50dc-4c8c-b65b-69c407d4612a
keywords:
- VMEndpointType enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMEndpointType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912eb43147af03dd2b9923c4bdb778044f40d023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873737"
---
# <a name="vmendpointtype-enumeration"></a><span data-ttu-id="e8d19-104">Enumerazione VMEndpointType</span><span class="sxs-lookup"><span data-stu-id="e8d19-104">VMEndpointType enumeration</span></span>

<span data-ttu-id="e8d19-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e8d19-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e8d19-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e8d19-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e8d19-107">Specifica il tipo di endpoint.</span><span class="sxs-lookup"><span data-stu-id="e8d19-107">Specifies the endpoint type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8d19-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8d19-108">Syntax</span></span>


```C++
typedef enum  { 
  vmEndpoint_NamedPipe  = 0,
  vmEndpoint_TCPIP      = 1
} VMEndpointType;
```



## <a name="constants"></a><span data-ttu-id="e8d19-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="e8d19-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e8d19-110"><span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**\_NamedPipe vmEndpoint**</span><span class="sxs-lookup"><span data-stu-id="e8d19-110"><span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**vmEndpoint\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="e8d19-111">Lato host.</span><span class="sxs-lookup"><span data-stu-id="e8d19-111">The host side.</span></span>

</dd> <dt>

<span data-ttu-id="e8d19-112"><span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**vmEndpoint \_ Tcpip**</span><span class="sxs-lookup"><span data-stu-id="e8d19-112"><span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**vmEndpoint\_TCPIP**</span></span>
</dt> <dd>

<span data-ttu-id="e8d19-113">Lato Guest.</span><span class="sxs-lookup"><span data-stu-id="e8d19-113">The guest side.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8d19-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8d19-114">Requirements</span></span>



| <span data-ttu-id="e8d19-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8d19-115">Requirement</span></span> | <span data-ttu-id="e8d19-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e8d19-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d19-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8d19-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e8d19-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e8d19-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8d19-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8d19-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e8d19-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e8d19-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e8d19-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e8d19-121">End of client support</span></span><br/>    | <span data-ttu-id="e8d19-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8d19-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e8d19-123">Prodotto</span><span class="sxs-lookup"><span data-stu-id="e8d19-123">Product</span></span><br/>                  | <span data-ttu-id="e8d19-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e8d19-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e8d19-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8d19-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8d19-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8d19-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8d19-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8d19-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8d19-128">**IVMVirtualMachine::StartCommunicationChannel**</span><span class="sxs-lookup"><span data-stu-id="e8d19-128">**IVMVirtualMachine::StartCommunicationChannel**</span></span>](ivmvirtualmachine-startcommunicationchannel.md)
</dt> </dl>

 

