---
title: Proprietà IVMVirtualPC UnconnectedNetworkAdapters (VPCCOMInterfaces. h)
description: Recupera una raccolta enumerabile di interfacce di rete non connesse.
ms.assetid: 2d95f289-083a-4388-b842-0a11b4e1a06f
keywords:
- Proprietà UnconnectedNetworkAdapters Virtual PC
- Proprietà UnconnectedNetworkAdapters Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà UnconnectedNetworkAdapters
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnconnectedNetworkAdapters
- IVMVirtualPC.get_UnconnectedNetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0694c6c5ce782e05ca322ba57f4ce7aaf5f708d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048490"
---
# <a name="ivmvirtualpcunconnectednetworkadapters-property"></a><span data-ttu-id="414a5-106">Proprietà IVMVirtualPC:: UnconnectedNetworkAdapters</span><span class="sxs-lookup"><span data-stu-id="414a5-106">IVMVirtualPC::UnconnectedNetworkAdapters property</span></span>

<span data-ttu-id="414a5-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="414a5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="414a5-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="414a5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="414a5-109">Recupera una raccolta enumerabile di interfacce di rete non connesse.</span><span class="sxs-lookup"><span data-stu-id="414a5-109">Retrieves an enumerable collection of unconnected network interfaces.</span></span>

<span data-ttu-id="414a5-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="414a5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="414a5-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="414a5-111">Syntax</span></span>


```C++
HRESULT get_UnconnectedNetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **unconnectedNetworkAdapterCollection
);
```



## <a name="property-value"></a><span data-ttu-id="414a5-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="414a5-112">Property value</span></span>

<span data-ttu-id="414a5-113">Raccolta di oggetti [**IVMNetworkAdapter**](ivmnetworkadapter.md) non connessi.</span><span class="sxs-lookup"><span data-stu-id="414a5-113">A collection of unconnected [**IVMNetworkAdapter**](ivmnetworkadapter.md) objects.</span></span> <span data-ttu-id="414a5-114">Vedere [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md).</span><span class="sxs-lookup"><span data-stu-id="414a5-114">See [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="414a5-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="414a5-115">Error codes</span></span>



| <span data-ttu-id="414a5-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="414a5-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="414a5-117">Significato</span><span class="sxs-lookup"><span data-stu-id="414a5-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="414a5-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="414a5-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="414a5-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="414a5-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="414a5-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="414a5-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="414a5-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="414a5-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="414a5-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="414a5-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="414a5-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="414a5-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="414a5-124"><dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="414a5-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="414a5-125">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="414a5-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="414a5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="414a5-126">Requirements</span></span>



| <span data-ttu-id="414a5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="414a5-127">Requirement</span></span> | <span data-ttu-id="414a5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="414a5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="414a5-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="414a5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="414a5-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="414a5-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="414a5-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="414a5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="414a5-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="414a5-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="414a5-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="414a5-133">End of client support</span></span><br/>    | <span data-ttu-id="414a5-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="414a5-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="414a5-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="414a5-135">Product</span></span><br/>                  | <span data-ttu-id="414a5-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="414a5-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="414a5-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="414a5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="414a5-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="414a5-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="414a5-139">IID</span><span class="sxs-lookup"><span data-stu-id="414a5-139">IID</span></span><br/>                      | <span data-ttu-id="414a5-140">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="414a5-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="414a5-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="414a5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="414a5-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="414a5-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

