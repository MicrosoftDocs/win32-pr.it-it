---
title: Metodo IVMFloppyDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Rilascia un'unità fisica nell'host dall'unità floppy.
ms.assetid: 6d5a8e7c-684c-42bc-84e5-76d3e761b7f0
keywords:
- Metodo ReleaseHostDrive Virtual PC
- Metodo ReleaseHostDrive Virtual PC, interfaccia IVMFloppyDrive
- Interfaccia IVMFloppyDrive Virtual PC, metodo ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ab726ba87dd978a21c4f27b20437926e07c19b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739770"
---
# <a name="ivmfloppydrivereleasehostdrive-method"></a><span data-ttu-id="eb549-106">Metodo IVMFloppyDrive:: ReleaseHostDrive</span><span class="sxs-lookup"><span data-stu-id="eb549-106">IVMFloppyDrive::ReleaseHostDrive method</span></span>

<span data-ttu-id="eb549-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="eb549-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="eb549-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="eb549-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="eb549-109">Rilascia un'unità fisica nell'host dall'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="eb549-109">Releases a physical drive on the host from the floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb549-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb549-110">Syntax</span></span>


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a><span data-ttu-id="eb549-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb549-111">Parameters</span></span>

<span data-ttu-id="eb549-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="eb549-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb549-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb549-113">Return value</span></span>

<span data-ttu-id="eb549-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="eb549-114">This method can return one of these values.</span></span>



| <span data-ttu-id="eb549-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb549-115">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="eb549-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb549-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb549-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eb549-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="eb549-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="eb549-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="eb549-119"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="eb549-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>          | <span data-ttu-id="eb549-120">La configurazione per questa macchina virtuale non è valida o non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="eb549-120">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="eb549-121"><dt>**Macchina virtuale \_ E \_ media \_ di \_ tipo errato**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="eb549-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl>  | <span data-ttu-id="eb549-122">Il supporto collegato a questa unità floppy non è un'unità floppy fisica.</span><span class="sxs-lookup"><span data-stu-id="eb549-122">The media attached to this floppy drive is not a physical floppy drive.</span></span><br/>     |
| <dl> <span data-ttu-id="eb549-123"><dt>**Macchina virtuale \_ E \_ nessun \_ supporto \_ acquisito**</dt> <dt>0xA00400652</dt></span><span class="sxs-lookup"><span data-stu-id="eb549-123"><dt>**VM\_E\_NO\_MEDIA\_CAPTURED**</dt> <dt>0xA00400652</dt></span></span> </dl> | <span data-ttu-id="eb549-124">Nessun supporto collegato a questa unità floppy.</span><span class="sxs-lookup"><span data-stu-id="eb549-124">There is no media attached to this floppy drive.</span></span><br/>                            |
| <dl> <span data-ttu-id="eb549-125"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="eb549-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="eb549-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="eb549-126">An unexpected error has occurred.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="eb549-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb549-127">Requirements</span></span>



| <span data-ttu-id="eb549-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb549-128">Requirement</span></span> | <span data-ttu-id="eb549-129">Valore</span><span class="sxs-lookup"><span data-stu-id="eb549-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb549-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb549-130">Minimum supported client</span></span><br/> | <span data-ttu-id="eb549-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="eb549-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb549-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb549-132">Minimum supported server</span></span><br/> | <span data-ttu-id="eb549-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="eb549-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="eb549-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="eb549-134">End of client support</span></span><br/>    | <span data-ttu-id="eb549-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eb549-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="eb549-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="eb549-136">Product</span></span><br/>                  | <span data-ttu-id="eb549-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="eb549-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="eb549-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb549-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb549-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb549-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="eb549-140">IID</span><span class="sxs-lookup"><span data-stu-id="eb549-140">IID</span></span><br/>                      | <span data-ttu-id="eb549-141">IID \_ IVMFloppyDrive è definito come 661abee6-112A-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="eb549-141">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="eb549-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb549-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb549-143">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="eb549-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

