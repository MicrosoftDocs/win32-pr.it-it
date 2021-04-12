---
title: Proprietà HardDisk IVMHardDiskConnection (VPCCOMInterfaces. h)
description: Recupera un oggetto disco rigido corrispondente a questa connessione.
ms.assetid: dbe369d8-ec05-4039-9494-fc196262f697
keywords:
- Proprietà disco rigido Virtual PC
- Proprietà HardDisk Virtual PC, interfaccia IVMHardDiskConnection
- Interfaccia IVMHardDiskConnection Virtual PC, proprietà HardDisk
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.HardDisk
- IVMHardDiskConnection.get_HardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9baa365606b71b693dd841471d50a475a42677d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400724"
---
# <a name="ivmharddiskconnectionharddisk-property"></a><span data-ttu-id="fad93-106">Proprietà IVMHardDiskConnection:: HardDisk</span><span class="sxs-lookup"><span data-stu-id="fad93-106">IVMHardDiskConnection::HardDisk property</span></span>

<span data-ttu-id="fad93-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fad93-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fad93-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fad93-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fad93-109">Recupera un oggetto disco rigido corrispondente a questa connessione.</span><span class="sxs-lookup"><span data-stu-id="fad93-109">Retrieves a hard disk object corresponding to this connection.</span></span>

<span data-ttu-id="fad93-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fad93-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad93-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fad93-111">Syntax</span></span>


```C++
HRESULT get_HardDisk(
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="property-value"></a><span data-ttu-id="fad93-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fad93-112">Property value</span></span>

<span data-ttu-id="fad93-113">Oggetto [**IVMHardDisk**](ivmharddisk.md) che descrive il disco rigido associato a questa connessione.</span><span class="sxs-lookup"><span data-stu-id="fad93-113">An [**IVMHardDisk**](ivmharddisk.md) object that describes the hard disk associated with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fad93-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="fad93-114">Error codes</span></span>



| <span data-ttu-id="fad93-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="fad93-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="fad93-116">Significato</span><span class="sxs-lookup"><span data-stu-id="fad93-116">Meaning</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fad93-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fad93-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="fad93-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="fad93-118">The operation was successful.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="fad93-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fad93-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="fad93-120">Il parametro è **null** o non è valido.</span><span class="sxs-lookup"><span data-stu-id="fad93-120">The parameter is **NULL** or not valid.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="fad93-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fad93-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="fad93-122">La configurazione della macchina virtuale corrente non è valida.</span><span class="sxs-lookup"><span data-stu-id="fad93-122">The current virtual machine configuration is not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="fad93-123"><dt>Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fad93-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="fad93-124">Il percorso del bus per questa connessione non è stato inizializzato correttamente o il dispositivo in questa posizione non è un disco rigido valido.</span><span class="sxs-lookup"><span data-stu-id="fad93-124">The bus location for this connection has not been properly initialized, or the device at this location is not a valid hard disk.</span></span><br/> |
| <dl> <span data-ttu-id="fad93-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fad93-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="fad93-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="fad93-126">An unexpected error has occurred.</span></span><br/>                                                                                                |



## <a name="requirements"></a><span data-ttu-id="fad93-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fad93-127">Requirements</span></span>



| <span data-ttu-id="fad93-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fad93-128">Requirement</span></span> | <span data-ttu-id="fad93-129">Valore</span><span class="sxs-lookup"><span data-stu-id="fad93-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fad93-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fad93-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fad93-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fad93-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fad93-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fad93-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fad93-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fad93-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fad93-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fad93-134">End of client support</span></span><br/>    | <span data-ttu-id="fad93-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fad93-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fad93-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="fad93-136">Product</span></span><br/>                  | <span data-ttu-id="fad93-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fad93-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fad93-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fad93-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fad93-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fad93-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fad93-140">IID</span><span class="sxs-lookup"><span data-stu-id="fad93-140">IID</span></span><br/>                      | <span data-ttu-id="fad93-141">IID \_ IVMHardDiskconnection è definito come aefa36a5-463A-46AE-9E6C-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="fad93-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="fad93-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fad93-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad93-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="fad93-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

