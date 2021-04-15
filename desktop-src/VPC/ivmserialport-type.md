---
title: Proprietà Type di IVMSerialPort (VPCCOMInterfaces. h)
description: Recupera il tipo della porta seriale.
ms.assetid: 0ec9c9d7-9387-458e-befe-42d58c38df35
keywords:
- Tipo proprietà PC virtuale
- Proprietà del tipo Virtual PC, interfaccia IVMSerialPort
- Interfaccia IVMSerialPort Virtual PC, proprietà Type
topic_type:
- apiref
api_name:
- IVMSerialPort.Type
- IVMSerialPort.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ab32ba6e205911fca85474c047e24b7ad7f1f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477062"
---
# <a name="ivmserialporttype-property"></a><span data-ttu-id="f5d29-106">Proprietà IVMSerialPort:: Type</span><span class="sxs-lookup"><span data-stu-id="f5d29-106">IVMSerialPort::Type property</span></span>

<span data-ttu-id="f5d29-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f5d29-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f5d29-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f5d29-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f5d29-109">Recupera il tipo della porta seriale.</span><span class="sxs-lookup"><span data-stu-id="f5d29-109">Retrieves the type of the serial port.</span></span>

<span data-ttu-id="f5d29-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f5d29-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d29-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5d29-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMSerialPortType *portType
);
```



## <a name="property-value"></a><span data-ttu-id="f5d29-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f5d29-112">Property value</span></span>

<span data-ttu-id="f5d29-113">Tipo di porta seriale.</span><span class="sxs-lookup"><span data-stu-id="f5d29-113">The type of serial port.</span></span> <span data-ttu-id="f5d29-114">Per un elenco di valori, vedere [**VMSerialPortType**](vmserialporttype.md).</span><span class="sxs-lookup"><span data-stu-id="f5d29-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="f5d29-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f5d29-115">Error codes</span></span>



| <span data-ttu-id="f5d29-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="f5d29-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f5d29-117">Significato</span><span class="sxs-lookup"><span data-stu-id="f5d29-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5d29-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5d29-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f5d29-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f5d29-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="f5d29-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f5d29-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f5d29-121">Il parametro è NULL.</span><span class="sxs-lookup"><span data-stu-id="f5d29-121">The parameter is NULL.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f5d29-122"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f5d29-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f5d29-123">La configurazione per questa macchina virtuale non è valida.</span><span class="sxs-lookup"><span data-stu-id="f5d29-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="f5d29-124"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f5d29-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f5d29-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f5d29-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="f5d29-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5d29-126">Requirements</span></span>



| <span data-ttu-id="f5d29-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5d29-127">Requirement</span></span> | <span data-ttu-id="f5d29-128">Valore</span><span class="sxs-lookup"><span data-stu-id="f5d29-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d29-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5d29-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d29-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f5d29-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5d29-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5d29-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d29-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f5d29-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f5d29-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f5d29-133">End of client support</span></span><br/>    | <span data-ttu-id="f5d29-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5d29-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f5d29-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f5d29-135">Product</span></span><br/>                  | <span data-ttu-id="f5d29-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f5d29-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f5d29-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5d29-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5d29-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d29-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f5d29-139">IID</span><span class="sxs-lookup"><span data-stu-id="f5d29-139">IID</span></span><br/>                      | <span data-ttu-id="f5d29-140">IID \_ IVMSerialPort è definito come 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="f5d29-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="f5d29-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5d29-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d29-142">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="f5d29-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

