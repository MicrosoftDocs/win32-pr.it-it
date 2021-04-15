---
title: Proprietà Version IVMVirtualPC (VPCCOMInterfaces. h)
description: Recupera la versione di questa istanza di Windows Virtual PC.
ms.assetid: efcd5e71-8752-45a2-8138-4bc214762f39
keywords:
- Proprietà versione Virtual PC
- Proprietà Version Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà Version
topic_type:
- apiref
api_name:
- IVMVirtualPC.Version
- IVMVirtualPC.get_Version
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0dc84fd714c50c0a0adb3084603aeea2419d3ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479222"
---
# <a name="ivmvirtualpcversion-property"></a><span data-ttu-id="a839d-106">Proprietà IVMVirtualPC:: Version</span><span class="sxs-lookup"><span data-stu-id="a839d-106">IVMVirtualPC::Version property</span></span>

<span data-ttu-id="a839d-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a839d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a839d-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a839d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a839d-109">Recupera la versione di questa istanza di Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="a839d-109">Retrieves the version of this instance of Windows Virtual PC.</span></span>

<span data-ttu-id="a839d-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a839d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a839d-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a839d-111">Syntax</span></span>


```C++
HRESULT get_Version(
  [out, retval] BSTR *version
);
```



## <a name="property-value"></a><span data-ttu-id="a839d-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a839d-112">Property value</span></span>

<span data-ttu-id="a839d-113">Versione.</span><span class="sxs-lookup"><span data-stu-id="a839d-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a839d-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a839d-114">Error codes</span></span>



| <span data-ttu-id="a839d-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="a839d-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="a839d-116">Significato</span><span class="sxs-lookup"><span data-stu-id="a839d-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a839d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a839d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="a839d-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a839d-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a839d-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a839d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="a839d-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="a839d-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="a839d-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a839d-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="a839d-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a839d-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="a839d-123"><dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="a839d-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="a839d-124">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="a839d-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a839d-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="a839d-125">Remarks</span></span>

<span data-ttu-id="a839d-126">Le informazioni sulla versione di Windows Virtual PC vengono restituite come valore stringa con il formato seguente: "*v*. *s*. *BBB*. *Tee*", dove *v* è il numero di versione principale, *s* è il numero di versione secondario, *BBB* è il numero di build, *t* è il tipo di compilazione (0 = Release Build) ed *EE* è l'edizione server (se = Standard Edition, EE = Enterprise Edition).</span><span class="sxs-lookup"><span data-stu-id="a839d-126">The Windows Virtual PC version information is returned as a string value with the following format: "*v*.*s*.*bbb*.*tee*", where *v* is the major version number, *s* is the minor version number, *bbb* is the build number, *t* is the build type (0 = release build), and *ee* is the server edition (SE = Standard Edition, EE = Enterprise Edition).</span></span>

## <a name="requirements"></a><span data-ttu-id="a839d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a839d-127">Requirements</span></span>



| <span data-ttu-id="a839d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a839d-128">Requirement</span></span> | <span data-ttu-id="a839d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a839d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a839d-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a839d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a839d-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a839d-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a839d-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a839d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a839d-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a839d-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a839d-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a839d-134">End of client support</span></span><br/>    | <span data-ttu-id="a839d-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a839d-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a839d-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a839d-136">Product</span></span><br/>                  | <span data-ttu-id="a839d-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a839d-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a839d-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a839d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a839d-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a839d-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a839d-140">IID</span><span class="sxs-lookup"><span data-stu-id="a839d-140">IID</span></span><br/>                      | <span data-ttu-id="a839d-141">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="a839d-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a839d-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a839d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a839d-143">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="a839d-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

