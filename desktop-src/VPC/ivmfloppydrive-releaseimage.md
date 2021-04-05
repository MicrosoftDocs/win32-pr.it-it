---
title: Metodo IVMFloppyDrive ReleaseImage (VPCCOMInterfaces. h)
description: Rilascia un'immagine di supporti floppy nell'host dall'unità floppy.
ms.assetid: 12fc6dc4-8450-4122-b0f0-ed11cc10134c
keywords:
- Metodo ReleaseImage Virtual PC
- Metodo ReleaseImage Virtual PC, interfaccia IVMFloppyDrive
- Interfaccia IVMFloppyDrive Virtual PC, metodo ReleaseImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece899bbb615fc2d54a3cbdc86193e743168ef23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739767"
---
# <a name="ivmfloppydrivereleaseimage-method"></a><span data-ttu-id="68776-106">Metodo IVMFloppyDrive:: ReleaseImage</span><span class="sxs-lookup"><span data-stu-id="68776-106">IVMFloppyDrive::ReleaseImage method</span></span>

<span data-ttu-id="68776-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="68776-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="68776-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="68776-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="68776-109">Rilascia un'immagine di supporti floppy nell'host dall'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="68776-109">Releases a floppy media image on the host from the floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="68776-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68776-110">Syntax</span></span>


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a><span data-ttu-id="68776-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="68776-111">Parameters</span></span>

<span data-ttu-id="68776-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="68776-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68776-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68776-113">Return value</span></span>

<span data-ttu-id="68776-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="68776-114">This method can return one of these values.</span></span>



| <span data-ttu-id="68776-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="68776-115">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="68776-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68776-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68776-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="68776-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="68776-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="68776-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="68776-119"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="68776-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>          | <span data-ttu-id="68776-120">La configurazione per questa macchina virtuale non è valida o non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="68776-120">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="68776-121"><dt>**Macchina virtuale \_ E \_ media \_ di \_ tipo errato**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="68776-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl>  | <span data-ttu-id="68776-122">Il supporto collegato a questa unità floppy non è un'immagine di disco floppy.</span><span class="sxs-lookup"><span data-stu-id="68776-122">The media attached to this floppy drive is not a floppy disk image.</span></span><br/>         |
| <dl> <span data-ttu-id="68776-123"><dt>**Macchina virtuale \_ E \_ nessun \_ supporto \_ acquisito**</dt> <dt>0xA00400652</dt></span><span class="sxs-lookup"><span data-stu-id="68776-123"><dt>**VM\_E\_NO\_MEDIA\_CAPTURED**</dt> <dt>0xA00400652</dt></span></span> </dl> | <span data-ttu-id="68776-124">Nessun supporto collegato a questa unità floppy.</span><span class="sxs-lookup"><span data-stu-id="68776-124">There is no media attached to this floppy drive.</span></span><br/>                            |
| <dl> <span data-ttu-id="68776-125"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="68776-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="68776-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="68776-126">An unexpected error has occurred.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="68776-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68776-127">Requirements</span></span>



| <span data-ttu-id="68776-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="68776-128">Requirement</span></span> | <span data-ttu-id="68776-129">Valore</span><span class="sxs-lookup"><span data-stu-id="68776-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="68776-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68776-130">Minimum supported client</span></span><br/> | <span data-ttu-id="68776-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="68776-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68776-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68776-132">Minimum supported server</span></span><br/> | <span data-ttu-id="68776-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="68776-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="68776-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="68776-134">End of client support</span></span><br/>    | <span data-ttu-id="68776-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="68776-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="68776-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="68776-136">Product</span></span><br/>                  | <span data-ttu-id="68776-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="68776-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="68776-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68776-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="68776-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="68776-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="68776-140">IID</span><span class="sxs-lookup"><span data-stu-id="68776-140">IID</span></span><br/>                      | <span data-ttu-id="68776-141">IID \_ IVMFloppyDrive è definito come 661abee6-112A-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="68776-141">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="68776-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68776-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68776-143">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="68776-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

