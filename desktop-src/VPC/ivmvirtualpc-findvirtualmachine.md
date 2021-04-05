---
title: Metodo IVMVirtualPC FindVirtualMachine (VPCCOMInterfaces. h)
description: Recupera un oggetto macchina virtuale che corrisponde alla configurazione richiesta.
ms.assetid: 1c73d6f7-5662-485e-a864-e8e48197f8e4
keywords:
- Metodo FindVirtualMachine Virtual PC
- Metodo FindVirtualMachine Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo FindVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e5702738e16fa7b4f4a263264b0574966d1fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120786"
---
# <a name="ivmvirtualpcfindvirtualmachine-method"></a><span data-ttu-id="8efe9-106">Metodo IVMVirtualPC:: FindVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8efe9-106">IVMVirtualPC::FindVirtualMachine method</span></span>

<span data-ttu-id="8efe9-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8efe9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8efe9-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8efe9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8efe9-109">Recupera un oggetto macchina virtuale che corrisponde alla configurazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="8efe9-109">Retrieves a virtual machine object that matches the requested configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="8efe9-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8efe9-110">Syntax</span></span>


```C++
HRESULT FindVirtualMachine(
  [in]          BSTR              configurationName,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="8efe9-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="8efe9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8efe9-112">*ConfigurationName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8efe9-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efe9-113">Nome della macchina virtuale da trovare.</span><span class="sxs-lookup"><span data-stu-id="8efe9-113">The name of the virtual machine to be found.</span></span>

</dd> <dt>

<span data-ttu-id="8efe9-114">*virtualmachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8efe9-114">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8efe9-115">Puntatore a un nuovo oggetto [**IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8efe9-115">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8efe9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8efe9-116">Return value</span></span>

<span data-ttu-id="8efe9-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="8efe9-117">This method can return one of these values.</span></span>



| <span data-ttu-id="8efe9-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="8efe9-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="8efe9-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8efe9-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8efe9-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8efe9-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="8efe9-121">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8efe9-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="8efe9-122"><dt>**S \_ FALSE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8efe9-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="8efe9-123">Impossibile trovare la configurazione specificata.</span><span class="sxs-lookup"><span data-stu-id="8efe9-123">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="8efe9-124"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8efe9-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="8efe9-125">Il parametro *ConfigurationName* non è valido o *virtualmachine* è **null**.</span><span class="sxs-lookup"><span data-stu-id="8efe9-125">The *configurationName* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="8efe9-126"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8efe9-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="8efe9-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="8efe9-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="8efe9-128"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="8efe9-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="8efe9-129">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="8efe9-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8efe9-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="8efe9-130">Remarks</span></span>

<span data-ttu-id="8efe9-131">I nomi delle macchine virtuali non fanno distinzione tra maiuscole e minuscole, ad esempio, "MyVM" e "MyVM" si riferiscono alla stessa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8efe9-131">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="8efe9-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8efe9-132">Requirements</span></span>



| <span data-ttu-id="8efe9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8efe9-133">Requirement</span></span> | <span data-ttu-id="8efe9-134">Valore</span><span class="sxs-lookup"><span data-stu-id="8efe9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8efe9-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8efe9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8efe9-136">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8efe9-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8efe9-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8efe9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8efe9-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8efe9-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8efe9-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8efe9-139">End of client support</span></span><br/>    | <span data-ttu-id="8efe9-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8efe9-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8efe9-141">Prodotto</span><span class="sxs-lookup"><span data-stu-id="8efe9-141">Product</span></span><br/>                  | <span data-ttu-id="8efe9-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8efe9-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8efe9-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8efe9-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="8efe9-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8efe9-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8efe9-145">IID</span><span class="sxs-lookup"><span data-stu-id="8efe9-145">IID</span></span><br/>                      | <span data-ttu-id="8efe9-146">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="8efe9-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8efe9-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8efe9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8efe9-148">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="8efe9-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

