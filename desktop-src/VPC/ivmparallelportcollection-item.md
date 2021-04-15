---
title: Proprietà Item di IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Recupera l'oggetto porta parallela corrispondente all'indice specificato.
ms.assetid: f67a4224-ca96-4d68-9f0f-4977ffff859e
keywords:
- Proprietà elemento Virtual PC
- Proprietà elemento Virtual PC, interfaccia IVMParallelPortCollection
- Interfaccia IVMParallelPortCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Item
- IVMParallelPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa450f1859db8af6ed884b37fc693fc4fb1990f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478694"
---
# <a name="ivmparallelportcollectionitem-property"></a><span data-ttu-id="022b2-106">Proprietà IVMParallelPortCollection:: Item</span><span class="sxs-lookup"><span data-stu-id="022b2-106">IVMParallelPortCollection::Item property</span></span>

<span data-ttu-id="022b2-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="022b2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="022b2-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="022b2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="022b2-109">Recupera l'oggetto porta parallela corrispondente all'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="022b2-109">Retrieves the parallel port object that corresponds to the specified index.</span></span>

<span data-ttu-id="022b2-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="022b2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="022b2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="022b2-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long            index,
  [out, retval] IVMParallelPort **vmParallelPort
);
```



## <a name="property-value"></a><span data-ttu-id="022b2-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="022b2-112">Property value</span></span>

<span data-ttu-id="022b2-113">Oggetto [**IVMParallelPort**](ivmparallelport.md) .</span><span class="sxs-lookup"><span data-stu-id="022b2-113">The [**IVMParallelPort**](ivmparallelport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="022b2-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="022b2-114">Error codes</span></span>



| <span data-ttu-id="022b2-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="022b2-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="022b2-116">Significato</span><span class="sxs-lookup"><span data-stu-id="022b2-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="022b2-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="022b2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="022b2-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="022b2-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="022b2-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="022b2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="022b2-120">Il parametro *vmParallelPort* è **null**.</span><span class="sxs-lookup"><span data-stu-id="022b2-120">The *vmParallelPort* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="022b2-121"><dt>Disp \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="022b2-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="022b2-122">L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="022b2-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="022b2-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="022b2-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="022b2-124">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="022b2-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="022b2-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="022b2-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="022b2-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="022b2-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="022b2-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="022b2-127">Requirements</span></span>



| <span data-ttu-id="022b2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="022b2-128">Requirement</span></span> | <span data-ttu-id="022b2-129">Valore</span><span class="sxs-lookup"><span data-stu-id="022b2-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="022b2-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="022b2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="022b2-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="022b2-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="022b2-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="022b2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="022b2-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="022b2-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="022b2-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="022b2-134">End of client support</span></span><br/>    | <span data-ttu-id="022b2-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="022b2-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="022b2-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="022b2-136">Product</span></span><br/>                  | <span data-ttu-id="022b2-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="022b2-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="022b2-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="022b2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="022b2-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="022b2-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="022b2-140">IID</span><span class="sxs-lookup"><span data-stu-id="022b2-140">IID</span></span><br/>                      | <span data-ttu-id="022b2-141">IID \_ IVMParallelPortCollection è definito come 27c3e036-198f-430C-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="022b2-141">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="022b2-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="022b2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022b2-143">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="022b2-143">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="022b2-144">**IVMParallelPortCollection**</span><span class="sxs-lookup"><span data-stu-id="022b2-144">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

