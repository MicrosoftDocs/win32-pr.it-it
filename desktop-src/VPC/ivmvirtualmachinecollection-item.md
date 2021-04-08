---
title: Proprietà Item di IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Recupera l'oggetto macchina virtuale che corrisponde all'indice specificato.
ms.assetid: b3afe211-5d97-4ccf-96b7-e074deb320fb
keywords:
- Proprietà elemento Virtual PC
- Proprietà elemento Virtual PC, interfaccia IVMVirtualMachineCollection
- Interfaccia IVMVirtualMachineCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Item
- IVMVirtualMachineCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d70a6e30ff53f234f40803cd02fa16539f09e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047798"
---
# <a name="ivmvirtualmachinecollectionitem-property"></a><span data-ttu-id="df391-106">Proprietà IVMVirtualMachineCollection:: Item</span><span class="sxs-lookup"><span data-stu-id="df391-106">IVMVirtualMachineCollection::Item property</span></span>

<span data-ttu-id="df391-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="df391-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="df391-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="df391-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="df391-109">Recupera l'oggetto macchina virtuale che corrisponde all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="df391-109">Retrieves the virtual machine object that corresponds to the specified index.</span></span>

<span data-ttu-id="df391-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="df391-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="df391-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df391-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="df391-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="df391-112">Property value</span></span>

<span data-ttu-id="df391-113">Oggetto [**IVMVirtualMachine**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="df391-113">The [**IVMVirtualMachine**](ivmvirtualmachine.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="df391-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="df391-114">Error codes</span></span>



| <span data-ttu-id="df391-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="df391-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="df391-116">Significato</span><span class="sxs-lookup"><span data-stu-id="df391-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df391-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="df391-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="df391-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="df391-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="df391-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="df391-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="df391-120">Il parametro *virtualmachine* è **null**.</span><span class="sxs-lookup"><span data-stu-id="df391-120">The *virtualMachine* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="df391-121"><dt>Disp \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="df391-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="df391-122">L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="df391-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="df391-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="df391-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="df391-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="df391-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="df391-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df391-125">Requirements</span></span>



| <span data-ttu-id="df391-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="df391-126">Requirement</span></span> | <span data-ttu-id="df391-127">Valore</span><span class="sxs-lookup"><span data-stu-id="df391-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df391-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df391-128">Minimum supported client</span></span><br/> | <span data-ttu-id="df391-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="df391-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="df391-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df391-130">Minimum supported server</span></span><br/> | <span data-ttu-id="df391-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="df391-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="df391-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="df391-132">End of client support</span></span><br/>    | <span data-ttu-id="df391-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="df391-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="df391-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="df391-134">Product</span></span><br/>                  | <span data-ttu-id="df391-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="df391-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="df391-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df391-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="df391-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="df391-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="df391-138">IID</span><span class="sxs-lookup"><span data-stu-id="df391-138">IID</span></span><br/>                      | <span data-ttu-id="df391-139">IID \_ IVMVirtualMachineCollection è definito come 59f31786-2a3d-4FBF-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="df391-139">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df391-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df391-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df391-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="df391-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="df391-142">**IVMVirtualMachineCollection**</span><span class="sxs-lookup"><span data-stu-id="df391-142">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

