---
title: Proprietà IVMVirtualMachine ChassisSerialNumber (VPCCOMInterfaces. h)
description: Numero di serie dello chassis.
ms.assetid: 03e02e6e-6819-4052-a0e0-9167eb5fdf4b
keywords:
- Proprietà ChassisSerialNumber Virtual PC
- Proprietà ChassisSerialNumber Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà ChassisSerialNumber
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisSerialNumber
- IVMVirtualMachine.get_ChassisSerialNumber
- IVMVirtualMachine.put_ChassisSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00edbac12248f624ac06d1f7b88c3782c3f5a3df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048459"
---
# <a name="ivmvirtualmachinechassisserialnumber-property"></a><span data-ttu-id="b3517-106">Proprietà IVMVirtualMachine:: ChassisSerialNumber</span><span class="sxs-lookup"><span data-stu-id="b3517-106">IVMVirtualMachine::ChassisSerialNumber property</span></span>

<span data-ttu-id="b3517-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b3517-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b3517-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b3517-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b3517-109">Recupera e imposta il numero di serie dello chassis.</span><span class="sxs-lookup"><span data-stu-id="b3517-109">Retrieves and sets the chassis serial number.</span></span>

<span data-ttu-id="b3517-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b3517-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3517-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3517-111">Syntax</span></span>


```C++
HRESULT put_ChassisSerialNumber(
  [in]          BSTR chasisSerialNumber
);

HRESULT get_ChassisSerialNumber(
  [out, retval] BSTR *chassisSerialNumber
);
```



## <a name="property-value"></a><span data-ttu-id="b3517-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b3517-112">Property value</span></span>

<span data-ttu-id="b3517-113">Specifica il numero di serie dello chassis.</span><span class="sxs-lookup"><span data-stu-id="b3517-113">Specifies the chassis serial number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b3517-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b3517-114">Error codes</span></span>



| <span data-ttu-id="b3517-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="b3517-115">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="b3517-116">Significato</span><span class="sxs-lookup"><span data-stu-id="b3517-116">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3517-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b3517-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="b3517-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b3517-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b3517-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b3517-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="b3517-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="b3517-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="b3517-121"><dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b3517-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="b3517-122">Il parametro è maggiore di 32 caratteri, una stringa vuota o non valido.</span><span class="sxs-lookup"><span data-stu-id="b3517-122">The parameter is greater than 32 characters, an empty string, or not valid.</span></span><br/> |
| <dl> <span data-ttu-id="b3517-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b3517-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="b3517-124">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="b3517-124">The configuration is unknown.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b3517-125"><dt>Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="b3517-125"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="b3517-126">Lo stato della macchina virtuale è in esecuzione o salvato.</span><span class="sxs-lookup"><span data-stu-id="b3517-126">The virtual machine is in a running or saved state.</span></span><br/>                         |
| <dl> <span data-ttu-id="b3517-127"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b3517-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="b3517-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="b3517-128">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="remarks"></a><span data-ttu-id="b3517-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3517-129">Remarks</span></span>

<span data-ttu-id="b3517-130">Questa proprietà non conterrà informazioni valide fino a quando la macchina virtuale non viene avviata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="b3517-130">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="b3517-131">Se viene letta prima dell'avvio iniziale, verrà restituita una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="b3517-131">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3517-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3517-132">Requirements</span></span>



| <span data-ttu-id="b3517-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3517-133">Requirement</span></span> | <span data-ttu-id="b3517-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b3517-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3517-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3517-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b3517-136">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b3517-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3517-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3517-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b3517-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b3517-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b3517-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b3517-139">End of client support</span></span><br/>    | <span data-ttu-id="b3517-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b3517-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b3517-141">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b3517-141">Product</span></span><br/>                  | <span data-ttu-id="b3517-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b3517-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b3517-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3517-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3517-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3517-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b3517-145">IID</span><span class="sxs-lookup"><span data-stu-id="b3517-145">IID</span></span><br/>                      | <span data-ttu-id="b3517-146">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b3517-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b3517-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3517-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3517-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="b3517-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

