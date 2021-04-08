---
title: Proprietà SerialPort IVMHostInfo (VPCCOMInterfaces. h)
description: Recupera i nomi delle porte seriali associati alle porte seriali host.
ms.assetid: ef3bc474-19c9-4d91-8aa0-7619c89fec2d
keywords:
- Proprietà di SerialPort del PC virtuale
- Proprietà SerialPorts Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà SerialPorts
topic_type:
- apiref
api_name:
- IVMHostInfo.SerialPorts
- IVMHostInfo.get_SerialPorts
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8cb520ee82b53e93f9073b66d4dc4d69a2ef75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047805"
---
# <a name="ivmhostinfoserialports-property"></a><span data-ttu-id="d6044-106">Proprietà IVMHostInfo:: SerialPorts</span><span class="sxs-lookup"><span data-stu-id="d6044-106">IVMHostInfo::SerialPorts property</span></span>

<span data-ttu-id="d6044-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d6044-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d6044-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d6044-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d6044-109">Recupera i nomi delle porte seriali associati alle porte seriali host.</span><span class="sxs-lookup"><span data-stu-id="d6044-109">Retrieves the serial port names associated with host serial ports.</span></span>

<span data-ttu-id="d6044-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d6044-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6044-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6044-111">Syntax</span></span>


```C++
HRESULT get_SerialPorts(
  [out, retval] BSTR *serialPorts
);
```



## <a name="property-value"></a><span data-ttu-id="d6044-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d6044-112">Property value</span></span>

<span data-ttu-id="d6044-113">Elenco delimitato da punti e virgola dei nomi delle porte seriali.</span><span class="sxs-lookup"><span data-stu-id="d6044-113">A semicolon-delimited list of serial port names.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d6044-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d6044-114">Error codes</span></span>



| <span data-ttu-id="d6044-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="d6044-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d6044-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d6044-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d6044-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d6044-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d6044-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d6044-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d6044-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d6044-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d6044-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="d6044-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d6044-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d6044-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d6044-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d6044-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d6044-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6044-123">Requirements</span></span>



| <span data-ttu-id="d6044-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6044-124">Requirement</span></span> | <span data-ttu-id="d6044-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d6044-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6044-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6044-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d6044-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d6044-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d6044-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6044-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d6044-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d6044-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d6044-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d6044-130">End of client support</span></span><br/>    | <span data-ttu-id="d6044-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d6044-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d6044-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d6044-132">Product</span></span><br/>                  | <span data-ttu-id="d6044-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d6044-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d6044-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6044-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6044-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6044-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d6044-136">IID</span><span class="sxs-lookup"><span data-stu-id="d6044-136">IID</span></span><br/>                      | <span data-ttu-id="d6044-137">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="d6044-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="d6044-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6044-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6044-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="d6044-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

