---
title: Proprietà IVMVirtualMachine BIOSGUID (VPCCOMInterfaces. h)
description: GUID del BIOS.
ms.assetid: d866838d-31e9-41f1-be57-43e778b9db95
keywords:
- Proprietà BIOSGUID Virtual PC
- Proprietà BIOSGUID Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà BIOSGUID
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSGUID
- IVMVirtualMachine.get_BIOSGUID
- IVMVirtualMachine.put_BIOSGUID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10263e32ab71c2a5b9533b3dde6547f774d6b302
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873738"
---
# <a name="ivmvirtualmachinebiosguid-property"></a><span data-ttu-id="c8526-106">Proprietà IVMVirtualMachine:: BIOSGUID</span><span class="sxs-lookup"><span data-stu-id="c8526-106">IVMVirtualMachine::BIOSGUID property</span></span>

<span data-ttu-id="c8526-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c8526-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c8526-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c8526-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c8526-109">Recupera e imposta il GUID del BIOS.</span><span class="sxs-lookup"><span data-stu-id="c8526-109">Retrieves and sets the BIOS GUID.</span></span>

<span data-ttu-id="c8526-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c8526-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8526-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8526-111">Syntax</span></span>


```C++
HRESULT put_BIOSGUID(
  [in]          BSTR biosGUID
);

HRESULT get_BIOSGUID(
  [out, retval] BSTR *biosGUID
);
```



## <a name="property-value"></a><span data-ttu-id="c8526-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c8526-112">Property value</span></span>

<span data-ttu-id="c8526-113">Specifica il GUID del BIOS.</span><span class="sxs-lookup"><span data-stu-id="c8526-113">Specifies the BIOS GUID.</span></span> <span data-ttu-id="c8526-114">Includere le parentesi graffe sinistra e destra intorno alle cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="c8526-114">Include left and right braces around the hex digits.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8526-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c8526-115">Error codes</span></span>



| <span data-ttu-id="c8526-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="c8526-116">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="c8526-117">Significato</span><span class="sxs-lookup"><span data-stu-id="c8526-117">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="c8526-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8526-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="c8526-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c8526-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="c8526-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c8526-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="c8526-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="c8526-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="c8526-122"><dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c8526-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="c8526-123">Il parametro non è valido o è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="c8526-123">The parameter is not valid or is an empty string.</span></span><br/>   |
| <dl> <span data-ttu-id="c8526-124"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c8526-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="c8526-125">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="c8526-125">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="c8526-126"><dt>Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="c8526-126"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="c8526-127">Lo stato della macchina virtuale è in esecuzione o salvato.</span><span class="sxs-lookup"><span data-stu-id="c8526-127">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="c8526-128"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c8526-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="c8526-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="c8526-129">An unexpected error has occurred.</span></span><br/>                   |



## <a name="remarks"></a><span data-ttu-id="c8526-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8526-130">Remarks</span></span>

<span data-ttu-id="c8526-131">Questa proprietà non conterrà informazioni valide fino a quando la macchina virtuale non viene avviata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="c8526-131">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="c8526-132">Se viene letta prima dell'avvio iniziale, verrà restituita una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="c8526-132">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8526-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8526-133">Requirements</span></span>



| <span data-ttu-id="c8526-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8526-134">Requirement</span></span> | <span data-ttu-id="c8526-135">Valore</span><span class="sxs-lookup"><span data-stu-id="c8526-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8526-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8526-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c8526-137">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c8526-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8526-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8526-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c8526-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c8526-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c8526-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c8526-140">End of client support</span></span><br/>    | <span data-ttu-id="c8526-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8526-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c8526-142">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c8526-142">Product</span></span><br/>                  | <span data-ttu-id="c8526-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c8526-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c8526-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8526-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8526-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8526-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c8526-146">IID</span><span class="sxs-lookup"><span data-stu-id="c8526-146">IID</span></span><br/>                      | <span data-ttu-id="c8526-147">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="c8526-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c8526-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8526-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8526-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="c8526-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

