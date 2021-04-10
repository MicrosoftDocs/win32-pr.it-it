---
title: Proprietà IVMHostInfo OSVersionString (VPCCOMInterfaces. h)
description: Recupera la versione del sistema operativo in esecuzione nel computer host.
ms.assetid: ac3a162a-d3e6-420d-ac26-d77f1c9646a6
keywords:
- Proprietà OSVersionString Virtual PC
- Proprietà OSVersionString Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà OSVersionString
topic_type:
- apiref
api_name:
- IVMHostInfo.OSVersionString
- IVMHostInfo.get_OSVersionString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a84017c753edc12dfddc60c9524bc971d7e53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048684"
---
# <a name="ivmhostinfoosversionstring-property"></a><span data-ttu-id="c07ce-106">Proprietà IVMHostInfo:: OSVersionString</span><span class="sxs-lookup"><span data-stu-id="c07ce-106">IVMHostInfo::OSVersionString property</span></span>

<span data-ttu-id="c07ce-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c07ce-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c07ce-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c07ce-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c07ce-109">Recupera la versione del sistema operativo in esecuzione nel computer host.</span><span class="sxs-lookup"><span data-stu-id="c07ce-109">Retrieves the operating system version running on the host machine.</span></span>

<span data-ttu-id="c07ce-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c07ce-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c07ce-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c07ce-111">Syntax</span></span>


```C++
HRESULT get_OSVersionString(
  [out, retval] BSTR *OSVersion
);
```



## <a name="property-value"></a><span data-ttu-id="c07ce-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c07ce-112">Property value</span></span>

<span data-ttu-id="c07ce-113">Versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c07ce-113">The operating system version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c07ce-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c07ce-114">Error codes</span></span>



| <span data-ttu-id="c07ce-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="c07ce-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c07ce-116">Significato</span><span class="sxs-lookup"><span data-stu-id="c07ce-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c07ce-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c07ce-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c07ce-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c07ce-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c07ce-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c07ce-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c07ce-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="c07ce-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c07ce-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c07ce-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c07ce-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="c07ce-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c07ce-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c07ce-123">Requirements</span></span>



| <span data-ttu-id="c07ce-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c07ce-124">Requirement</span></span> | <span data-ttu-id="c07ce-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c07ce-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c07ce-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c07ce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c07ce-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c07ce-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c07ce-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c07ce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c07ce-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c07ce-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c07ce-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c07ce-130">End of client support</span></span><br/>    | <span data-ttu-id="c07ce-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c07ce-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c07ce-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c07ce-132">Product</span></span><br/>                  | <span data-ttu-id="c07ce-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c07ce-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c07ce-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c07ce-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c07ce-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c07ce-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c07ce-136">IID</span><span class="sxs-lookup"><span data-stu-id="c07ce-136">IID</span></span><br/>                      | <span data-ttu-id="c07ce-137">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="c07ce-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="c07ce-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c07ce-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c07ce-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="c07ce-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

