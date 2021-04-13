---
title: Metodo IVMGuestOS InstallIntegrationComponents (VPCCOMInterfaces. h)
description: Individua e installa i componenti di integrazione più recenti nel sistema operativo guest.
ms.assetid: 06f302b3-ec2b-471a-8e2e-095ed6ecbd3d
keywords:
- Metodo InstallIntegrationComponents Virtual PC
- Metodo InstallIntegrationComponents Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo InstallIntegrationComponents
topic_type:
- apiref
api_name:
- IVMGuestOS.InstallIntegrationComponents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879ded1464ebd310e1d1da4e3a952dc086600350
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400268"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a><span data-ttu-id="b1214-106">Metodo IVMGuestOS:: InstallIntegrationComponents</span><span class="sxs-lookup"><span data-stu-id="b1214-106">IVMGuestOS::InstallIntegrationComponents method</span></span>

<span data-ttu-id="b1214-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b1214-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b1214-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b1214-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b1214-109">Individua e installa i componenti di integrazione più recenti nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="b1214-109">Locates and installs the latest Integration Components into the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1214-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1214-110">Syntax</span></span>


```C++
HRESULT InstallIntegrationComponents();
```



## <a name="parameters"></a><span data-ttu-id="b1214-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1214-111">Parameters</span></span>

<span data-ttu-id="b1214-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b1214-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1214-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1214-113">Return value</span></span>

<span data-ttu-id="b1214-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="b1214-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b1214-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1214-115">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="b1214-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1214-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1214-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b1214-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="b1214-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b1214-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b1214-119"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="b1214-119"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                       | <span data-ttu-id="b1214-120">Per questa operazione è necessario che la macchina virtuale sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b1214-120">The virtual machine must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="b1214-121"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b1214-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="b1214-122">Impossibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b1214-122">The virtual machine could not be found.</span></span><br/>                                     |
| <dl> <span data-ttu-id="b1214-123"><dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b1214-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="b1214-124">La macchina virtuale non dispone di un'unità DVD vuota.</span><span class="sxs-lookup"><span data-stu-id="b1214-124">The virtual machine does not have an empty DVD drive.</span></span><br/>                       |
| <dl> <span data-ttu-id="b1214-125"><dt>**Macchina virtuale \_ E \_ \_ smontaggio supporto \_ 0xA0040508 non riuscito**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b1214-125"><dt>**VM\_E\_MEDIA\_UNMOUNT\_FAIL**</dt> <dt>0xA0040508</dt></span></span> </dl>                   | <span data-ttu-id="b1214-126">Il tentativo di smontare il supporto dall'unità DVD della macchina virtuale non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b1214-126">The attempt to unmount the media from the virtual machine DVD drive failed.</span></span><br/> |
| <dl> <span data-ttu-id="b1214-127"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b1214-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="b1214-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="b1214-128">An unexpected error has occurred.</span></span><br/>                                           |
| <dl> <span data-ttu-id="b1214-129"><dt>**HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="b1214-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="b1214-130">Il sistema non è in grado di trovare il file ISO per i componenti di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b1214-130">The system cannot find the ISO file for the Integration Components.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="b1214-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1214-131">Requirements</span></span>



| <span data-ttu-id="b1214-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1214-132">Requirement</span></span> | <span data-ttu-id="b1214-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b1214-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1214-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1214-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b1214-135">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b1214-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b1214-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1214-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b1214-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b1214-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b1214-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b1214-138">End of client support</span></span><br/>    | <span data-ttu-id="b1214-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b1214-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b1214-140">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b1214-140">Product</span></span><br/>                  | <span data-ttu-id="b1214-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b1214-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b1214-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1214-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1214-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1214-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b1214-144">IID</span><span class="sxs-lookup"><span data-stu-id="b1214-144">IID</span></span><br/>                      | <span data-ttu-id="b1214-145">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="b1214-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b1214-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1214-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1214-147">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="b1214-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

