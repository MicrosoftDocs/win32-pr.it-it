---
title: Proprietà IVMHostInfo NetworkAddresses (VPCCOMInterfaces. h)
description: Recupera una raccolta enumerabile di indirizzi TCP/IP nel computer host.
ms.assetid: 94716b82-8f35-4702-873d-64507d879dc3
keywords:
- Proprietà NetworkAddresses Virtual PC
- Proprietà NetworkAddresses Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà NetworkAddresses
topic_type:
- apiref
api_name:
- IVMHostInfo.NetworkAddresses
- IVMHostInfo.get_NetworkAddresses
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 824bedf8433c1025e1f4afc1e624c27606b8d0d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400204"
---
# <a name="ivmhostinfonetworkaddresses-property"></a><span data-ttu-id="68750-106">Proprietà IVMHostInfo:: NetworkAddresses</span><span class="sxs-lookup"><span data-stu-id="68750-106">IVMHostInfo::NetworkAddresses property</span></span>

<span data-ttu-id="68750-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="68750-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="68750-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="68750-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="68750-109">Recupera una raccolta enumerabile di indirizzi TCP/IP nel computer host.</span><span class="sxs-lookup"><span data-stu-id="68750-109">Retrieves an enumerable collection of TCP/IP addresses in the host machine.</span></span>

<span data-ttu-id="68750-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="68750-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="68750-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68750-111">Syntax</span></span>


```C++
HRESULT get_NetworkAddresses(
  [out, retval] VARIANT *hostAddresses
);
```



## <a name="property-value"></a><span data-ttu-id="68750-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="68750-112">Property value</span></span>

<span data-ttu-id="68750-113">Matrice di indirizzi TCP/IP, in notazione decimale punteggiata.</span><span class="sxs-lookup"><span data-stu-id="68750-113">An array of TCP/IP addresses, in dotted-decimal notation.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68750-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="68750-114">Error codes</span></span>



| <span data-ttu-id="68750-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="68750-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="68750-116">Significato</span><span class="sxs-lookup"><span data-stu-id="68750-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="68750-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="68750-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="68750-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="68750-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="68750-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="68750-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="68750-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="68750-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="68750-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="68750-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="68750-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="68750-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="68750-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68750-123">Requirements</span></span>



| <span data-ttu-id="68750-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="68750-124">Requirement</span></span> | <span data-ttu-id="68750-125">Valore</span><span class="sxs-lookup"><span data-stu-id="68750-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="68750-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68750-126">Minimum supported client</span></span><br/> | <span data-ttu-id="68750-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="68750-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68750-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68750-128">Minimum supported server</span></span><br/> | <span data-ttu-id="68750-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="68750-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="68750-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="68750-130">End of client support</span></span><br/>    | <span data-ttu-id="68750-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="68750-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="68750-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="68750-132">Product</span></span><br/>                  | <span data-ttu-id="68750-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="68750-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="68750-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68750-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="68750-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="68750-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="68750-136">IID</span><span class="sxs-lookup"><span data-stu-id="68750-136">IID</span></span><br/>                      | <span data-ttu-id="68750-137">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="68750-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="68750-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68750-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68750-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="68750-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

