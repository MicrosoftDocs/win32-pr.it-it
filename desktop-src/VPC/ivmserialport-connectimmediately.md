---
title: Proprietà IVMSerialPort ConnectImmediately (VPCCOMInterfaces. h)
description: Determina se la porta seriale deve essere aperta senza attendere la ricezione di un comando del modem.
ms.assetid: 5ac22906-0fe2-477d-98af-7c05ce274cc5
keywords:
- Proprietà ConnectImmediately Virtual PC
- Proprietà ConnectImmediately Virtual PC, interfaccia IVMSerialPort
- Interfaccia IVMSerialPort Virtual PC, proprietà ConnectImmediately
topic_type:
- apiref
api_name:
- IVMSerialPort.ConnectImmediately
- IVMSerialPort.get_ConnectImmediately
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7661b9cf3b118427b1ecb2b6f450913e35e35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741743"
---
# <a name="ivmserialportconnectimmediately-property"></a><span data-ttu-id="f191e-106">Proprietà IVMSerialPort:: ConnectImmediately</span><span class="sxs-lookup"><span data-stu-id="f191e-106">IVMSerialPort::ConnectImmediately property</span></span>

<span data-ttu-id="f191e-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f191e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f191e-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f191e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f191e-109">Determina se la porta seriale deve essere aperta senza attendere la ricezione di un comando del modem.</span><span class="sxs-lookup"><span data-stu-id="f191e-109">Determines whether the serial port should be opened without waiting for a modem command to be received.</span></span>

<span data-ttu-id="f191e-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f191e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f191e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f191e-111">Syntax</span></span>


```C++
HRESULT get_ConnectImmediately(
  [out, retval] VARIANT_BOOL *vmConnectImmediately
);
```



## <a name="property-value"></a><span data-ttu-id="f191e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f191e-112">Property value</span></span>

<span data-ttu-id="f191e-113">**Variante \_ TRUE** se la porta seriale deve essere aperta senza attendere la ricezione di un comando del modem. **Variante \_** In caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="f191e-113">**VARIANT\_TRUE** if the serial port should be opened without waiting for a modem command to be received; **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f191e-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f191e-114">Error codes</span></span>



| <span data-ttu-id="f191e-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="f191e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f191e-116">Significato</span><span class="sxs-lookup"><span data-stu-id="f191e-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="f191e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f191e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f191e-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f191e-118">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="f191e-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f191e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f191e-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="f191e-120">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="f191e-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f191e-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f191e-122">La configurazione per questa macchina virtuale non è valida.</span><span class="sxs-lookup"><span data-stu-id="f191e-122">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="f191e-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f191e-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f191e-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f191e-124">An unexpected error has occurred.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="f191e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f191e-125">Remarks</span></span>

<span data-ttu-id="f191e-126">Questa proprietà è valida solo se la proprietà [**tipo**](ivmserialport-type.md) porta è **vmSerialPort \_ portahost**.</span><span class="sxs-lookup"><span data-stu-id="f191e-126">This property is valid only if the port [**Type**](ivmserialport-type.md) property is **vmSerialPort\_HostPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f191e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f191e-127">Requirements</span></span>



| <span data-ttu-id="f191e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f191e-128">Requirement</span></span> | <span data-ttu-id="f191e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f191e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f191e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f191e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f191e-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f191e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f191e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f191e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f191e-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f191e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f191e-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f191e-134">End of client support</span></span><br/>    | <span data-ttu-id="f191e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f191e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f191e-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f191e-136">Product</span></span><br/>                  | <span data-ttu-id="f191e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f191e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f191e-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f191e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f191e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f191e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f191e-140">IID</span><span class="sxs-lookup"><span data-stu-id="f191e-140">IID</span></span><br/>                      | <span data-ttu-id="f191e-141">IID \_ IVMSerialPort è definito come 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="f191e-141">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="f191e-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f191e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f191e-143">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="f191e-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

