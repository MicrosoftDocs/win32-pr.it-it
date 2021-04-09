---
title: Metodo _ID IVMSerialPort (VPCCOMInterfaces. h)
description: Identificatore interno della porta seriale.
ms.assetid: c26c18dc-5491-4edf-9338-e4f3bf431084
keywords:
- Metodo di _ID Virtual PC
- Metodo _ID Virtual PC, interfaccia IVMSerialPort
- Interfaccia IVMSerialPort Virtual PC, metodo _ID
topic_type:
- apiref
api_name:
- IVMSerialPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e60f301f80f24681ee297d0fb579994561155
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119698"
---
# <a name="ivmserialport_id-method"></a><span data-ttu-id="4eb7b-106">Metodo IVMSerialPort:: \_ ID</span><span class="sxs-lookup"><span data-stu-id="4eb7b-106">IVMSerialPort::\_ID method</span></span>

<span data-ttu-id="4eb7b-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4eb7b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4eb7b-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4eb7b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4eb7b-109">Recupera l'identificatore interno della porta seriale.</span><span class="sxs-lookup"><span data-stu-id="4eb7b-109">Retrieves the internal identifier of the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb7b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4eb7b-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a><span data-ttu-id="4eb7b-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4eb7b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eb7b-112">*ID porta* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4eb7b-112">*portID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb7b-113">Identificatore della porta seriale.</span><span class="sxs-lookup"><span data-stu-id="4eb7b-113">The serial port identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eb7b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4eb7b-114">Return value</span></span>

<span data-ttu-id="4eb7b-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="4eb7b-115">This method can return one of these values.</span></span>



| <span data-ttu-id="4eb7b-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="4eb7b-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="4eb7b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4eb7b-117">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="4eb7b-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4eb7b-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4eb7b-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4eb7b-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="4eb7b-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4eb7b-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4eb7b-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="4eb7b-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="4eb7b-122"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4eb7b-122"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4eb7b-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="4eb7b-123">An unexpected error has occurred.</span></span><br/>                        |
| <dl> <span data-ttu-id="4eb7b-124"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4eb7b-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="4eb7b-125">La configurazione per questa macchina virtuale non è valida.</span><span class="sxs-lookup"><span data-stu-id="4eb7b-125">The configuration for this virtual machine is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4eb7b-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="4eb7b-126">Remarks</span></span>

<span data-ttu-id="4eb7b-127">Questa proprietà non è utilizzabile dai linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="4eb7b-127">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb7b-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4eb7b-128">Requirements</span></span>



| <span data-ttu-id="4eb7b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eb7b-129">Requirement</span></span> | <span data-ttu-id="4eb7b-130">Valore</span><span class="sxs-lookup"><span data-stu-id="4eb7b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb7b-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4eb7b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb7b-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4eb7b-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4eb7b-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4eb7b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb7b-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4eb7b-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4eb7b-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4eb7b-135">End of client support</span></span><br/>    | <span data-ttu-id="4eb7b-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4eb7b-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4eb7b-137">Prodotto</span><span class="sxs-lookup"><span data-stu-id="4eb7b-137">Product</span></span><br/>                  | <span data-ttu-id="4eb7b-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4eb7b-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4eb7b-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4eb7b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb7b-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eb7b-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4eb7b-141">IID</span><span class="sxs-lookup"><span data-stu-id="4eb7b-141">IID</span></span><br/>                      | <span data-ttu-id="4eb7b-142">IID \_ IVMSerialPort è definito come 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="4eb7b-142">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="4eb7b-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4eb7b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb7b-144">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="4eb7b-144">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

