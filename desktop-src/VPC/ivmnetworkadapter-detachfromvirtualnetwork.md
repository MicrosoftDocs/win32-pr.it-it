---
title: Metodo IVMNetworkAdapter DetachFromVirtualNetwork (VPCCOMInterfaces. h)
description: Scollega l'interfaccia di rete dalla relativa rete virtuale.
ms.assetid: f1a00ea2-2b79-4b5c-a4bd-3cab66deb0d0
keywords:
- Metodo DetachFromVirtualNetwork Virtual PC
- Metodo DetachFromVirtualNetwork Virtual PC, interfaccia IVMNetworkAdapter
- Interfaccia IVMNetworkAdapter Virtual PC, metodo DetachFromVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.DetachFromVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d5046844764fe9e9eb6552fe1a04b6140201b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400697"
---
# <a name="ivmnetworkadapterdetachfromvirtualnetwork-method"></a><span data-ttu-id="ea375-106">IVMNetworkAdapter::D Metodo etachFromVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ea375-106">IVMNetworkAdapter::DetachFromVirtualNetwork method</span></span>

<span data-ttu-id="ea375-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ea375-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ea375-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ea375-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ea375-109">Scollega l'interfaccia di rete dalla relativa rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea375-109">Detaches the network interface from its virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea375-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea375-110">Syntax</span></span>


```C++
HRESULT DetachFromVirtualNetwork();
```



## <a name="parameters"></a><span data-ttu-id="ea375-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea375-111">Parameters</span></span>

<span data-ttu-id="ea375-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ea375-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea375-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea375-113">Return value</span></span>

<span data-ttu-id="ea375-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ea375-114">This method can return one of these values.</span></span>



| <span data-ttu-id="ea375-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea375-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="ea375-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea375-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ea375-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ea375-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ea375-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ea375-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="ea375-119"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ea375-119"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ea375-120">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="ea375-120">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ea375-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea375-121">Requirements</span></span>



| <span data-ttu-id="ea375-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea375-122">Requirement</span></span> | <span data-ttu-id="ea375-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ea375-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea375-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea375-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ea375-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ea375-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ea375-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea375-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ea375-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ea375-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ea375-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ea375-128">End of client support</span></span><br/>    | <span data-ttu-id="ea375-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ea375-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ea375-130">Prodotto</span><span class="sxs-lookup"><span data-stu-id="ea375-130">Product</span></span><br/>                  | <span data-ttu-id="ea375-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ea375-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ea375-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea375-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea375-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea375-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ea375-134">IID</span><span class="sxs-lookup"><span data-stu-id="ea375-134">IID</span></span><br/>                      | <span data-ttu-id="ea375-135">IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="ea375-135">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ea375-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea375-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea375-137">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="ea375-137">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

