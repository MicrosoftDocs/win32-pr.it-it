---
title: Proprietà Name di IVMParallelPort (VPCCOMInterfaces. h)
description: Nome della porta parallela.
ms.assetid: 254df134-2b48-4a81-8229-0f5fbacf2e1c
keywords:
- Nome proprietà PC virtuale
- Proprietà nome Virtual PC, interfaccia IVMParallelPort
- Interfaccia IVMParallelPort Virtual PC, proprietà Name
topic_type:
- apiref
api_name:
- IVMParallelPort.Name
- IVMParallelPort.get_Name
- IVMParallelPort.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f89638504b7e0fd8814ea8b429ee70f43c6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118910"
---
# <a name="ivmparallelportname-property"></a><span data-ttu-id="3c3ef-106">Proprietà IVMParallelPort:: Name</span><span class="sxs-lookup"><span data-stu-id="3c3ef-106">IVMParallelPort::Name property</span></span>

<span data-ttu-id="3c3ef-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3c3ef-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3c3ef-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3c3ef-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3c3ef-109">Recupera e imposta il nome della porta parallela.</span><span class="sxs-lookup"><span data-stu-id="3c3ef-109">Retrieves and sets the name of the parallel port.</span></span>

<span data-ttu-id="3c3ef-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3c3ef-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c3ef-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c3ef-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR portName
);

HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="3c3ef-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3c3ef-112">Property value</span></span>

<span data-ttu-id="3c3ef-113">Imposta il nome della porta parallela (ad esempio, "LPT1").</span><span class="sxs-lookup"><span data-stu-id="3c3ef-113">Sets the name of the parallel port (for example, "LPT1").</span></span>

## <a name="error-codes"></a><span data-ttu-id="3c3ef-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="3c3ef-114">Error codes</span></span>



| <span data-ttu-id="3c3ef-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="3c3ef-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3c3ef-116">Significato</span><span class="sxs-lookup"><span data-stu-id="3c3ef-116">Meaning</span></span>                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c3ef-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c3ef-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3c3ef-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3c3ef-118">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="3c3ef-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3c3ef-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3c3ef-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="3c3ef-120">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="3c3ef-121"><dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3c3ef-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="3c3ef-122">Il parametro fa riferimento a una porta parallela non valida.</span><span class="sxs-lookup"><span data-stu-id="3c3ef-122">The parameter refers to a parallel port that is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="3c3ef-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3c3ef-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="3c3ef-124">La configurazione per questa macchina virtuale non è valida.</span><span class="sxs-lookup"><span data-stu-id="3c3ef-124">The configuration for this virtual machine is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="3c3ef-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3c3ef-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3c3ef-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="3c3ef-126">An unexpected error has occurred.</span></span><br/>                          |



## <a name="requirements"></a><span data-ttu-id="3c3ef-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c3ef-127">Requirements</span></span>



| <span data-ttu-id="3c3ef-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c3ef-128">Requirement</span></span> | <span data-ttu-id="3c3ef-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3c3ef-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3ef-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c3ef-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3c3ef-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3c3ef-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c3ef-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c3ef-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3c3ef-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3c3ef-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3c3ef-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3c3ef-134">End of client support</span></span><br/>    | <span data-ttu-id="3c3ef-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3c3ef-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3c3ef-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="3c3ef-136">Product</span></span><br/>                  | <span data-ttu-id="3c3ef-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3c3ef-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3c3ef-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c3ef-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c3ef-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c3ef-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3c3ef-140">IID</span><span class="sxs-lookup"><span data-stu-id="3c3ef-140">IID</span></span><br/>                      | <span data-ttu-id="3c3ef-141">IID \_ IVMParallelPort è definito come 097beecb-0A02-474F-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="3c3ef-141">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="3c3ef-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c3ef-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c3ef-143">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="3c3ef-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> </dl>

 

