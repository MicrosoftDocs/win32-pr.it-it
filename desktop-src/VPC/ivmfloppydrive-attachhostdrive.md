---
title: Metodo IVMFloppyDrive AttachHostDrive (VPCCOMInterfaces. h)
description: Connette un'unità fisica nell'host all'unità floppy della macchina virtuale.
ms.assetid: 9be84e06-e38a-419a-be50-dddd0cc6d2dd
keywords:
- Metodo AttachHostDrive Virtual PC
- Metodo AttachHostDrive Virtual PC, interfaccia IVMFloppyDrive
- Interfaccia IVMFloppyDrive Virtual PC, metodo AttachHostDrive
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a21785e3e1e4ec77146f048ab4cce018de9d8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048499"
---
# <a name="ivmfloppydriveattachhostdrive-method"></a><span data-ttu-id="4d1c7-106">Metodo IVMFloppyDrive:: AttachHostDrive</span><span class="sxs-lookup"><span data-stu-id="4d1c7-106">IVMFloppyDrive::AttachHostDrive method</span></span>

<span data-ttu-id="4d1c7-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4d1c7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4d1c7-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4d1c7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4d1c7-109">Connette un'unità fisica nell'host all'unità floppy della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4d1c7-109">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d1c7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d1c7-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="4d1c7-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d1c7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d1c7-112">*LetteraUnità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d1c7-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d1c7-113">Lettera di unità dell'unità floppy fisica del computer host a da collegare.</span><span class="sxs-lookup"><span data-stu-id="4d1c7-113">The drive letter of the physical floppy drive on the host machine to is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d1c7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d1c7-114">Return value</span></span>

<span data-ttu-id="4d1c7-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="4d1c7-115">This method can return one of these values.</span></span>



| <span data-ttu-id="4d1c7-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d1c7-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="4d1c7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d1c7-117">Description</span></span>                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d1c7-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4d1c7-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4d1c7-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4d1c7-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="4d1c7-120"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4d1c7-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="4d1c7-121">Il parametro *LetteraUnità* è **null**, non è un'unità floppy valida oppure il percorso specificato è vuoto.</span><span class="sxs-lookup"><span data-stu-id="4d1c7-121">The *driveLetter* parameter is **NULL**, is not a valid floppy drive, or the given path is empty.</span></span><br/> |
| <dl> <span data-ttu-id="4d1c7-122"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4d1c7-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="4d1c7-123">La configurazione per questa macchina virtuale non è valida o non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="4d1c7-123">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                       |
| <dl> <span data-ttu-id="4d1c7-124"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4d1c7-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4d1c7-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="4d1c7-125">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="4d1c7-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d1c7-126">Requirements</span></span>



| <span data-ttu-id="4d1c7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d1c7-127">Requirement</span></span> | <span data-ttu-id="4d1c7-128">Valore</span><span class="sxs-lookup"><span data-stu-id="4d1c7-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d1c7-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d1c7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4d1c7-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4d1c7-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4d1c7-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d1c7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4d1c7-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4d1c7-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4d1c7-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4d1c7-133">End of client support</span></span><br/>    | <span data-ttu-id="4d1c7-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d1c7-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4d1c7-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="4d1c7-135">Product</span></span><br/>                  | <span data-ttu-id="4d1c7-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4d1c7-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4d1c7-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d1c7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d1c7-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d1c7-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4d1c7-139">IID</span><span class="sxs-lookup"><span data-stu-id="4d1c7-139">IID</span></span><br/>                      | <span data-ttu-id="4d1c7-140">IID \_ IVMFloppyDrive è definito come 661abee6-112A-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="4d1c7-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="4d1c7-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d1c7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d1c7-142">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="4d1c7-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

