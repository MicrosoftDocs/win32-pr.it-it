---
title: Proprietà IVMHostInfo I NetworkAdapter (VPCCOMInterfaces. h)
description: Recupera una raccolta enumerabile di schede di rete nel computer host.
ms.assetid: 17393d7a-c883-4d67-826b-83b886c0d7a6
keywords:
- Proprietà I NetworkAdapter Virtual PC
- Proprietà I NetworkAdapter Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà I NetworkAdapter
topic_type:
- apiref
api_name:
- IVMHostInfo.NetworkAdapters
- IVMHostInfo.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeff5c6d459fb8f6999f896c3c13fcd980bf70ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963725"
---
# <a name="ivmhostinfonetworkadapters-property"></a><span data-ttu-id="bf80e-106">Proprietà IVMHostInfo:: I NetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="bf80e-106">IVMHostInfo::NetworkAdapters property</span></span>

<span data-ttu-id="bf80e-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bf80e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bf80e-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bf80e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bf80e-109">Recupera una raccolta enumerabile di schede di rete nel computer host.</span><span class="sxs-lookup"><span data-stu-id="bf80e-109">Retrieves an enumerable collection of NICs in the host machine.</span></span>

<span data-ttu-id="bf80e-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bf80e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf80e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf80e-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] VARIANT *hostNICs
);
```



## <a name="property-value"></a><span data-ttu-id="bf80e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bf80e-112">Property value</span></span>

<span data-ttu-id="bf80e-113">Raccolta di schede di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="bf80e-113">A collection of network interface cards.</span></span> <span data-ttu-id="bf80e-114">Si tratta di una matrice di valori **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="bf80e-114">This is an array of **BSTR** values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bf80e-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="bf80e-115">Error codes</span></span>



| <span data-ttu-id="bf80e-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="bf80e-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="bf80e-117">Significato</span><span class="sxs-lookup"><span data-stu-id="bf80e-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bf80e-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bf80e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="bf80e-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="bf80e-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="bf80e-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bf80e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="bf80e-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="bf80e-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="bf80e-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bf80e-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="bf80e-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="bf80e-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bf80e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf80e-124">Requirements</span></span>



| <span data-ttu-id="bf80e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf80e-125">Requirement</span></span> | <span data-ttu-id="bf80e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="bf80e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf80e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf80e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bf80e-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bf80e-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf80e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf80e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bf80e-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bf80e-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bf80e-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bf80e-131">End of client support</span></span><br/>    | <span data-ttu-id="bf80e-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bf80e-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bf80e-133">Prodotto</span><span class="sxs-lookup"><span data-stu-id="bf80e-133">Product</span></span><br/>                  | <span data-ttu-id="bf80e-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bf80e-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bf80e-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf80e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf80e-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf80e-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bf80e-137">IID</span><span class="sxs-lookup"><span data-stu-id="bf80e-137">IID</span></span><br/>                      | <span data-ttu-id="bf80e-138">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="bf80e-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="bf80e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf80e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf80e-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="bf80e-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

