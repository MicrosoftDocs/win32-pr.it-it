---
title: Proprietà IVMHardDiskConnection UndoHardDisk (VPCCOMInterfaces. h)
description: Recupera un oggetto disco rigido corrispondente all'immagine del disco di annullamento della connessione.
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- Proprietà UndoHardDisk Virtual PC
- Proprietà UndoHardDisk Virtual PC, interfaccia IVMHardDiskConnection
- Interfaccia IVMHardDiskConnection Virtual PC, proprietà UndoHardDisk
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.UndoHardDisk
- IVMHardDiskConnection.get_UndoHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0fcbd6535c0cf91e1b42549047c131c1804215c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118926"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a><span data-ttu-id="0d6dd-106">Proprietà IVMHardDiskConnection:: UndoHardDisk</span><span class="sxs-lookup"><span data-stu-id="0d6dd-106">IVMHardDiskConnection::UndoHardDisk property</span></span>

<span data-ttu-id="0d6dd-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0d6dd-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0d6dd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0d6dd-109">Recupera un oggetto disco rigido corrispondente all'immagine del disco di annullamento della connessione.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-109">Retrieves a hard disk object corresponding to this connection's undo disk image.</span></span>

<span data-ttu-id="0d6dd-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d6dd-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d6dd-111">Syntax</span></span>


```C++
HRESULT get_UndoHardDisk(
  [out, retval] IVMHardDisk **undoHardDisk
);
```



## <a name="property-value"></a><span data-ttu-id="0d6dd-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0d6dd-112">Property value</span></span>

<span data-ttu-id="0d6dd-113">Oggetto [**IVMHardDisk**](ivmharddisk.md) che descrive il disco rigido di annullamento associato a questa connessione.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-113">An [**IVMHardDisk**](ivmharddisk.md) object that describes the undo hard disk associated with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0d6dd-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0d6dd-114">Error codes</span></span>



| <span data-ttu-id="0d6dd-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="0d6dd-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="0d6dd-116">Significato</span><span class="sxs-lookup"><span data-stu-id="0d6dd-116">Meaning</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d6dd-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0d6dd-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="0d6dd-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-118">The operation was successful.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="0d6dd-119"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0d6dd-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="0d6dd-120">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-120">An unexpected error has occurred.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="0d6dd-121"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0d6dd-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="0d6dd-122">Il parametro è **null** o non è valido.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-122">The parameter is **NULL** or not valid.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="0d6dd-123"><dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="0d6dd-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="0d6dd-124">Il disco di annullamento per questa connessione non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-124">The undo disk for this connection was not found.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="0d6dd-125"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0d6dd-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="0d6dd-126">La configurazione della macchina virtuale corrente non è valida.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-126">The current virtual machine configuration is not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="0d6dd-127"><dt>Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0d6dd-127"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="0d6dd-128">Il percorso del bus per questa connessione non è stato inizializzato correttamente o il dispositivo in questa posizione non è un disco rigido valido.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-128">The bus location for this connection has not been properly initialized, or the device at this location is not a valid hard disk.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0d6dd-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d6dd-129">Requirements</span></span>



| <span data-ttu-id="0d6dd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d6dd-130">Requirement</span></span> | <span data-ttu-id="0d6dd-131">Valore</span><span class="sxs-lookup"><span data-stu-id="0d6dd-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6dd-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d6dd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0d6dd-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0d6dd-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d6dd-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d6dd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0d6dd-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0d6dd-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0d6dd-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0d6dd-136">End of client support</span></span><br/>    | <span data-ttu-id="0d6dd-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d6dd-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0d6dd-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="0d6dd-138">Product</span></span><br/>                  | <span data-ttu-id="0d6dd-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0d6dd-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0d6dd-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d6dd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d6dd-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d6dd-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0d6dd-142">IID</span><span class="sxs-lookup"><span data-stu-id="0d6dd-142">IID</span></span><br/>                      | <span data-ttu-id="0d6dd-143">IID \_ IVMHardDiskconnection è definito come aefa36a5-463A-46AE-9E6C-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="0d6dd-143">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="0d6dd-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d6dd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d6dd-145">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="0d6dd-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

