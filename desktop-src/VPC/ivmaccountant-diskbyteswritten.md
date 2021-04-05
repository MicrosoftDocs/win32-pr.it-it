---
title: Proprietà IVMAccountant DiskBytesWritten (VPCCOMInterfaces. h)
description: Numero totale di byte scritti da tutti i controller di archiviazione per questa macchina virtuale.
ms.assetid: a2a5730b-a411-48b8-aca8-d09cf09432a9
keywords:
- Proprietà DiskBytesWritten Virtual PC
- Proprietà DiskBytesWritten Virtual PC, interfaccia IVMAccountant
- Interfaccia IVMAccountant Virtual PC, proprietà DiskBytesWritten
topic_type:
- apiref
api_name:
- IVMAccountant.DiskBytesWritten
- IVMAccountant.get_DiskBytesWritten
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e9ad27acf538af25daec676289df5e7664b169
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874502"
---
# <a name="ivmaccountantdiskbyteswritten-property"></a><span data-ttu-id="4154c-106">IVMAccountant::D Proprietà iskBytesWritten</span><span class="sxs-lookup"><span data-stu-id="4154c-106">IVMAccountant::DiskBytesWritten property</span></span>

<span data-ttu-id="4154c-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4154c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4154c-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4154c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4154c-109">Recupera il numero totale di byte scritti da tutti i controller di archiviazione per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4154c-109">Retrieves the total number of bytes written by all storage controllers for this virtual machine.</span></span>

<span data-ttu-id="4154c-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4154c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4154c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4154c-111">Syntax</span></span>


```C++
HRESULT get_DiskBytesWritten(
  [out, retval] VARIANT *bytesWritten
);
```



## <a name="property-value"></a><span data-ttu-id="4154c-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4154c-112">Property value</span></span>

<span data-ttu-id="4154c-113">Numero totale di byte.</span><span class="sxs-lookup"><span data-stu-id="4154c-113">The total number of bytes.</span></span> <span data-ttu-id="4154c-114">Questi dati vengono restituiti come **Variant** di tipo **\_ decimale VT**.</span><span class="sxs-lookup"><span data-stu-id="4154c-114">This data is returned as a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4154c-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4154c-115">Error codes</span></span>



| <span data-ttu-id="4154c-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="4154c-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4154c-117">Significato</span><span class="sxs-lookup"><span data-stu-id="4154c-117">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="4154c-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4154c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4154c-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4154c-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="4154c-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4154c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4154c-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="4154c-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="4154c-122"><dt>S \_ FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4154c-122"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="4154c-123">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4154c-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="4154c-124"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4154c-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4154c-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="4154c-125">An unexpected error has occurred.</span></span><br/>   |



## <a name="remarks"></a><span data-ttu-id="4154c-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="4154c-126">Remarks</span></span>

<span data-ttu-id="4154c-127">Si noti che le statistiche di I/O su disco vengono reimpostate su zero quando una macchina virtuale viene accesa, reimpostata o ripristinata dallo stato salvato.</span><span class="sxs-lookup"><span data-stu-id="4154c-127">Note that disk I/O statistics are reset to zero when a virtual machine is powered up, reset, or restored from saved state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4154c-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4154c-128">Requirements</span></span>



| <span data-ttu-id="4154c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4154c-129">Requirement</span></span> | <span data-ttu-id="4154c-130">Valore</span><span class="sxs-lookup"><span data-stu-id="4154c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4154c-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4154c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4154c-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4154c-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4154c-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4154c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4154c-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4154c-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4154c-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4154c-135">End of client support</span></span><br/>    | <span data-ttu-id="4154c-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4154c-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4154c-137">Prodotto</span><span class="sxs-lookup"><span data-stu-id="4154c-137">Product</span></span><br/>                  | <span data-ttu-id="4154c-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4154c-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4154c-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4154c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4154c-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4154c-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4154c-141">IID</span><span class="sxs-lookup"><span data-stu-id="4154c-141">IID</span></span><br/>                      | <span data-ttu-id="4154c-142">IID \_ IVMAccountant è definito come 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="4154c-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="4154c-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4154c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4154c-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="4154c-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

