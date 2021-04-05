---
title: Metodo Configure IVMSerialPort (VPCCOMInterfaces. h)
description: Configura la porta seriale.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Configurare il metodo Virtual PC
- Configurare il metodo Virtual PC, interfaccia IVMSerialPort
- Interfaccia IVMSerialPort Virtual PC, metodo Configure
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99440263dbf52282b6f3c2756ff7dd76151ff73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048434"
---
# <a name="ivmserialportconfigure-method"></a><span data-ttu-id="34ef1-106">Metodo IVMSerialPort:: Configure</span><span class="sxs-lookup"><span data-stu-id="34ef1-106">IVMSerialPort::Configure method</span></span>

<span data-ttu-id="34ef1-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="34ef1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="34ef1-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="34ef1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="34ef1-109">Configura la porta seriale.</span><span class="sxs-lookup"><span data-stu-id="34ef1-109">Configures the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="34ef1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34ef1-110">Syntax</span></span>


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a><span data-ttu-id="34ef1-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="34ef1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34ef1-112">*portType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ef1-112">*portType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ef1-113">Tipo di porta seriale.</span><span class="sxs-lookup"><span data-stu-id="34ef1-113">The type of serial port.</span></span> <span data-ttu-id="34ef1-114">Per un elenco di valori, vedere [**VMSerialPortType**](vmserialporttype.md).</span><span class="sxs-lookup"><span data-stu-id="34ef1-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

</dd> <dt>

<span data-ttu-id="34ef1-115">*portaname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ef1-115">*portName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ef1-116">Nome della porta seriale.</span><span class="sxs-lookup"><span data-stu-id="34ef1-116">The name of the serial port.</span></span> <span data-ttu-id="34ef1-117">Ad esempio, "COM1" per **vmSerialPort \_ portahost**, "C: \\SerialPort.txt" per **vmSerialPort \_ TextFile** o " \\ \\ *ServerName* \\ pipe \\ *pipeName*" per **vmSerialPort \_ NamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="34ef1-117">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

</dd> <dt>

<span data-ttu-id="34ef1-118">*vmConnectImmediately* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ef1-118">*vmConnectImmediately* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ef1-119">**True** se la porta seriale dell'host deve essere aperta immediatamente quando la macchina virtuale viene avviata e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="34ef1-119">**TRUE** if the host serial port should be opened immediately when the virtual machine is started and **FALSE** otherwise.</span></span> <span data-ttu-id="34ef1-120">Viene ignorato se *portType* non è **vmSerialPort \_ portahost**.</span><span class="sxs-lookup"><span data-stu-id="34ef1-120">Ignored if *portType* is not **vmSerialPort\_HostPort**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34ef1-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34ef1-121">Return value</span></span>

<span data-ttu-id="34ef1-122">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="34ef1-122">This method can return one of these values.</span></span>



| <span data-ttu-id="34ef1-123">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="34ef1-123">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="34ef1-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34ef1-124">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34ef1-125"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="34ef1-125"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="34ef1-126">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="34ef1-126">The operation was successful.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="34ef1-127"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="34ef1-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="34ef1-128">Il parametro *portType* non è valido.</span><span class="sxs-lookup"><span data-stu-id="34ef1-128">The *portType* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="34ef1-129"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="34ef1-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="34ef1-130">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="34ef1-130">An unexpected error has occurred.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="34ef1-131"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="34ef1-131"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="34ef1-132">Il parametro *PortName* è **null**.</span><span class="sxs-lookup"><span data-stu-id="34ef1-132">The *portName* parameter is **NULL**.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="34ef1-133"><dt>**HRESULT \_ DA \_ Win32 (Error \_ OutOfMemory)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="34ef1-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="34ef1-134">La memoria disponibile non è sufficiente per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="34ef1-134">There is not enough memory available to complete this request.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="34ef1-135"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="34ef1-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="34ef1-136">Il percorso specificato dal parametro *PortName* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="34ef1-136">The path specified by the *portName* parameter is too long.</span></span> <span data-ttu-id="34ef1-137">Il percorso deve essere minore di **Max \_ path** (260) caratteri.</span><span class="sxs-lookup"><span data-stu-id="34ef1-137">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="34ef1-138"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="34ef1-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="34ef1-139">Il parametro *PortName* contiene un carattere non valido (uno di " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="34ef1-139">The *portName* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="34ef1-140"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="34ef1-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="34ef1-141">Il parametro *PortName* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="34ef1-141">The *portName* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="34ef1-142">È necessario specificare un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="34ef1-142">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="34ef1-143"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="34ef1-143"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="34ef1-144">La configurazione per questa macchina virtuale non è valida.</span><span class="sxs-lookup"><span data-stu-id="34ef1-144">The configuration for this virtual machine is not valid.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="34ef1-145"><dt>**Macchina virtuale \_ 0xA0040301 \_ \_ \_ valore non valido E pref**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="34ef1-145"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>                   | <span data-ttu-id="34ef1-146">La porta specificata è già in uso.</span><span class="sxs-lookup"><span data-stu-id="34ef1-146">The specified port is already in use.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="34ef1-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34ef1-147">Requirements</span></span>



| <span data-ttu-id="34ef1-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="34ef1-148">Requirement</span></span> | <span data-ttu-id="34ef1-149">Valore</span><span class="sxs-lookup"><span data-stu-id="34ef1-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="34ef1-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34ef1-150">Minimum supported client</span></span><br/> | <span data-ttu-id="34ef1-151">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="34ef1-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="34ef1-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34ef1-152">Minimum supported server</span></span><br/> | <span data-ttu-id="34ef1-153">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="34ef1-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="34ef1-154">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="34ef1-154">End of client support</span></span><br/>    | <span data-ttu-id="34ef1-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="34ef1-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="34ef1-156">Prodotto</span><span class="sxs-lookup"><span data-stu-id="34ef1-156">Product</span></span><br/>                  | <span data-ttu-id="34ef1-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="34ef1-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="34ef1-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34ef1-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="34ef1-159"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="34ef1-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="34ef1-160">IID</span><span class="sxs-lookup"><span data-stu-id="34ef1-160">IID</span></span><br/>                      | <span data-ttu-id="34ef1-161">IID \_ IVMSerialPort è definito come 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="34ef1-161">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="34ef1-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34ef1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34ef1-163">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="34ef1-163">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

