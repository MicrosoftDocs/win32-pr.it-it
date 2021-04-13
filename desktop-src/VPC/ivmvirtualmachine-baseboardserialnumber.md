---
title: Proprietà IVMVirtualMachine BaseBoardSerialNumber (VPCCOMInterfaces. h)
description: Numero di serie della lavagna di base.
ms.assetid: 374ad471-e0de-4e55-bab6-f7ddf3e5797f
keywords:
- Proprietà BaseBoardSerialNumber Virtual PC
- Proprietà BaseBoardSerialNumber Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà BaseBoardSerialNumber
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BaseBoardSerialNumber
- IVMVirtualMachine.get_BaseBoardSerialNumber
- IVMVirtualMachine.put_BaseBoardSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a6e239216eb5eadd492cb0a021d9f9c69610342
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400200"
---
# <a name="ivmvirtualmachinebaseboardserialnumber-property"></a><span data-ttu-id="964e5-106">Proprietà IVMVirtualMachine:: BaseBoardSerialNumber</span><span class="sxs-lookup"><span data-stu-id="964e5-106">IVMVirtualMachine::BaseBoardSerialNumber property</span></span>

<span data-ttu-id="964e5-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="964e5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="964e5-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="964e5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="964e5-109">Recupera e imposta il numero di serie della lavagna di base.</span><span class="sxs-lookup"><span data-stu-id="964e5-109">Retrieves and sets the base board serial number.</span></span>

<span data-ttu-id="964e5-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="964e5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="964e5-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="964e5-111">Syntax</span></span>


```C++
HRESULT put_BaseBoardSerialNumber(
  [in]          BSTR baseBoardSerialNumber
);

HRESULT get_BaseBoardSerialNumber(
  [out, retval] BSTR *baseBoardSerialNumber
);
```



## <a name="property-value"></a><span data-ttu-id="964e5-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="964e5-112">Property value</span></span>

<span data-ttu-id="964e5-113">Specifica il numero di serie della lavagna di base.</span><span class="sxs-lookup"><span data-stu-id="964e5-113">Specifies the base board serial number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="964e5-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="964e5-114">Error codes</span></span>



| <span data-ttu-id="964e5-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="964e5-115">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="964e5-116">Significato</span><span class="sxs-lookup"><span data-stu-id="964e5-116">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="964e5-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="964e5-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="964e5-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="964e5-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="964e5-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="964e5-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="964e5-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="964e5-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="964e5-121"><dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="964e5-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="964e5-122">Il parametro è maggiore di 32 caratteri, una stringa vuota o non valido.</span><span class="sxs-lookup"><span data-stu-id="964e5-122">The parameter is greater than 32 characters, an empty string, or not valid.</span></span><br/> |
| <dl> <span data-ttu-id="964e5-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="964e5-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="964e5-124">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="964e5-124">The configuration is unknown.</span></span><br/>                                               |
| <dl> <span data-ttu-id="964e5-125"><dt>Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="964e5-125"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="964e5-126">Lo stato della macchina virtuale è in esecuzione o salvato.</span><span class="sxs-lookup"><span data-stu-id="964e5-126">The virtual machine is in a running or saved state.</span></span><br/>                         |
| <dl> <span data-ttu-id="964e5-127"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="964e5-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="964e5-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="964e5-128">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="remarks"></a><span data-ttu-id="964e5-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="964e5-129">Remarks</span></span>

<span data-ttu-id="964e5-130">Questa proprietà non conterrà informazioni valide fino a quando la macchina virtuale non viene avviata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="964e5-130">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="964e5-131">Se viene letta prima dell'avvio iniziale, verrà restituita una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="964e5-131">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="964e5-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="964e5-132">Requirements</span></span>



| <span data-ttu-id="964e5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="964e5-133">Requirement</span></span> | <span data-ttu-id="964e5-134">Valore</span><span class="sxs-lookup"><span data-stu-id="964e5-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="964e5-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="964e5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="964e5-136">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="964e5-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="964e5-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="964e5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="964e5-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="964e5-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="964e5-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="964e5-139">End of client support</span></span><br/>    | <span data-ttu-id="964e5-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="964e5-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="964e5-141">Prodotto</span><span class="sxs-lookup"><span data-stu-id="964e5-141">Product</span></span><br/>                  | <span data-ttu-id="964e5-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="964e5-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="964e5-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="964e5-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="964e5-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="964e5-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="964e5-145">IID</span><span class="sxs-lookup"><span data-stu-id="964e5-145">IID</span></span><br/>                      | <span data-ttu-id="964e5-146">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="964e5-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="964e5-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="964e5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="964e5-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="964e5-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

