---
title: Metodo IVMVirtualMachine StartCommunicationChannel (VPCCOMInterfaces. h)
description: Imposta un canale di comunicazione tra l'host e il sistema operativo guest.
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- Metodo StartCommunicationChannel Virtual PC
- Metodo StartCommunicationChannel Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo StartCommunicationChannel
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478323"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a><span data-ttu-id="772b1-106">Metodo IVMVirtualMachine:: StartCommunicationChannel</span><span class="sxs-lookup"><span data-stu-id="772b1-106">IVMVirtualMachine::StartCommunicationChannel method</span></span>

<span data-ttu-id="772b1-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="772b1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="772b1-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="772b1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="772b1-109">Imposta un canale di comunicazione tra l'host e il sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="772b1-109">Sets up a communication channel between host and guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="772b1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="772b1-110">Syntax</span></span>


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a><span data-ttu-id="772b1-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="772b1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="772b1-112">*inHostEndpointType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="772b1-112">*inHostEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772b1-113">Questo parametro deve essere **vmEndpoint \_ NamedPipe** (0).</span><span class="sxs-lookup"><span data-stu-id="772b1-113">This parameter must be **vmEndpoint\_NamedPipe** (0).</span></span>

</dd> <dt>

<span data-ttu-id="772b1-114">*inHostEndPointName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="772b1-114">*inHostEndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772b1-115">Nome univoco della pipe.</span><span class="sxs-lookup"><span data-stu-id="772b1-115">The unique pipe name.</span></span> <span data-ttu-id="772b1-116">Questa stringa deve avere il formato seguente: " \\ \\ . \\ pipe \\ *pipeName*".</span><span class="sxs-lookup"><span data-stu-id="772b1-116">This string must have the following form: "\\\\.\\pipe\\*pipename*".</span></span> <span data-ttu-id="772b1-117">La parte *pipeName* del nome può includere qualsiasi carattere diverso da una barra rovesciata, inclusi i numeri e i caratteri speciali.</span><span class="sxs-lookup"><span data-stu-id="772b1-117">The *pipename* part of the name can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="772b1-118">La lunghezza totale della stringa del nome della pipe può essere di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="772b1-118">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="772b1-119">Per i nomi di pipe non viene fatta distinzione tra maiuscole</span><span class="sxs-lookup"><span data-stu-id="772b1-119">Pipe names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="772b1-120">*inGuestEndpointType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="772b1-120">*inGuestEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772b1-121">Questo parametro deve essere **vmEndpoint \_ Tcpip** (1).</span><span class="sxs-lookup"><span data-stu-id="772b1-121">This parameter must be **vmEndpoint\_TCPIP** (1).</span></span>

</dd> <dt>

<span data-ttu-id="772b1-122">*inGuestEndpointName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="772b1-122">*inGuestEndpointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772b1-123">Numero di porta su cui il server TCP nel Guest è in ascolto.</span><span class="sxs-lookup"><span data-stu-id="772b1-123">The port number on which the TCP server in the guest is listening.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="772b1-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="772b1-124">Return value</span></span>

<span data-ttu-id="772b1-125">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="772b1-125">This method can return one of these values.</span></span>



