---
title: Proprietà IVMVirtualNetwork I NetworkAdapter (VPCCOMInterfaces. h)
description: Recupera una raccolta enumerabile di schede di rete collegate alla rete virtuale.
ms.assetid: d5b95831-4642-441e-93e8-34e125087a43
keywords:
- Proprietà I NetworkAdapter Virtual PC
- Proprietà I NetworkAdapter Virtual PC, interfaccia IVMVirtualNetwork
- Interfaccia IVMVirtualNetwork Virtual PC, proprietà I NetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.NetworkAdapters
- IVMVirtualNetwork.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ba86f649744eeb34139c65de9aa4523ddc74d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302551"
---
# <a name="ivmvirtualnetworknetworkadapters-property"></a><span data-ttu-id="955dc-106">Proprietà IVMVirtualNetwork:: I NetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="955dc-106">IVMVirtualNetwork::NetworkAdapters property</span></span>

<span data-ttu-id="955dc-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="955dc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="955dc-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="955dc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="955dc-109">Recupera una raccolta enumerabile di schede di rete collegate alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="955dc-109">Retrieves an enumerable collection of NICs attached to the virtual network.</span></span>

<span data-ttu-id="955dc-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="955dc-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="955dc-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="955dc-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkInterfaceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="955dc-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="955dc-112">Property value</span></span>

<span data-ttu-id="955dc-113">Nuovo [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) che include le schede di rete virtuali collegate a questa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="955dc-113">A new [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) which holds the virtual NICs attached to this virtual network.</span></span>

## <a name="error-codes"></a><span data-ttu-id="955dc-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="955dc-114">Error codes</span></span>



| <span data-ttu-id="955dc-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="955dc-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="955dc-116">Significato</span><span class="sxs-lookup"><span data-stu-id="955dc-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="955dc-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="955dc-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="955dc-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="955dc-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="955dc-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="955dc-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="955dc-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="955dc-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="955dc-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="955dc-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="955dc-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="955dc-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="955dc-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="955dc-123">Requirements</span></span>



| <span data-ttu-id="955dc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="955dc-124">Requirement</span></span> | <span data-ttu-id="955dc-125">Valore</span><span class="sxs-lookup"><span data-stu-id="955dc-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="955dc-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="955dc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="955dc-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="955dc-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="955dc-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="955dc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="955dc-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="955dc-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="955dc-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="955dc-130">End of client support</span></span><br/>    | <span data-ttu-id="955dc-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="955dc-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="955dc-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="955dc-132">Product</span></span><br/>                  | <span data-ttu-id="955dc-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="955dc-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="955dc-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="955dc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="955dc-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="955dc-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="955dc-136">IID</span><span class="sxs-lookup"><span data-stu-id="955dc-136">IID</span></span><br/>                      | <span data-ttu-id="955dc-137">IID \_ IVMVirtualNetwork è definito come 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="955dc-137">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="955dc-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="955dc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="955dc-139">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="955dc-139">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

