---
title: Proprietà Count IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Recupera il numero di dispositivi USB in questa raccolta.
ms.assetid: 8d17397b-4f4a-475d-99fe-4df0d74fe5a5
keywords:
- Conteggio proprietà PC virtuale
- Proprietà Count Virtual PC, interfaccia IVMUSBDeviceCollection
- Interfaccia IVMUSBDeviceCollection Virtual PC, proprietà Count
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Count
- IVMUSBDeviceCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a0c2146df70f0432a19d65daad44ba6f1ec372
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477050"
---
# <a name="ivmusbdevicecollectioncount-property"></a><span data-ttu-id="f3f6c-106">Proprietà IVMUSBDeviceCollection:: count</span><span class="sxs-lookup"><span data-stu-id="f3f6c-106">IVMUSBDeviceCollection::Count property</span></span>

<span data-ttu-id="f3f6c-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f3f6c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f3f6c-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f3f6c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f3f6c-109">Recupera il numero di dispositivi USB in questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="f3f6c-109">Retrieves the number of USB devices in this collection.</span></span>

<span data-ttu-id="f3f6c-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f3f6c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f6c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3f6c-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="f3f6c-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f3f6c-112">Property value</span></span>

<span data-ttu-id="f3f6c-113">Il numero di dispositivi USB.</span><span class="sxs-lookup"><span data-stu-id="f3f6c-113">The number of USB devices.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f3f6c-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f3f6c-114">Error codes</span></span>



| <span data-ttu-id="f3f6c-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="f3f6c-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f3f6c-116">Significato</span><span class="sxs-lookup"><span data-stu-id="f3f6c-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f3f6c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f3f6c-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f3f6c-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="f3f6c-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f3f6c-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="f3f6c-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="f3f6c-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f3f6c-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f3f6c-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f3f6c-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f3f6c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3f6c-123">Requirements</span></span>



| <span data-ttu-id="f3f6c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3f6c-124">Requirement</span></span> | <span data-ttu-id="f3f6c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f3f6c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f6c-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3f6c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f3f6c-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f3f6c-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f3f6c-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3f6c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f3f6c-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f3f6c-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f3f6c-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f3f6c-130">End of client support</span></span><br/>    | <span data-ttu-id="f3f6c-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3f6c-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f3f6c-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f3f6c-132">Product</span></span><br/>                  | <span data-ttu-id="f3f6c-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f3f6c-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f3f6c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3f6c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3f6c-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3f6c-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f3f6c-136">IID</span><span class="sxs-lookup"><span data-stu-id="f3f6c-136">IID</span></span><br/>                      | <span data-ttu-id="f3f6c-137">IID \_ IVMUSBDeviceCollection è definito come 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="f3f6c-137">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="f3f6c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3f6c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3f6c-139">**IVMUSBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="f3f6c-139">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