| <span data-ttu-id="772b1-126">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="772b1-126">Return code/value</span></span>                                                                                                                                                                                  | <span data-ttu-id="772b1-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="772b1-127">Description</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="772b1-128"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="772b1-128"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                        | <span data-ttu-id="772b1-129">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="772b1-129">The operation was successful.</span></span><br/>                                                                                                                    |
| <dl> <span data-ttu-id="772b1-130"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="772b1-130"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                       | <span data-ttu-id="772b1-131">Il parametro *inHostEndpointType* non è **vmEndpoint \_ NamedPipe** (0) o il parametro *inGuestEndpointType* non è **vmEndpoint \_ Tcpip** (1).</span><span class="sxs-lookup"><span data-stu-id="772b1-131">The *inHostEndpointType* parameter is not **vmEndpoint\_NamedPipe** (0) or the *inGuestEndpointType* parameter is not **vmEndpoint\_TCPIP** (1).</span></span><br/> |
| <dl> <span data-ttu-id="772b1-132"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="772b1-132"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                          | <span data-ttu-id="772b1-133">Il parametro *inHostEndPointName* o *inGuestEndpointName* è **null** o non è un valore valido.</span><span class="sxs-lookup"><span data-stu-id="772b1-133">The *inHostEndPointName* or *inGuestEndpointName* parameter is **NULL** or not a valid value.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="772b1-134"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="772b1-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                                  | <span data-ttu-id="772b1-135">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="772b1-135">An unexpected error has occurred.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="772b1-136"><dt>**HRESULT \_ DA \_ Win32 (errore \_ handle non valido \_ )**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="772b1-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_HANDLE)**</dt> <dt>0x80070006</dt></span></span> </dl>        | <span data-ttu-id="772b1-137">Handle non valido.</span><span class="sxs-lookup"><span data-stu-id="772b1-137">A handle is not valid.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="772b1-138"><dt>**HRESULT \_ DA \_ Win32 (Error \_ OutOfMemory)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="772b1-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>            | <span data-ttu-id="772b1-139">La memoria disponibile non è sufficiente per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="772b1-139">There is not enough memory available to complete this request.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="772b1-140"><dt>**HRESULT \_ DA \_ Win32 (errore \_ non \_ pronto)**</dt> <dt>0x80070015</dt></span><span class="sxs-lookup"><span data-stu-id="772b1-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_READY)**</dt> <dt>0x80070015</dt></span></span> </dl>             | <span data-ttu-id="772b1-141">Il sistema sottostante usato per fornire servizi di rete è attualmente in fase di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="772b1-141">The underlying system it uses to provide network services is currently being initialized.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="772b1-142"><dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="772b1-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>        | <span data-ttu-id="772b1-143">Il nome della pipe è già in uso.</span><span class="sxs-lookup"><span data-stu-id="772b1-143">The pipe name is already in use.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="772b1-144"><dt>**HRESULT \_ DA \_ Win32 (pipe di errore \_ \_ occupata)**</dt> <dt>0x800700e7</dt></span><span class="sxs-lookup"><span data-stu-id="772b1-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PIPE\_BUSY)**</dt> <dt>0x800700e7</dt></span></span> </dl>             | <span data-ttu-id="772b1-145">Uno o più canali sono in esecuzione e potrebbero essere disponibili a breve.</span><span class="sxs-lookup"><span data-stu-id="772b1-145">One or more channels are running down and may become available shortly.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="772b1-146"><dt>**HRESULT \_ DA \_ Win32 (errore \_ Max \_ sessioni \_ raggiunte)**</dt> <dt>0x80070161</dt></span><span class="sxs-lookup"><span data-stu-id="772b1-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_MAX\_SESSIONS\_REACHED)**</dt> <dt>0x80070161</dt></span></span> </dl> | <span data-ttu-id="772b1-147">Il numero massimo di canali di comunicazione disponibili è in uso.</span><span class="sxs-lookup"><span data-stu-id="772b1-147">The maximum numbers of communication channels available are in-use.</span></span> <span data-ttu-id="772b1-148">Non è possibile avviare un altro canale in questo momento.</span><span class="sxs-lookup"><span data-stu-id="772b1-148">Another channel cannot be started at this time.</span></span><br/>                              |
| <dl> <span data-ttu-id="772b1-149"><dt>**HRESULT \_ DA \_ Win32 ( \_ \_ mancata corrispondenza Revisione errore)**</dt> <dt>0x8007051a</dt></span><span class="sxs-lookup"><span data-stu-id="772b1-149"><dt>**HRESULT\_FROM\_WIN32(ERROR\_REVISION\_MISMATCH)**</dt> <dt>0x8007051a</dt></span></span> </dl>     | <span data-ttu-id="772b1-150">Mancata corrispondenza tra la versione dei sottosistemi host e Guest.</span><span class="sxs-lookup"><span data-stu-id="772b1-150">There is a mismatch between the version of the host and guest subsystems.</span></span> <span data-ttu-id="772b1-151">Per ulteriori informazioni, vedere il registro eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="772b1-151">See the Windows Event Log for more detail.</span></span><br/>                             |
| <dl> <span data-ttu-id="772b1-152"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="772b1-152"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                             | <span data-ttu-id="772b1-153">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="772b1-153">The VM is not running.</span></span><br/>                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="772b1-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="772b1-154">Remarks</span></span>

<span data-ttu-id="772b1-155">L'implementazione corrente supporta solo named pipe interfaccia sull'host e sull'interfaccia TCP/IP nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="772b1-155">The current implementation supports only named pipe interface on the host and TCP/IP interface on the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="772b1-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="772b1-156">Requirements</span></span>



| <span data-ttu-id="772b1-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="772b1-157">Requirement</span></span> | <span data-ttu-id="772b1-158">Valore</span><span class="sxs-lookup"><span data-stu-id="772b1-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="772b1-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="772b1-159">Minimum supported client</span></span><br/> | <span data-ttu-id="772b1-160">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="772b1-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="772b1-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="772b1-161">Minimum supported server</span></span><br/> | <span data-ttu-id="772b1-162">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="772b1-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="772b1-163">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="772b1-163">End of client support</span></span><br/>    | <span data-ttu-id="772b1-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="772b1-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="772b1-165">Prodotto</span><span class="sxs-lookup"><span data-stu-id="772b1-165">Product</span></span><br/>                  | <span data-ttu-id="772b1-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="772b1-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="772b1-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="772b1-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="772b1-168"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="772b1-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="772b1-169">IID</span><span class="sxs-lookup"><span data-stu-id="772b1-169">IID</span></span><br/>                      | <span data-ttu-id="772b1-170">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="772b1-170">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="772b1-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="772b1-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="772b1-172">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="772b1-172">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="772b1-173">**VMEndpointType**</span><span class="sxs-lookup"><span data-stu-id="772b1-173">**VMEndpointType**</span></span>](vmendpointtype.md)
</dt> </dl>

 

