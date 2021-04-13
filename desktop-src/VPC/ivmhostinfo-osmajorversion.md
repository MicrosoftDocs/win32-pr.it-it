---
title: Proprietà IVMHostInfo OSMajorVersion (VPCCOMInterfaces. h)
description: Recupera la versione principale del sistema operativo in esecuzione nel computer host.
ms.assetid: d0b62d2d-532f-45c7-8622-67176b9b4a8f
keywords:
- Proprietà OSMajorVersion Virtual PC
- Proprietà OSMajorVersion Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, Proprietà OSMajorVersion
topic_type:
- apiref
api_name:
- IVMHostInfo.OSMajorVersion
- IVMHostInfo.get_OSMajorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf064744d90ede010a7e48e0e23e6a62a19eb4af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400202"
---
# <a name="ivmhostinfoosmajorversion-property"></a><span data-ttu-id="01a15-106">Proprietà IVMHostInfo:: OSMajorVersion</span><span class="sxs-lookup"><span data-stu-id="01a15-106">IVMHostInfo::OSMajorVersion property</span></span>

<span data-ttu-id="01a15-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="01a15-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="01a15-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="01a15-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="01a15-109">Recupera la versione principale del sistema operativo in esecuzione nel computer host.</span><span class="sxs-lookup"><span data-stu-id="01a15-109">Retrieves the major version of the operating system running on the host machine.</span></span>

<span data-ttu-id="01a15-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="01a15-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a15-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01a15-111">Syntax</span></span>


```C++
HRESULT get_OSMajorVersion(
  [out, retval] long *osMajorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="01a15-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="01a15-112">Property value</span></span>

<span data-ttu-id="01a15-113">La versione principale.</span><span class="sxs-lookup"><span data-stu-id="01a15-113">The major version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01a15-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="01a15-114">Error codes</span></span>



| <span data-ttu-id="01a15-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="01a15-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="01a15-116">Significato</span><span class="sxs-lookup"><span data-stu-id="01a15-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="01a15-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="01a15-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="01a15-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="01a15-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="01a15-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="01a15-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="01a15-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="01a15-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="01a15-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="01a15-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="01a15-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="01a15-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="01a15-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01a15-123">Requirements</span></span>



| <span data-ttu-id="01a15-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a15-124">Requirement</span></span> | <span data-ttu-id="01a15-125">Valore</span><span class="sxs-lookup"><span data-stu-id="01a15-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="01a15-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01a15-126">Minimum supported client</span></span><br/> | <span data-ttu-id="01a15-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="01a15-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01a15-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01a15-128">Minimum supported server</span></span><br/> | <span data-ttu-id="01a15-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="01a15-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="01a15-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="01a15-130">End of client support</span></span><br/>    | <span data-ttu-id="01a15-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="01a15-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="01a15-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="01a15-132">Product</span></span><br/>                  | <span data-ttu-id="01a15-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="01a15-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="01a15-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01a15-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="01a15-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="01a15-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="01a15-136">IID</span><span class="sxs-lookup"><span data-stu-id="01a15-136">IID</span></span><br/>                      | <span data-ttu-id="01a15-137">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="01a15-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="01a15-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01a15-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a15-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="01a15-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

