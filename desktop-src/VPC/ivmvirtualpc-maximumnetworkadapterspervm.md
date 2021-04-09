---
title: Proprietà IVMVirtualPC MaximumNetworkAdaptersPerVM (VPCCOMInterfaces. h)
description: Numero massimo di interfacce di rete per macchina virtuale.
ms.assetid: 92da4958-5a67-422e-a6bd-68cabf1835ab
keywords:
- Proprietà MaximumNetworkAdaptersPerVM Virtual PC
- Proprietà MaximumNetworkAdaptersPerVM Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà MaximumNetworkAdaptersPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumNetworkAdaptersPerVM
- IVMVirtualPC.get_MaximumNetworkAdaptersPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0797775038440c566fa7a3397b05632af839a341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118899"
---
# <a name="ivmvirtualpcmaximumnetworkadapterspervm-property"></a><span data-ttu-id="a9f31-106">Proprietà IVMVirtualPC:: MaximumNetworkAdaptersPerVM</span><span class="sxs-lookup"><span data-stu-id="a9f31-106">IVMVirtualPC::MaximumNetworkAdaptersPerVM property</span></span>

<span data-ttu-id="a9f31-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a9f31-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a9f31-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a9f31-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a9f31-109">Recupera il numero massimo di interfacce di rete per macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a9f31-109">Retrieves the maximum number of networks interfaces per virtual machine.</span></span>

<span data-ttu-id="a9f31-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a9f31-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9f31-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9f31-111">Syntax</span></span>


```C++
HRESULT get_MaximumNetworkAdaptersPerVM(
  [out, retval] long *maxNetworkAdapters
);
```



## <a name="property-value"></a><span data-ttu-id="a9f31-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a9f31-112">Property value</span></span>

<span data-ttu-id="a9f31-113">Numero massimo di interfacce di rete per macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a9f31-113">The maximum number of network interfaces per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a9f31-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a9f31-114">Error codes</span></span>



| <span data-ttu-id="a9f31-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="a9f31-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="a9f31-116">Significato</span><span class="sxs-lookup"><span data-stu-id="a9f31-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a9f31-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a9f31-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="a9f31-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a9f31-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a9f31-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a9f31-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="a9f31-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="a9f31-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="a9f31-121"><dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="a9f31-121"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="a9f31-122">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="a9f31-122">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a9f31-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9f31-123">Requirements</span></span>



| <span data-ttu-id="a9f31-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9f31-124">Requirement</span></span> | <span data-ttu-id="a9f31-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a9f31-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f31-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9f31-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a9f31-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a9f31-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9f31-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9f31-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a9f31-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a9f31-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a9f31-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a9f31-130">End of client support</span></span><br/>    | <span data-ttu-id="a9f31-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9f31-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a9f31-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a9f31-132">Product</span></span><br/>                  | <span data-ttu-id="a9f31-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a9f31-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a9f31-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9f31-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9f31-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9f31-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a9f31-136">IID</span><span class="sxs-lookup"><span data-stu-id="a9f31-136">IID</span></span><br/>                      | <span data-ttu-id="a9f31-137">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="a9f31-137">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a9f31-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9f31-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9f31-139">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="a9f31-139">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

