---
title: Proprietà Name di IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Nome univoco dell'istanza di rete virtuale.
ms.assetid: dd4807dc-abae-4bdb-ba27-597cf1337834
keywords:
- Nome proprietà PC virtuale
- Proprietà nome Virtual PC, interfaccia IVMVirtualNetwork
- Interfaccia IVMVirtualNetwork Virtual PC, proprietà Name
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.Name
- IVMVirtualNetwork.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c962d7b65bfddaf5293bd391ae84f04bae512ba9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964771"
---
# <a name="ivmvirtualnetworkname-property"></a><span data-ttu-id="7d099-106">Proprietà IVMVirtualNetwork:: Name</span><span class="sxs-lookup"><span data-stu-id="7d099-106">IVMVirtualNetwork::Name property</span></span>

<span data-ttu-id="7d099-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7d099-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7d099-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7d099-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7d099-109">Recupera il nome univoco dell'istanza di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7d099-109">Retrieves the unique name of the virtual network instance.</span></span>

<span data-ttu-id="7d099-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7d099-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d099-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d099-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualNetworkName
);
```



## <a name="property-value"></a><span data-ttu-id="7d099-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7d099-112">Property value</span></span>

<span data-ttu-id="7d099-113">nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7d099-113">The name of the virtual network.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7d099-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7d099-114">Error codes</span></span>



| <span data-ttu-id="7d099-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="7d099-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7d099-116">Significato</span><span class="sxs-lookup"><span data-stu-id="7d099-116">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7d099-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7d099-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7d099-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7d099-118">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="7d099-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7d099-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7d099-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="7d099-120">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="7d099-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7d099-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7d099-122">Si è verificato un errore imprevisto o l'istanza della rete virtuale è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="7d099-122">An unexpected error has occurred or the virtual network instance is unknown.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7d099-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d099-123">Remarks</span></span>

<span data-ttu-id="7d099-124">I nomi delle reti virtuali non fanno distinzione tra maiuscole e minuscole, ad esempio, "rete" e "rete" si riferiscono alla stessa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7d099-124">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d099-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d099-125">Requirements</span></span>



| <span data-ttu-id="7d099-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d099-126">Requirement</span></span> | <span data-ttu-id="7d099-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7d099-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d099-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d099-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7d099-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7d099-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d099-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d099-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7d099-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7d099-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7d099-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7d099-132">End of client support</span></span><br/>    | <span data-ttu-id="7d099-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7d099-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7d099-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="7d099-134">Product</span></span><br/>                  | <span data-ttu-id="7d099-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7d099-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7d099-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d099-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d099-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d099-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7d099-138">IID</span><span class="sxs-lookup"><span data-stu-id="7d099-138">IID</span></span><br/>                      | <span data-ttu-id="7d099-139">IID \_ IVMVirtualNetwork è definito come 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="7d099-139">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7d099-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d099-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d099-141">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="7d099-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

