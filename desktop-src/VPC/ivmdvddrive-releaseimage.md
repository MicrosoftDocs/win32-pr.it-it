---
title: Metodo IVMDVDDrive ReleaseImage (VPCCOMInterfaces. h)
description: Rilascia un'immagine ISO acquisita dall'unità DVD.
ms.assetid: 7cc95cf3-9d25-495f-863c-8eddd4068835
keywords:
- Metodo ReleaseImage Virtual PC
- Metodo ReleaseImage Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, metodo ReleaseImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a36a13b258d155760269399d9f25f5eda6f296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475448"
---
# <a name="ivmdvddrivereleaseimage-method"></a><span data-ttu-id="1cfba-106">Metodo IVMDVDDrive:: ReleaseImage</span><span class="sxs-lookup"><span data-stu-id="1cfba-106">IVMDVDDrive::ReleaseImage method</span></span>

<span data-ttu-id="1cfba-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1cfba-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1cfba-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1cfba-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1cfba-109">Rilascia un'immagine ISO acquisita dall'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="1cfba-109">Releases a captured ISO image from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cfba-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cfba-110">Syntax</span></span>


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a><span data-ttu-id="1cfba-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cfba-111">Parameters</span></span>

<span data-ttu-id="1cfba-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1cfba-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cfba-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cfba-113">Return value</span></span>

<span data-ttu-id="1cfba-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="1cfba-114">This method can return one of these values.</span></span>



| <span data-ttu-id="1cfba-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cfba-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="1cfba-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cfba-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1cfba-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1cfba-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="1cfba-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="1cfba-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="1cfba-119"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1cfba-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="1cfba-120">Impossibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1cfba-120">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="1cfba-121"><dt>**Macchina virtuale \_ E \_ media \_ di \_ tipo errato**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="1cfba-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="1cfba-122">Il supporto attualmente acquisito non è un'unità disco host.</span><span class="sxs-lookup"><span data-stu-id="1cfba-122">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="1cfba-123"><dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1cfba-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="1cfba-124">Non è stato possibile inizializzare l'unità a causa di una posizione del bus non valida.</span><span class="sxs-lookup"><span data-stu-id="1cfba-124">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="1cfba-125"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1cfba-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="1cfba-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1cfba-126">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="1cfba-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cfba-127">Requirements</span></span>



| <span data-ttu-id="1cfba-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cfba-128">Requirement</span></span> | <span data-ttu-id="1cfba-129">Valore</span><span class="sxs-lookup"><span data-stu-id="1cfba-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cfba-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cfba-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1cfba-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1cfba-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1cfba-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cfba-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1cfba-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1cfba-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1cfba-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1cfba-134">End of client support</span></span><br/>    | <span data-ttu-id="1cfba-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1cfba-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1cfba-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="1cfba-136">Product</span></span><br/>                  | <span data-ttu-id="1cfba-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1cfba-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1cfba-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cfba-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cfba-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cfba-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1cfba-140">IID</span><span class="sxs-lookup"><span data-stu-id="1cfba-140">IID</span></span><br/>                      | <span data-ttu-id="1cfba-141">IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="1cfba-141">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="1cfba-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cfba-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cfba-143">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="1cfba-143">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

