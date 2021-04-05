---
title: Proprietà IVMFloppyDrive DriveNumber (VPCCOMInterfaces. h)
description: Recupera l'indice in base zero del controller a cui è collegata l'unità floppy.
ms.assetid: 79a40cad-d280-4c67-9214-0532569e47e4
keywords:
- Proprietà DriveNumber Virtual PC
- Proprietà DriveNumber Virtual PC, interfaccia IVMFloppyDrive
- Interfaccia IVMFloppyDrive Virtual PC, proprietà DriveNumber
topic_type:
- apiref
api_name:
- IVMFloppyDrive.DriveNumber
- IVMFloppyDrive.get_DriveNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2f2aeacaf3067515e9e44c58422cd4c9f31fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873953"
---
# <a name="ivmfloppydrivedrivenumber-property"></a><span data-ttu-id="bed4c-106">IVMFloppyDrive::D Proprietà riveNumber</span><span class="sxs-lookup"><span data-stu-id="bed4c-106">IVMFloppyDrive::DriveNumber property</span></span>

<span data-ttu-id="bed4c-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bed4c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bed4c-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bed4c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bed4c-109">Recupera l'indice in base zero del controller a cui è collegata l'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="bed4c-109">Retrieves the zero-based index of the controller to which the floppy drive is attached.</span></span>

<span data-ttu-id="bed4c-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bed4c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bed4c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bed4c-111">Syntax</span></span>


```C++
HRESULT get_DriveNumber(
  [out, retval] long *driveNumber
);
```



## <a name="property-value"></a><span data-ttu-id="bed4c-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bed4c-112">Property value</span></span>

<span data-ttu-id="bed4c-113">Indice in base zero del controller.</span><span class="sxs-lookup"><span data-stu-id="bed4c-113">The zero-based index of the controller.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bed4c-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="bed4c-114">Error codes</span></span>



| <span data-ttu-id="bed4c-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="bed4c-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="bed4c-116">Significato</span><span class="sxs-lookup"><span data-stu-id="bed4c-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bed4c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bed4c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="bed4c-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="bed4c-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="bed4c-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bed4c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="bed4c-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="bed4c-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="bed4c-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bed4c-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="bed4c-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="bed4c-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bed4c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bed4c-123">Requirements</span></span>



| <span data-ttu-id="bed4c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bed4c-124">Requirement</span></span> | <span data-ttu-id="bed4c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="bed4c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bed4c-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bed4c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bed4c-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bed4c-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bed4c-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bed4c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bed4c-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bed4c-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bed4c-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bed4c-130">End of client support</span></span><br/>    | <span data-ttu-id="bed4c-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bed4c-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bed4c-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="bed4c-132">Product</span></span><br/>                  | <span data-ttu-id="bed4c-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bed4c-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bed4c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bed4c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bed4c-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bed4c-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bed4c-136">IID</span><span class="sxs-lookup"><span data-stu-id="bed4c-136">IID</span></span><br/>                      | <span data-ttu-id="bed4c-137">IID \_ IVMFloppyDrive è definito come 661abee6-112A-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="bed4c-137">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="bed4c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bed4c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed4c-139">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="bed4c-139">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

