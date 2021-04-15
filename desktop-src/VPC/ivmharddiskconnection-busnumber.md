---
title: Proprietà IVMHardDiskConnection BusNumber (VPCCOMInterfaces. h)
description: Recupera il numero di bus a cui è collegata l'immagine dell'unità.
ms.assetid: 2a792930-d8c9-419d-88eb-ddec7c43c5bc
keywords:
- Proprietà BusNumber Virtual PC
- Proprietà BusNumber Virtual PC, interfaccia IVMHardDiskConnection
- Interfaccia IVMHardDiskConnection Virtual PC, proprietà BusNumber
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.BusNumber
- IVMHardDiskConnection.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdc49a0d4cb284ecd1e2a1340d3b0bf8d9ed43ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477992"
---
# <a name="ivmharddiskconnectionbusnumber-property"></a><span data-ttu-id="d86f6-106">Proprietà IVMHardDiskConnection:: BusNumber</span><span class="sxs-lookup"><span data-stu-id="d86f6-106">IVMHardDiskConnection::BusNumber property</span></span>

<span data-ttu-id="d86f6-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d86f6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d86f6-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d86f6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d86f6-109">Recupera il numero di bus a cui è collegata l'immagine dell'unità.</span><span class="sxs-lookup"><span data-stu-id="d86f6-109">Retrieves the bus number to which the drive image is attached.</span></span>

<span data-ttu-id="d86f6-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d86f6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d86f6-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d86f6-111">Syntax</span></span>


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a><span data-ttu-id="d86f6-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d86f6-112">Property value</span></span>

<span data-ttu-id="d86f6-113">Numero del bus corrispondente a questa connessione.</span><span class="sxs-lookup"><span data-stu-id="d86f6-113">The bus number that corresponds with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d86f6-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d86f6-114">Error codes</span></span>



| <span data-ttu-id="d86f6-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="d86f6-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="d86f6-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d86f6-116">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d86f6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d86f6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="d86f6-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d86f6-118">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="d86f6-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d86f6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="d86f6-120">Il parametro è **null** o non è valido.</span><span class="sxs-lookup"><span data-stu-id="d86f6-120">The parameter is **NULL** or not valid.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d86f6-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d86f6-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="d86f6-122">La configurazione della macchina virtuale corrente non è valida.</span><span class="sxs-lookup"><span data-stu-id="d86f6-122">The current virtual machine configuration is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="d86f6-123"><dt>Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d86f6-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="d86f6-124">Il percorso del bus per questa connessione non è stato inizializzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="d86f6-124">The bus location for this connection has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="d86f6-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d86f6-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="d86f6-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d86f6-126">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="d86f6-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d86f6-127">Requirements</span></span>



| <span data-ttu-id="d86f6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d86f6-128">Requirement</span></span> | <span data-ttu-id="d86f6-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d86f6-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d86f6-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d86f6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d86f6-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d86f6-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d86f6-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d86f6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d86f6-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d86f6-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d86f6-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d86f6-134">End of client support</span></span><br/>    | <span data-ttu-id="d86f6-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d86f6-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d86f6-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d86f6-136">Product</span></span><br/>                  | <span data-ttu-id="d86f6-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d86f6-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d86f6-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d86f6-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d86f6-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d86f6-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d86f6-140">IID</span><span class="sxs-lookup"><span data-stu-id="d86f6-140">IID</span></span><br/>                      | <span data-ttu-id="d86f6-141">IID \_ IVMHardDiskconnection è definito come aefa36a5-463A-46AE-9E6C-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="d86f6-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="d86f6-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d86f6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d86f6-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="d86f6-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

