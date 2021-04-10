---
title: Proprietà IVMDisplay VideoMode (VPCCOMInterfaces. h)
description: Recupera la modalità video corrente.
ms.assetid: e5a090c2-f7e6-4b85-8729-64d2ff68fcf3
keywords:
- Proprietà VideoMode Virtual PC
- Proprietà VideoMode Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, proprietà VideoMode
topic_type:
- apiref
api_name:
- IVMDisplay.VideoMode
- IVMDisplay.get_VideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164a658766cb8973a7c1ac403756ee888abab1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964173"
---
# <a name="ivmdisplayvideomode-property"></a><span data-ttu-id="36f59-106">Proprietà IVMDisplay:: VideoMode</span><span class="sxs-lookup"><span data-stu-id="36f59-106">IVMDisplay::VideoMode property</span></span>

<span data-ttu-id="36f59-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="36f59-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="36f59-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="36f59-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="36f59-109">Recupera la modalità video corrente.</span><span class="sxs-lookup"><span data-stu-id="36f59-109">Retrieves the current video mode.</span></span>

<span data-ttu-id="36f59-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="36f59-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f59-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36f59-111">Syntax</span></span>


```C++
HRESULT get_VideoMode(
  [out, retval] VMDisplayVideoMode *videoMode
);
```



## <a name="property-value"></a><span data-ttu-id="36f59-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="36f59-112">Property value</span></span>

<span data-ttu-id="36f59-113">Modalità video corrente del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="36f59-113">The current video mode of the guest operating system.</span></span> <span data-ttu-id="36f59-114">Per un elenco di valori, vedere [**VMDisplayVideoMode**](vmdisplayvideomode.md).</span><span class="sxs-lookup"><span data-stu-id="36f59-114">For a list of values, see [**VMDisplayVideoMode**](vmdisplayvideomode.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="36f59-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="36f59-115">Error codes</span></span>



| <span data-ttu-id="36f59-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="36f59-116">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="36f59-117">Significato</span><span class="sxs-lookup"><span data-stu-id="36f59-117">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36f59-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="36f59-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="36f59-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="36f59-119">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="36f59-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="36f59-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="36f59-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="36f59-121">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="36f59-122"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="36f59-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="36f59-123">Per questa operazione è necessario che la macchina virtuale sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="36f59-123">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="36f59-124"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="36f59-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="36f59-125">La macchina virtuale non è valida o non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="36f59-125">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="36f59-126"><dt>Macchina virtuale \_ E \_ Nessuna \_ visualizzazione</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="36f59-126"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="36f59-127">Non è possibile individuare una visualizzazione valida per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="36f59-127">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="36f59-128"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="36f59-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="36f59-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="36f59-129">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="36f59-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36f59-130">Requirements</span></span>



| <span data-ttu-id="36f59-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="36f59-131">Requirement</span></span> | <span data-ttu-id="36f59-132">Valore</span><span class="sxs-lookup"><span data-stu-id="36f59-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="36f59-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36f59-133">Minimum supported client</span></span><br/> | <span data-ttu-id="36f59-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="36f59-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="36f59-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36f59-135">Minimum supported server</span></span><br/> | <span data-ttu-id="36f59-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="36f59-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="36f59-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="36f59-137">End of client support</span></span><br/>    | <span data-ttu-id="36f59-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="36f59-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="36f59-139">Prodotto</span><span class="sxs-lookup"><span data-stu-id="36f59-139">Product</span></span><br/>                  | <span data-ttu-id="36f59-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="36f59-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="36f59-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36f59-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="36f59-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="36f59-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="36f59-143">IID</span><span class="sxs-lookup"><span data-stu-id="36f59-143">IID</span></span><br/>                      | <span data-ttu-id="36f59-144">IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="36f59-144">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="36f59-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36f59-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f59-146">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="36f59-146">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

