---
title: Proprietà Name di IVMSerialPort (VPCCOMInterfaces. h)
description: Nome della porta seriale.
ms.assetid: 4d3fe008-f089-4a1b-9c90-2e0b3ded58fa
keywords:
- Nome proprietà PC virtuale
- Proprietà nome Virtual PC, interfaccia IVMSerialPort
- Interfaccia IVMSerialPort Virtual PC, proprietà Name
topic_type:
- apiref
api_name:
- IVMSerialPort.Name
- IVMSerialPort.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540540e2af91647b9c77735a1c601ed62aecdbdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874374"
---
# <a name="ivmserialportname-property"></a><span data-ttu-id="c61a8-106">Proprietà IVMSerialPort:: Name</span><span class="sxs-lookup"><span data-stu-id="c61a8-106">IVMSerialPort::Name property</span></span>

<span data-ttu-id="c61a8-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c61a8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c61a8-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c61a8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c61a8-109">Recupera il nome della porta seriale.</span><span class="sxs-lookup"><span data-stu-id="c61a8-109">Retrieves the name of the serial port.</span></span>

<span data-ttu-id="c61a8-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c61a8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c61a8-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c61a8-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="c61a8-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c61a8-112">Property value</span></span>

<span data-ttu-id="c61a8-113">Nome della porta seriale.</span><span class="sxs-lookup"><span data-stu-id="c61a8-113">The name of the serial port.</span></span> <span data-ttu-id="c61a8-114">Ad esempio, "COM1" per **vmSerialPort \_ portahost**, "C: \\SerialPort.txt" per **vmSerialPort \_ TextFile** o " \\ \\ *ServerName* \\ pipe \\ *pipeName*" per **vmSerialPort \_ NamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="c61a8-114">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c61a8-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c61a8-115">Error codes</span></span>



| <span data-ttu-id="c61a8-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="c61a8-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c61a8-117">Significato</span><span class="sxs-lookup"><span data-stu-id="c61a8-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="c61a8-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c61a8-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c61a8-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c61a8-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="c61a8-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c61a8-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c61a8-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="c61a8-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="c61a8-122"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c61a8-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c61a8-123">La configurazione per questa macchina virtuale non è valida.</span><span class="sxs-lookup"><span data-stu-id="c61a8-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="c61a8-124"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c61a8-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c61a8-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="c61a8-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="c61a8-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c61a8-126">Requirements</span></span>



| <span data-ttu-id="c61a8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c61a8-127">Requirement</span></span> | <span data-ttu-id="c61a8-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c61a8-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c61a8-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c61a8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c61a8-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c61a8-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c61a8-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c61a8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c61a8-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c61a8-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c61a8-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c61a8-133">End of client support</span></span><br/>    | <span data-ttu-id="c61a8-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c61a8-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c61a8-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c61a8-135">Product</span></span><br/>                  | <span data-ttu-id="c61a8-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c61a8-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c61a8-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c61a8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c61a8-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c61a8-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c61a8-139">IID</span><span class="sxs-lookup"><span data-stu-id="c61a8-139">IID</span></span><br/>                      | <span data-ttu-id="c61a8-140">IID \_ IVMSerialPort è definito come 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="c61a8-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="c61a8-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c61a8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61a8-142">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="c61a8-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

