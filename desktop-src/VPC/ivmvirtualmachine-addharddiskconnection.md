---
title: Metodo IVMVirtualMachine AddHardDiskConnection (VPCCOMInterfaces. h)
description: Aggiunge una nuova connessione al disco rigido alla macchina virtuale.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- Metodo AddHardDiskConnection Virtual PC
- Metodo AddHardDiskConnection Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo AddHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301776"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a><span data-ttu-id="6d742-106">Metodo IVMVirtualMachine:: AddHardDiskConnection</span><span class="sxs-lookup"><span data-stu-id="6d742-106">IVMVirtualMachine::AddHardDiskConnection method</span></span>

<span data-ttu-id="6d742-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6d742-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6d742-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6d742-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6d742-109">Aggiunge una nuova connessione al disco rigido alla macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="6d742-109">Adds a new hard disk connection to the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d742-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d742-110">Syntax</span></span>


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="6d742-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d742-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d742-112">*hardDiskPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d742-112">*hardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d742-113">Percorso completo del file del disco rigido virtuale (VHD) da connettere.</span><span class="sxs-lookup"><span data-stu-id="6d742-113">The full path of the virtual hard disk (VHD) file to connect.</span></span>

</dd> <dt>

<span data-ttu-id="6d742-114">*busNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d742-114">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d742-115">Il bus al quale verrà collegata l'unità.</span><span class="sxs-lookup"><span data-stu-id="6d742-115">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="6d742-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6d742-116">Value</span></span>                                                                        | <span data-ttu-id="6d742-117">Significato</span><span class="sxs-lookup"><span data-stu-id="6d742-117">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="6d742-118"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-118"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6d742-119">L'unità verrà collegata al primo bus.</span><span class="sxs-lookup"><span data-stu-id="6d742-119">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="6d742-120"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-120"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6d742-121">L'unità verrà collegata al secondo bus.</span><span class="sxs-lookup"><span data-stu-id="6d742-121">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6d742-122">*deviceNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d742-122">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d742-123">Dispositivo a cui verrà collegata l'unità.</span><span class="sxs-lookup"><span data-stu-id="6d742-123">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="6d742-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6d742-124">Value</span></span>                                                                        | <span data-ttu-id="6d742-125">Significato</span><span class="sxs-lookup"><span data-stu-id="6d742-125">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d742-126"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-126"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6d742-127">L'unità verrà collegata al primo dispositivo del bus.</span><span class="sxs-lookup"><span data-stu-id="6d742-127">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="6d742-128"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-128"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6d742-129">L'unità verrà collegata al secondo dispositivo del bus.</span><span class="sxs-lookup"><span data-stu-id="6d742-129">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6d742-130">*hardDiskConnection* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6d742-130">*hardDiskConnection* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6d742-131">Oggetto [**IVMHardDiskConnection**](ivmharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="6d742-131">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d742-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d742-132">Return value</span></span>

<span data-ttu-id="6d742-133">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="6d742-133">This method can return one of these values.</span></span>



| <span data-ttu-id="6d742-134">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d742-134">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="6d742-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d742-135">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d742-136"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-136"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="6d742-137">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="6d742-137">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="6d742-138"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-138"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="6d742-139">Il parametro *hardDiskConnection* è **null**.</span><span class="sxs-lookup"><span data-stu-id="6d742-139">The *hardDiskConnection* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="6d742-140"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="6d742-140"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="6d742-141">Il parametro *hardDiskPath* è **null** o il parametro *busNumber* o *deviceNumber* non è valido.</span><span class="sxs-lookup"><span data-stu-id="6d742-141">A *hardDiskPath* parameter is **NULL** or the *busNumber* or *deviceNumber* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="6d742-142"><dt>**HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="6d742-143">Il sistema non è in grado di trovare il file specificato dal parametro *hardDiskPath* .</span><span class="sxs-lookup"><span data-stu-id="6d742-143">The system cannot find the file specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="6d742-144"><dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="6d742-145">Il sistema non è in grado di trovare il percorso specificato dal parametro *hardDiskPath* .</span><span class="sxs-lookup"><span data-stu-id="6d742-145">The system cannot find the path specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="6d742-146"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="6d742-147">Il parametro *hardDiskPath* contiene un carattere non valido (uno di " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="6d742-147">The *hardDiskPath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6d742-148"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="6d742-149">Il parametro *hardDiskPath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="6d742-149">The *hardDiskPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="6d742-150">È necessario specificare un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="6d742-150">An absolute path is required.</span></span><br/>                                                |
| <dl> <span data-ttu-id="6d742-151"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-151"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="6d742-152">Il percorso specificato dal parametro *hardDiskPath* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="6d742-152">The path specified by the *hardDiskPath* parameter is too long.</span></span> <span data-ttu-id="6d742-153">Il percorso deve essere composto da meno di 260 caratteri.</span><span class="sxs-lookup"><span data-stu-id="6d742-153">The path must be less than 260 characters.</span></span><br/>                                     |
| <dl> <span data-ttu-id="6d742-154"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6d742-154"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                              | <span data-ttu-id="6d742-155">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="6d742-155">The configuration is unknown.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="6d742-156"><dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-156"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>                   | <span data-ttu-id="6d742-157">Lo stato della macchina virtuale è in esecuzione o salvato.</span><span class="sxs-lookup"><span data-stu-id="6d742-157">The VM is in a running or saved state.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="6d742-158"><dt>**Macchina virtuale \_ E \_ la \_ \_ loc \_ del bus di unità in \_ use**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-158"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl>                | <span data-ttu-id="6d742-159">Il percorso del bus specificato è in uso.</span><span class="sxs-lookup"><span data-stu-id="6d742-159">The specified bus location is in use.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="6d742-160"><dt>**Macchina virtuale \_ E \_ \_ \_ file HD non valido**</dt> <dt>0xA0040682</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-160"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="6d742-161">Il disco rigido virtuale è maggiore di 127 GB e non può essere connesso al bus IDE.</span><span class="sxs-lookup"><span data-stu-id="6d742-161">The VHD is greater than 127 GB and cannot be connected to the IDE bus.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="6d742-162"><dt>**Macchina virtuale \_ E \_ \_ \_ \_ tipo di disco HD non supportato**</dt> <dt>0xA00400686</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-162"><dt>**VM\_E\_UNSUPPORTED\_HD\_DISK\_TYPE**</dt> <dt>0xA00400686</dt></span></span> </dl>             | <span data-ttu-id="6d742-163">Il parametro *hardDiskPath* fa riferimento a un VHD collegato o a un disco rigido virtuale differenze in un disco rigido virtuale collegato.</span><span class="sxs-lookup"><span data-stu-id="6d742-163">The *hardDiskPath* parameter refers to a linked VHD or a differencing VHD to a linked VHD.</span></span> <span data-ttu-id="6d742-164">Non è possibile collegare VHD collegati alle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="6d742-164">Linked VHDs cannot be attached to virtual machines.</span></span><br/> |
| <dl> <span data-ttu-id="6d742-165"><dt>**HRESULT \_ Da \_ Win32 (violazione della condivisione degli errori \_ \_ )**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-165"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="6d742-166">Il disco rigido virtuale specificato è già connesso a un altro percorso del bus per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6d742-166">The specified VHD is already connected to another bus location for this VM.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="6d742-167"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6d742-167"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="6d742-168">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="6d742-168">An unexpected error has occurred.</span></span><br/>                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="6d742-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d742-169">Remarks</span></span>

<span data-ttu-id="6d742-170">È possibile aggiungere solo una nuova connessione al disco rigido a una macchina virtuale arrestata.</span><span class="sxs-lookup"><span data-stu-id="6d742-170">You can only add a new hard disk connection to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d742-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d742-171">Requirements</span></span>



| <span data-ttu-id="6d742-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d742-172">Requirement</span></span> | <span data-ttu-id="6d742-173">Valore</span><span class="sxs-lookup"><span data-stu-id="6d742-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d742-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d742-174">Minimum supported client</span></span><br/> | <span data-ttu-id="6d742-175">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6d742-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d742-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d742-176">Minimum supported server</span></span><br/> | <span data-ttu-id="6d742-177">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6d742-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6d742-178">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6d742-178">End of client support</span></span><br/>    | <span data-ttu-id="6d742-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6d742-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6d742-180">Prodotto</span><span class="sxs-lookup"><span data-stu-id="6d742-180">Product</span></span><br/>                  | <span data-ttu-id="6d742-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6d742-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6d742-182">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d742-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d742-183"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d742-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6d742-184">IID</span><span class="sxs-lookup"><span data-stu-id="6d742-184">IID</span></span><br/>                      | <span data-ttu-id="6d742-185">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="6d742-185">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6d742-186">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d742-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d742-187">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="6d742-187">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

