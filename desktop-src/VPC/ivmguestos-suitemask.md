---
title: Proprietà IVMGuestOS SuiteMask (VPCCOMInterfaces. h)
description: Recupera il SuiteMask del sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- Proprietà SuiteMask Virtual PC
- Proprietà SuiteMask Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà SuiteMask
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 348384dd729c5c7e63a45fcb8b3f05d0189a7fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743591"
---
# <a name="ivmguestossuitemask-property"></a><span data-ttu-id="0984f-106">Proprietà IVMGuestOS:: SuiteMask</span><span class="sxs-lookup"><span data-stu-id="0984f-106">IVMGuestOS::SuiteMask property</span></span>

<span data-ttu-id="0984f-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0984f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0984f-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0984f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0984f-109">Recupera il SuiteMask del sistema operativo guest in esecuzione nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0984f-109">Retrieves the SuiteMask of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="0984f-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0984f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0984f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0984f-111">Syntax</span></span>


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a><span data-ttu-id="0984f-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0984f-112">Property value</span></span>

<span data-ttu-id="0984f-113">Maschera del gruppo.</span><span class="sxs-lookup"><span data-stu-id="0984f-113">The suite mask.</span></span> <span data-ttu-id="0984f-114">Sono supportati i valori stringa seguenti.</span><span class="sxs-lookup"><span data-stu-id="0984f-114">The following string values are supported.</span></span>



| <span data-ttu-id="0984f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0984f-115">Value</span></span>                                                                                   | <span data-ttu-id="0984f-116">Significato</span><span class="sxs-lookup"><span data-stu-id="0984f-116">Meaning</span></span>                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0984f-117"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-117"><dt>"0x00000004"</dt></span></span> </dl> | <span data-ttu-id="0984f-118">Microsoft BackOffice Components è installato.</span><span class="sxs-lookup"><span data-stu-id="0984f-118">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="0984f-119"><dt>"0x00000400"</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-119"><dt>"0x00000400"</dt></span></span> </dl> | <span data-ttu-id="0984f-120">Windows Server 2003, Web Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="0984f-120">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="0984f-121"><dt>"0x00004000"</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-121"><dt>"0x00004000"</dt></span></span> </dl> | <span data-ttu-id="0984f-122">Windows Server 2003, Compute Cluster Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="0984f-122">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="0984f-123"><dt>"0x00000080"</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-123"><dt>"0x00000080"</dt></span></span> </dl> | <span data-ttu-id="0984f-124">Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server è installato.</span><span class="sxs-lookup"><span data-stu-id="0984f-124">Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/> |
| <dl> <span data-ttu-id="0984f-125"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-125"><dt>"0x00000002"</dt></span></span> </dl> | <span data-ttu-id="0984f-126">Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows 2000 Advanced Server è installato.</span><span class="sxs-lookup"><span data-stu-id="0984f-126">Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span><br/>   |
| <dl> <span data-ttu-id="0984f-127"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-127"><dt>"0x00000040"</dt></span></span> </dl> | <span data-ttu-id="0984f-128">Windows XP Embedded è installato.</span><span class="sxs-lookup"><span data-stu-id="0984f-128">Windows XP Embedded is installed.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="0984f-129"><dt>"0x00000200"</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-129"><dt>"0x00000200"</dt></span></span> </dl> | <span data-ttu-id="0984f-130">Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="0984f-130">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="0984f-131"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-131"><dt>"0x00000100"</dt></span></span> </dl> | <span data-ttu-id="0984f-132">Desktop remoto è supportato, ma è supportata una sola sessione interattiva.</span><span class="sxs-lookup"><span data-stu-id="0984f-132">Remote Desktop is supported, but only one interactive session is supported.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="0984f-133"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-133"><dt>"0x00000001"</dt></span></span> </dl> | <span data-ttu-id="0984f-134">Microsoft Small Business Server è stato installato nel sistema, ma potrebbe essere stato aggiornato a un'altra versione di Windows.</span><span class="sxs-lookup"><span data-stu-id="0984f-134">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span><br/>                                 |
| <dl> <span data-ttu-id="0984f-135"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-135"><dt>"0x00000020"</dt></span></span> </dl> | <span data-ttu-id="0984f-136">Microsoft Small Business Server viene installato con la licenza client restrittiva in vigore.</span><span class="sxs-lookup"><span data-stu-id="0984f-136">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="0984f-137"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-137"><dt>"0x00002000"</dt></span></span> </dl> | <span data-ttu-id="0984f-138">Windows Storage Server 2003 R2 o Windows Storage Server 2003 è installato.</span><span class="sxs-lookup"><span data-stu-id="0984f-138">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="0984f-139"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-139"><dt>"0x00000010"</dt></span></span> </dl> | <span data-ttu-id="0984f-140">Servizi Desktop remoto è installato.</span><span class="sxs-lookup"><span data-stu-id="0984f-140">Remote Desktop Services is installed.</span></span> <span data-ttu-id="0984f-141">Questo valore è sempre impostato.</span><span class="sxs-lookup"><span data-stu-id="0984f-141">This value is always set.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0984f-142"><dt>"0x00008000"</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-142"><dt>"0x00008000"</dt></span></span> </dl> | <span data-ttu-id="0984f-143">Windows Home Server è installato.</span><span class="sxs-lookup"><span data-stu-id="0984f-143">Windows Home Server is installed.</span></span><br/>                                                                                                                           |



 

## <a name="error-codes"></a><span data-ttu-id="0984f-144">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0984f-144">Error codes</span></span>



| <span data-ttu-id="0984f-145">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="0984f-145">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="0984f-146">Significato</span><span class="sxs-lookup"><span data-stu-id="0984f-146">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0984f-147"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-147"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="0984f-148">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0984f-148">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="0984f-149"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-149"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="0984f-150">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="0984f-150">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="0984f-151"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-151"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="0984f-152">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0984f-152">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="0984f-153"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-153"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="0984f-154">I componenti di integrazione non sono installati in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0984f-154">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="0984f-155"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0984f-155"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="0984f-156">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="0984f-156">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="0984f-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0984f-157">Requirements</span></span>



| <span data-ttu-id="0984f-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="0984f-158">Requirement</span></span> | <span data-ttu-id="0984f-159">Valore</span><span class="sxs-lookup"><span data-stu-id="0984f-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0984f-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0984f-160">Minimum supported client</span></span><br/> | <span data-ttu-id="0984f-161">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0984f-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0984f-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0984f-162">Minimum supported server</span></span><br/> | <span data-ttu-id="0984f-163">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0984f-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0984f-164">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0984f-164">End of client support</span></span><br/>    | <span data-ttu-id="0984f-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0984f-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0984f-166">Prodotto</span><span class="sxs-lookup"><span data-stu-id="0984f-166">Product</span></span><br/>                  | <span data-ttu-id="0984f-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0984f-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0984f-168">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0984f-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="0984f-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0984f-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0984f-170">IID</span><span class="sxs-lookup"><span data-stu-id="0984f-170">IID</span></span><br/>                      | <span data-ttu-id="0984f-171">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="0984f-171">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="0984f-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0984f-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0984f-173">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="0984f-173">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

