---
title: Proprietà Error IVMTask (VPCCOMInterfaces. h)
description: Recupera l'errore registrato per questa attività.
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Proprietà errore Virtual PC
- Proprietà Error Virtual PC, interfaccia IVMTask
- Interfaccia IVMTask Virtual PC, proprietà Error
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301844"
---
# <a name="ivmtaskerror-property"></a><span data-ttu-id="38fa4-106">Proprietà IVMTask:: Error</span><span class="sxs-lookup"><span data-stu-id="38fa4-106">IVMTask::Error property</span></span>

<span data-ttu-id="38fa4-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="38fa4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="38fa4-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="38fa4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="38fa4-109">Recupera l'errore registrato per questa attività.</span><span class="sxs-lookup"><span data-stu-id="38fa4-109">Retrieves the error recorded for this task.</span></span>

<span data-ttu-id="38fa4-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="38fa4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="38fa4-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38fa4-111">Syntax</span></span>


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a><span data-ttu-id="38fa4-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="38fa4-112">Property value</span></span>

<span data-ttu-id="38fa4-113">Errore registrato.</span><span class="sxs-lookup"><span data-stu-id="38fa4-113">The recorded error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="38fa4-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="38fa4-114">Error codes</span></span>

<span data-ttu-id="38fa4-115">Le istanze di [**IVMTask**](ivmtask.md) restituite da altre interfacce possono restituire valori aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="38fa4-115">Instances of [**IVMTask**](ivmtask.md) returned by other interfaces may return additional values.</span></span> <span data-ttu-id="38fa4-116">Per informazioni dettagliate, vedere la documentazione relativa ai metodi che restituiscono un'istanza di **IVMTask** .</span><span class="sxs-lookup"><span data-stu-id="38fa4-116">For details, see the documentation of the methods that return a **IVMTask** instance.</span></span>



| <span data-ttu-id="38fa4-117">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="38fa4-117">Name/value</span></span>                                                                                                                                                                        | <span data-ttu-id="38fa4-118">Significato</span><span class="sxs-lookup"><span data-stu-id="38fa4-118">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="38fa4-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="38fa4-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                           | <span data-ttu-id="38fa4-120">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="38fa4-120">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="38fa4-121"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="38fa4-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                             | <span data-ttu-id="38fa4-122">Il valore del parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="38fa4-122">The parameter value is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="38fa4-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="38fa4-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                     | <span data-ttu-id="38fa4-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="38fa4-124">An unexpected error has occurred.</span></span><br/>                          |
| <dl> <span data-ttu-id="38fa4-125"><dt>Macchina virtuale \_ E \_ VMVIRTUALPC \_ \_ versione precedente</dt> <dt>0xA0040952</dt></span><span class="sxs-lookup"><span data-stu-id="38fa4-125"><dt>VM\_E\_VMVIRTUALPC\_OLDER\_VERSION</dt> <dt>0xA0040952</dt></span></span> </dl>     | <span data-ttu-id="38fa4-126">Sono installati sia Virtual PC 2007 che Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="38fa4-126">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <dl> <span data-ttu-id="38fa4-127"><dt>Macchina virtuale \_ E \_ altri \_ \_ software di virtualizzazione</dt> <dt>0xA0040953</dt></span><span class="sxs-lookup"><span data-stu-id="38fa4-127"><dt>VM\_E\_OTHER\_VIRTUALIZATION\_SOFTWARE</dt> <dt>0xA0040953</dt></span></span> </dl> | <span data-ttu-id="38fa4-128">È installato altro software di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="38fa4-128">Other virtualization software is installed.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="38fa4-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38fa4-129">Requirements</span></span>



| <span data-ttu-id="38fa4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="38fa4-130">Requirement</span></span> | <span data-ttu-id="38fa4-131">Valore</span><span class="sxs-lookup"><span data-stu-id="38fa4-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="38fa4-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38fa4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="38fa4-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="38fa4-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38fa4-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38fa4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="38fa4-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="38fa4-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="38fa4-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="38fa4-136">End of client support</span></span><br/>    | <span data-ttu-id="38fa4-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="38fa4-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="38fa4-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="38fa4-138">Product</span></span><br/>                  | <span data-ttu-id="38fa4-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="38fa4-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="38fa4-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38fa4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="38fa4-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="38fa4-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="38fa4-142">IID</span><span class="sxs-lookup"><span data-stu-id="38fa4-142">IID</span></span><br/>                      | <span data-ttu-id="38fa4-143">IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="38fa4-143">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="38fa4-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38fa4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38fa4-145">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="38fa4-145">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

