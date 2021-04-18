---
title: Metodo IVMVirtualPC RegisterVirtualMachine (VPCCOMInterfaces. h)
description: Registra una configurazione di macchina virtuale esistente e recupera l'oggetto macchina virtuale.
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- Metodo RegisterVirtualMachine Virtual PC
- Metodo RegisterVirtualMachine Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo RegisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.RegisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cc1e27a657eaad70aeec81c0216d1e707fa36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302411"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a><span data-ttu-id="db897-106">Metodo IVMVirtualPC:: RegisterVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="db897-106">IVMVirtualPC::RegisterVirtualMachine method</span></span>

<span data-ttu-id="db897-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="db897-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="db897-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="db897-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="db897-109">Registra una configurazione di macchina virtuale esistente e recupera l'oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="db897-109">Registers an existing virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="db897-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db897-110">Syntax</span></span>


```C++
HRESULT RegisterVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="db897-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="db897-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db897-112">*ConfigurationName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db897-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db897-113">Nome della macchina virtuale da registrare.</span><span class="sxs-lookup"><span data-stu-id="db897-113">The name of the virtual machine to be registered.</span></span> <span data-ttu-id="db897-114">La lunghezza del nome non può superare i 80 caratteri e la lunghezza combinata del nome e del percorso non può superare il **numero massimo \_** di caratteri (260).</span><span class="sxs-lookup"><span data-stu-id="db897-114">The length of the name cannot exceed 80 characters and the combined length of the name and path cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="db897-115">Il nome specificato può contenere l'estensione vmc.</span><span class="sxs-lookup"><span data-stu-id="db897-115">The specified name may contain the .vmc extension.</span></span> <span data-ttu-id="db897-116">Se questo parametro è **null** o una stringa vuota, il parametro *configurationPath* deve specificare il percorso completo del file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="db897-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="db897-117">*configurationPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db897-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db897-118">Percorso della cartella che contiene il file di configurazione esistente.</span><span class="sxs-lookup"><span data-stu-id="db897-118">The path to the folder that contains the existing configuration file.</span></span> <span data-ttu-id="db897-119">Se il parametro *ConfigurationName* è **null** o una stringa vuota, è necessario specificare il percorso completo del file di configurazione esistente.</span><span class="sxs-lookup"><span data-stu-id="db897-119">If the *configurationName* parameter is **NULL** or an empty string, this must specify the full path to the existing configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="db897-120">*virtualmachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="db897-120">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="db897-121">Puntatore a un nuovo oggetto [**IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="db897-121">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db897-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db897-122">Return value</span></span>

<span data-ttu-id="db897-123">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="db897-123">This method can return one of these values.</span></span>



| <span data-ttu-id="db897-124">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="db897-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="db897-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db897-125">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db897-126"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="db897-126"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="db897-127">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="db897-127">The operation was successful.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="db897-128"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="db897-128"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="db897-129">Il parametro *ConfigurationName* o *configurationPath* non è valido oppure *virtualmachine* è **null**.</span><span class="sxs-lookup"><span data-stu-id="db897-129">The *configurationName* or *configurationPath* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="db897-130"><dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="db897-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="db897-131">Il sistema non è in grado di trovare il percorso specificato dai parametri *ConfigurationName* e *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="db897-131">The system cannot find the path specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="db897-132"><dt>**HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="db897-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="db897-133">Il sistema non è in grado di trovare il file specificato dai parametri *ConfigurationName* e *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="db897-133">The system cannot find the file specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="db897-134"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="db897-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="db897-135">Il parametro *configurationPath* contiene un carattere non valido (uno di " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="db897-135">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="db897-136"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="db897-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="db897-137">Il parametro *configurationPath* parametro specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="db897-137">The parameter *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="db897-138">È necessario specificare un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="db897-138">An absolute path is required.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="db897-139"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="db897-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="db897-140">Il percorso specificato dai parametri *ConfigurationName* e *configurationPath* restituisce un percorso troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="db897-140">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="db897-141">La lunghezza combinata del percorso deve essere minore di **Max \_ path** (260) caratteri.</span><span class="sxs-lookup"><span data-stu-id="db897-141">The combined length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="db897-142"><dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="db897-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="db897-143">Un file di configurazione con questo nome esiste già in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="db897-143">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="db897-144"><dt>**Macchina virtuale \_ Nome di configurazione di E \_ \_ \_ troppo \_ lungo**</dt> <dt>0xA0040401</dt></span><span class="sxs-lookup"><span data-stu-id="db897-144"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="db897-145">Il parametro *ConfigurationName* è di lunghezza superiore a 80 caratteri.</span><span class="sxs-lookup"><span data-stu-id="db897-145">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="db897-146"><dt>**Macchina virtuale \_ Il \_ nome di configurazione E 0xA0040402 \_ non è \_ valido \_**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="db897-146"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="db897-147">Il parametro *ConfigurationName* contiene un carattere non valido (uno di " \* ?: <>/ \| \\ " ").</span><span class="sxs-lookup"><span data-stu-id="db897-147">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="db897-148"><dt>**Macchina virtuale \_ E \_ config \_ \_ nome duplicato**</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="db897-148"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="db897-149">Esiste già una macchina virtuale con questo nome.</span><span class="sxs-lookup"><span data-stu-id="db897-149">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="db897-150"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="db897-150"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="db897-151">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="db897-151">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="db897-152"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="db897-152"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="db897-153">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="db897-153">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="db897-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="db897-154">Remarks</span></span>

<span data-ttu-id="db897-155">I nomi delle macchine virtuali non fanno distinzione tra maiuscole e minuscole, ad esempio, "MyVM" e "MyVM" si riferiscono alla stessa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="db897-155">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="db897-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db897-156">Requirements</span></span>



| <span data-ttu-id="db897-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="db897-157">Requirement</span></span> | <span data-ttu-id="db897-158">Valore</span><span class="sxs-lookup"><span data-stu-id="db897-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="db897-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db897-159">Minimum supported client</span></span><br/> | <span data-ttu-id="db897-160">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="db897-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db897-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db897-161">Minimum supported server</span></span><br/> | <span data-ttu-id="db897-162">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="db897-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="db897-163">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="db897-163">End of client support</span></span><br/>    | <span data-ttu-id="db897-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="db897-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="db897-165">Prodotto</span><span class="sxs-lookup"><span data-stu-id="db897-165">Product</span></span><br/>                  | <span data-ttu-id="db897-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="db897-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="db897-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db897-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="db897-168"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="db897-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="db897-169">IID</span><span class="sxs-lookup"><span data-stu-id="db897-169">IID</span></span><br/>                      | <span data-ttu-id="db897-170">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="db897-170">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="db897-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db897-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db897-172">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="db897-172">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

