---
title: Metodo IVMVirtualPC CreateVirtualMachine (VPCCOMInterfaces. h)
description: Crea una nuova configurazione di macchina virtuale e recupera l'oggetto macchina virtuale.
ms.assetid: 35f7364f-debd-4b9c-8240-23c0512eb004
keywords:
- Metodo CreateVirtualMachine Virtual PC
- Metodo CreateVirtualMachine Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo CreateVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 494d5166271e6c4086b8dfee12deb61e32ae8a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478154"
---
# <a name="ivmvirtualpccreatevirtualmachine-method"></a><span data-ttu-id="27572-106">Metodo IVMVirtualPC:: CreateVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="27572-106">IVMVirtualPC::CreateVirtualMachine method</span></span>

<span data-ttu-id="27572-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="27572-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="27572-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="27572-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="27572-109">Crea una nuova configurazione di macchina virtuale e recupera l'oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="27572-109">Creates a new virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="27572-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27572-110">Syntax</span></span>


```C++
HRESULT CreateVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="27572-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="27572-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27572-112">*ConfigurationName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27572-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27572-113">Nome della macchina virtuale da creare.</span><span class="sxs-lookup"><span data-stu-id="27572-113">The name of the virtual machine to be created.</span></span> <span data-ttu-id="27572-114">La lunghezza del nome non può superare i 80 caratteri e la lunghezza combinata del nome e del percorso dei file VMC e VMCX non può superare il numero massimo di caratteri di **\_ percorso** (260).</span><span class="sxs-lookup"><span data-stu-id="27572-114">The length of the name cannot exceed 80 characters and the combined length of the name and path to VMC and VMCX files cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="27572-115">Quando vengono creati i file di configurazione, il nome file Extensions. vmc e. vmcx verrà aggiunto alla fine del nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="27572-115">The file name extensions .vmc and .vmcx will be appended to the end of the virtual machine name when the configuration files are created.</span></span> <span data-ttu-id="27572-116">Se questo parametro è **null** o una stringa vuota, il parametro *configurationPath* deve specificare il percorso completo del file vmc.</span><span class="sxs-lookup"><span data-stu-id="27572-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the VMC file.</span></span>

</dd> <dt>

<span data-ttu-id="27572-117">*configurationPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27572-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27572-118">Percorso della cartella che conterrà il file VMC.</span><span class="sxs-lookup"><span data-stu-id="27572-118">The path to the folder that will contain the VMC file.</span></span> <span data-ttu-id="27572-119">Questa cartella verrà creata se non esiste.</span><span class="sxs-lookup"><span data-stu-id="27572-119">This folder will be created if it does not exist.</span></span> <span data-ttu-id="27572-120">Se *ConfigurationName* è **null** o una stringa vuota, è necessario specificare il percorso completo del nuovo file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="27572-120">If *configurationName* is **NULL** or an empty string, this must specify the full path of the new configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="27572-121">*virtualmachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="27572-121">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="27572-122">Puntatore a un nuovo oggetto [**IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="27572-122">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27572-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27572-123">Return value</span></span>

<span data-ttu-id="27572-124">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="27572-124">This method can return one of these values.</span></span>



| <span data-ttu-id="27572-125">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="27572-125">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="27572-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27572-126">Description</span></span>                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27572-127"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="27572-127"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="27572-128">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="27572-128">The operation was successful.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="27572-129"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="27572-129"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="27572-130">Il parametro *ConfigurationName* o *configurationPath* non è valido oppure il parametro *virtualmachine* è **null**.</span><span class="sxs-lookup"><span data-stu-id="27572-130">The *configurationName* or *configurationPath* parameter is not valid, or the *virtualMachine* parameter is **NULL**.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="27572-131"><dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="27572-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="27572-132">Il sistema non è in grado di trovare il percorso specificato dal parametro *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="27572-132">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="27572-133"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="27572-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="27572-134">Il parametro *configurationPath* contiene un carattere non valido (uno di " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="27572-134">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="27572-135"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="27572-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="27572-136">Il parametro *configurationPath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="27572-136">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="27572-137">È necessario specificare un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="27572-137">An absolute path is required.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="27572-138"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="27572-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="27572-139">Il percorso specificato dai parametri *ConfigurationName* e *configurationPath* restituisce un percorso troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="27572-139">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="27572-140">La lunghezza totale del percorso deve essere minore di **Max \_ path** (260) caratteri.</span><span class="sxs-lookup"><span data-stu-id="27572-140">The total length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="27572-141"><dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="27572-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="27572-142">Un file di configurazione con questo nome esiste già in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="27572-142">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="27572-143"><dt>**Macchina virtuale \_ E \_ config \_ senza \_ nome**</dt> <dt>0xA0040400</dt></span><span class="sxs-lookup"><span data-stu-id="27572-143"><dt>**VM\_E\_CONFIG\_NO\_NAME**</dt> <dt>0xA0040400</dt></span></span> </dl>                       | <span data-ttu-id="27572-144">Il parametro *ConfigurationName* è vuoto.</span><span class="sxs-lookup"><span data-stu-id="27572-144">The *configurationName* parameter is empty.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="27572-145"><dt>**Macchina virtuale \_ Nome di configurazione di E \_ \_ \_ troppo \_ lungo**</dt> <dt>0xA0040401</dt></span><span class="sxs-lookup"><span data-stu-id="27572-145"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="27572-146">Il parametro *ConfigurationName* è di lunghezza superiore a 80 caratteri.</span><span class="sxs-lookup"><span data-stu-id="27572-146">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="27572-147"><dt>**Macchina virtuale \_ Il \_ nome di configurazione E 0xA0040402 \_ non è \_ valido \_**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="27572-147"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="27572-148">Il parametro *ConfigurationName* contiene un carattere non valido (uno di " \* ?: <>/ \| \\ " ").</span><span class="sxs-lookup"><span data-stu-id="27572-148">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="27572-149"><dt>**Macchina virtuale \_ E \_ config \_ \_ nome duplicato**</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="27572-149"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="27572-150">Esiste già una macchina virtuale con questo nome.</span><span class="sxs-lookup"><span data-stu-id="27572-150">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="27572-151"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="27572-151"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="27572-152">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="27572-152">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="27572-153"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="27572-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="27572-154">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="27572-154">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="27572-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="27572-155">Remarks</span></span>

<span data-ttu-id="27572-156">I nomi delle macchine virtuali non fanno distinzione tra maiuscole e minuscole, ad esempio, "MyVM" e "MyVM" si riferiscono alla stessa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="27572-156">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="27572-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27572-157">Requirements</span></span>



| <span data-ttu-id="27572-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="27572-158">Requirement</span></span> | <span data-ttu-id="27572-159">Valore</span><span class="sxs-lookup"><span data-stu-id="27572-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="27572-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27572-160">Minimum supported client</span></span><br/> | <span data-ttu-id="27572-161">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="27572-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27572-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27572-162">Minimum supported server</span></span><br/> | <span data-ttu-id="27572-163">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="27572-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="27572-164">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="27572-164">End of client support</span></span><br/>    | <span data-ttu-id="27572-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27572-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="27572-166">Prodotto</span><span class="sxs-lookup"><span data-stu-id="27572-166">Product</span></span><br/>                  | <span data-ttu-id="27572-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="27572-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="27572-168">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27572-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="27572-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="27572-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="27572-170">IID</span><span class="sxs-lookup"><span data-stu-id="27572-170">IID</span></span><br/>                      | <span data-ttu-id="27572-171">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="27572-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="27572-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27572-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27572-173">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="27572-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

