---
title: Proprietà IVMHardDiskConnection DeviceNumber (VPCCOMInterfaces. h)
description: Recupera il numero di dispositivo a cui è collegata l'immagine dell'unità.
ms.assetid: fea8bac6-fb25-495a-bc56-1d517b831f33
keywords:
- Proprietà DeviceNumber Virtual PC
- Proprietà DeviceNumber Virtual PC, interfaccia IVMHardDiskConnection
- Interfaccia IVMHardDiskConnection Virtual PC, proprietà DeviceNumber
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.DeviceNumber
- IVMHardDiskConnection.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69f7d9d3f9a373c9b8086857af56c7e5da9f5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121190"
---
# <a name="ivmharddiskconnectiondevicenumber-property"></a><span data-ttu-id="1fedd-106">IVMHardDiskConnection::D Proprietà eviceNumber</span><span class="sxs-lookup"><span data-stu-id="1fedd-106">IVMHardDiskConnection::DeviceNumber property</span></span>

<span data-ttu-id="1fedd-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1fedd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1fedd-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1fedd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1fedd-109">Recupera il numero di dispositivo a cui è collegata l'immagine dell'unità.</span><span class="sxs-lookup"><span data-stu-id="1fedd-109">Retrieves the device number to which the drive image is attached.</span></span>

<span data-ttu-id="1fedd-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1fedd-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fedd-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1fedd-111">Syntax</span></span>


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a><span data-ttu-id="1fedd-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1fedd-112">Property value</span></span>

<span data-ttu-id="1fedd-113">Numero del dispositivo che corrisponde a questa connessione.</span><span class="sxs-lookup"><span data-stu-id="1fedd-113">The device number that corresponds with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1fedd-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="1fedd-114">Error codes</span></span>



| <span data-ttu-id="1fedd-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="1fedd-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="1fedd-116">Significato</span><span class="sxs-lookup"><span data-stu-id="1fedd-116">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1fedd-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1fedd-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="1fedd-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="1fedd-118">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="1fedd-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1fedd-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="1fedd-120">Il parametro è **null** o non è valido.</span><span class="sxs-lookup"><span data-stu-id="1fedd-120">The parameter is **NULL** or not valid.</span></span><br/>                                 |
| <dl> <span data-ttu-id="1fedd-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1fedd-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="1fedd-122">La configurazione della macchina virtuale corrente non è valida.</span><span class="sxs-lookup"><span data-stu-id="1fedd-122">The current virtual machine configuration is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="1fedd-123"><dt>Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1fedd-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="1fedd-124">Il percorso del bus per questa connessione non è stato inizializzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="1fedd-124">The bus location for this connection has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="1fedd-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1fedd-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="1fedd-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1fedd-126">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="1fedd-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fedd-127">Requirements</span></span>



| <span data-ttu-id="1fedd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fedd-128">Requirement</span></span> | <span data-ttu-id="1fedd-129">Valore</span><span class="sxs-lookup"><span data-stu-id="1fedd-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fedd-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fedd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1fedd-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1fedd-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1fedd-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fedd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1fedd-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1fedd-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1fedd-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1fedd-134">End of client support</span></span><br/>    | <span data-ttu-id="1fedd-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1fedd-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1fedd-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="1fedd-136">Product</span></span><br/>                  | <span data-ttu-id="1fedd-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1fedd-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1fedd-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1fedd-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fedd-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fedd-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1fedd-140">IID</span><span class="sxs-lookup"><span data-stu-id="1fedd-140">IID</span></span><br/>                      | <span data-ttu-id="1fedd-141">IID \_ IVMHardDiskconnection è definito come aefa36a5-463A-46AE-9E6C-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="1fedd-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="1fedd-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1fedd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fedd-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="1fedd-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

