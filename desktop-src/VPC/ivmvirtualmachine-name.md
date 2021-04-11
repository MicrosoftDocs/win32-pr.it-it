---
title: Proprietà Name di IVMVirtualMachine (VPCCOMInterfaces. h)
description: Nome della configurazione della macchina virtuale.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Nome proprietà PC virtuale
- Proprietà nome Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà Name
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c163173a778d8103922fd8c8948ab5156f512ed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120051"
---
# <a name="ivmvirtualmachinename-property"></a><span data-ttu-id="f5fb2-106">Proprietà IVMVirtualMachine:: Name</span><span class="sxs-lookup"><span data-stu-id="f5fb2-106">IVMVirtualMachine::Name property</span></span>

<span data-ttu-id="f5fb2-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f5fb2-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f5fb2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f5fb2-109">Recupera e imposta il nome della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-109">Retrieves and sets the name of the virtual machine configuration.</span></span>

<span data-ttu-id="f5fb2-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5fb2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5fb2-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a><span data-ttu-id="f5fb2-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f5fb2-112">Property value</span></span>

<span data-ttu-id="f5fb2-113">Specifica il nome della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-113">Specifies the name of the virtual machine configuration.</span></span> <span data-ttu-id="f5fb2-114">La lunghezza del nome non può superare i 80 caratteri e la lunghezza totale del percorso completo che include il file di configurazione del nome della macchina virtuale non può essere maggiore di **Max \_ path** (260) caratteri.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-114">The length of the name cannot be more than 80 characters and the total length of the fully qualified path that includes the virtual machine name configuration file cannot be more than **MAX\_PATH** (260) characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f5fb2-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f5fb2-115">Error codes</span></span>



| <span data-ttu-id="f5fb2-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="f5fb2-116">Name/value</span></span>                                                                                                                                                                    | <span data-ttu-id="f5fb2-117">Significato</span><span class="sxs-lookup"><span data-stu-id="f5fb2-117">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5fb2-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5fb2-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                       | <span data-ttu-id="f5fb2-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f5fb2-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f5fb2-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                         | <span data-ttu-id="f5fb2-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="f5fb2-122"><dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f5fb2-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                      | <span data-ttu-id="f5fb2-123">Il parametro non è valido o è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-123">The parameter is not valid or is an empty string.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f5fb2-124"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f5fb2-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                 | <span data-ttu-id="f5fb2-125">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-125">The configuration is unknown.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f5fb2-126"><dt>Macchina virtuale \_ 0xA0040302 \_ virtuale E pref \_ VM \_ attiva</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f5fb2-126"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl>            | <span data-ttu-id="f5fb2-127">La macchina virtuale è in esecuzione o salvata.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-127">The virtual machine is running or saved.</span></span><br/>                                             |
| <dl> <span data-ttu-id="f5fb2-128"><dt>Macchina virtuale \_ E \_ config \_ senza \_ nome</dt> <dt>0xA0040400</dt></span><span class="sxs-lookup"><span data-stu-id="f5fb2-128"><dt>VM\_E\_CONFIG\_NO\_NAME</dt> <dt>0xA0040400</dt></span></span> </dl>            | <span data-ttu-id="f5fb2-129">Il parametro *virtualMachineName* è vuoto.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-129">The *virtualMachineName* parameter is empty.</span></span><br/>                                         |
| <dl> <span data-ttu-id="f5fb2-130"><dt>Macchina virtuale \_ Nome di configurazione di E \_ \_ \_ troppo \_ lungo</dt> <dt>0xA00400401</dt></span><span class="sxs-lookup"><span data-stu-id="f5fb2-130"><dt>VM\_E\_CONFIG\_NAME\_TOO\_LONG</dt> <dt>0xA00400401</dt></span></span> </dl>    | <span data-ttu-id="f5fb2-131">Il parametro contiene troppi caratteri.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-131">The parameter contains too many characters.</span></span><br/>                                          |
| <dl> <span data-ttu-id="f5fb2-132"><dt>Macchina virtuale \_ Il \_ nome di configurazione E 0xA0040402 \_ non è \_ valido \_ </dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f5fb2-132"><dt>VM\_E\_CONFIG\_NAME\_INVALID\_CHAR</dt> <dt>0xA0040402</dt></span></span> </dl> | <span data-ttu-id="f5fb2-133">Il parametro contiene uno dei seguenti caratteri non validi \* : "?: <>/ \| \\ " ".</span><span class="sxs-lookup"><span data-stu-id="f5fb2-133">The parameter contains one of the following invalid characters "\*?:<>/\|\\"".</span></span><br/> |
| <dl> <span data-ttu-id="f5fb2-134"><dt>Macchina virtuale \_ E \_ config \_ \_ nome duplicato</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="f5fb2-134"><dt>VM\_E\_CONFIG\_DUPLICATE\_NAME</dt> <dt>0xA0040403</dt></span></span> </dl>     | <span data-ttu-id="f5fb2-135">Il nome specificato esiste già come nome di un'altra macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-135">The specified name already exists as the name of another virtual machine.</span></span><br/>            |
| <dl> <span data-ttu-id="f5fb2-136"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f5fb2-136"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                 | <span data-ttu-id="f5fb2-137">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-137">An unexpected error has occurred.</span></span><br/>                                                    |



## <a name="remarks"></a><span data-ttu-id="f5fb2-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5fb2-138">Remarks</span></span>

<span data-ttu-id="f5fb2-139">I nomi delle macchine virtuali non fanno distinzione tra maiuscole e minuscole, ad esempio "MyVM" e "MyVM" fanno riferimento alla stessa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-139">Virtual machine names are case-insensitive, e.g. "MyVM" and "myvm" refer to the same virtual machine.</span></span> <span data-ttu-id="f5fb2-140">Si tratta della proprietà predefinita per [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="f5fb2-140">This is the default property for [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="f5fb2-141">Se VPC.exe è in esecuzione e la macchina virtuale viene salvata, l'impostazione della proprietà **Name** avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-141">If VPC.exe is running and the VM is saved then setting the **Name** property will not succeed.</span></span> <span data-ttu-id="f5fb2-142">Se VPC.exe non è in esecuzione e la macchina virtuale viene salvata, l'impostazione della proprietà **Name** avrà esito positivo al successivo avvio di VPC.exe.</span><span class="sxs-lookup"><span data-stu-id="f5fb2-142">If VPC.exe is not running and the VM is saved then setting the **Name** property will succeed when VPC.exe is next started.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5fb2-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5fb2-143">Requirements</span></span>



| <span data-ttu-id="f5fb2-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5fb2-144">Requirement</span></span> | <span data-ttu-id="f5fb2-145">Valore</span><span class="sxs-lookup"><span data-stu-id="f5fb2-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5fb2-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5fb2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f5fb2-147">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f5fb2-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5fb2-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5fb2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f5fb2-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f5fb2-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f5fb2-150">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f5fb2-150">End of client support</span></span><br/>    | <span data-ttu-id="f5fb2-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5fb2-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f5fb2-152">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f5fb2-152">Product</span></span><br/>                  | <span data-ttu-id="f5fb2-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f5fb2-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f5fb2-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5fb2-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5fb2-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5fb2-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f5fb2-156">IID</span><span class="sxs-lookup"><span data-stu-id="f5fb2-156">IID</span></span><br/>                      | <span data-ttu-id="f5fb2-157">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="f5fb2-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="f5fb2-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5fb2-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5fb2-159">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="f5fb2-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

