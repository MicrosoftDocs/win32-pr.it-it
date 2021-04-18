---
title: Proprietà IVMVirtualMachine FloppyDrives (VPCCOMInterfaces. h)
description: Recupera una raccolta enumerabile di unità floppy collegate alla macchina virtuale.
ms.assetid: 8b8ea1c7-77c3-46b6-ab0b-0c7b4ab387ae
keywords:
- Proprietà FloppyDrives Virtual PC
- Proprietà FloppyDrives Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà FloppyDrives
topic_type:
- apiref
api_name:
- IVMVirtualMachine.FloppyDrives
- IVMVirtualMachine.get_FloppyDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4ec942d55c3d98b3d45a013fb1142ea097edfca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302412"
---
# <a name="ivmvirtualmachinefloppydrives-property"></a><span data-ttu-id="c0f99-106">Proprietà IVMVirtualMachine:: FloppyDrives</span><span class="sxs-lookup"><span data-stu-id="c0f99-106">IVMVirtualMachine::FloppyDrives property</span></span>

<span data-ttu-id="c0f99-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c0f99-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c0f99-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c0f99-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c0f99-109">Recupera una raccolta enumerabile di unità floppy collegate alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0f99-109">Retrieves an enumerable collection of floppy drives attached to the virtual machine.</span></span>

<span data-ttu-id="c0f99-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c0f99-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f99-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0f99-111">Syntax</span></span>


```C++
HRESULT get_FloppyDrives(
  [out, retval] IVMFloppyDriveCollection **floppyCollection
);
```



## <a name="property-value"></a><span data-ttu-id="c0f99-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c0f99-112">Property value</span></span>

<span data-ttu-id="c0f99-113">Oggetto [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="c0f99-113">An [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c0f99-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c0f99-114">Error codes</span></span>



| <span data-ttu-id="c0f99-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="c0f99-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c0f99-116">Significato</span><span class="sxs-lookup"><span data-stu-id="c0f99-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c0f99-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c0f99-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c0f99-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c0f99-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c0f99-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c0f99-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c0f99-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="c0f99-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c0f99-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c0f99-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c0f99-122">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="c0f99-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="c0f99-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c0f99-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c0f99-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="c0f99-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c0f99-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0f99-125">Requirements</span></span>



| <span data-ttu-id="c0f99-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0f99-126">Requirement</span></span> | <span data-ttu-id="c0f99-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c0f99-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f99-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0f99-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f99-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c0f99-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0f99-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0f99-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f99-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c0f99-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c0f99-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c0f99-132">End of client support</span></span><br/>    | <span data-ttu-id="c0f99-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0f99-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c0f99-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c0f99-134">Product</span></span><br/>                  | <span data-ttu-id="c0f99-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c0f99-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c0f99-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0f99-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0f99-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0f99-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c0f99-138">IID</span><span class="sxs-lookup"><span data-stu-id="c0f99-138">IID</span></span><br/>                      | <span data-ttu-id="c0f99-139">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="c0f99-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c0f99-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0f99-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f99-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="c0f99-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

