---
title: Metodo IVMGuestOS GetOsVersionInfo (VPCCOMInterfaces. h)
description: Recupera le informazioni sulla versione per il sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- Metodo GetOsVersionInfo Virtual PC
- Metodo GetOsVersionInfo Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo GetOsVersionInfo
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec0c0c2516a8ef16a3d9d9c6c4178abb31bd52f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302561"
---
# <a name="ivmguestosgetosversioninfo-method"></a><span data-ttu-id="4104f-106">Metodo IVMGuestOS:: GetOsVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4104f-106">IVMGuestOS::GetOsVersionInfo method</span></span>

<span data-ttu-id="4104f-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4104f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4104f-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4104f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4104f-109">Recupera le informazioni sulla versione per il sistema operativo guest in esecuzione nella macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="4104f-109">Retrieves version information for the guest operating system running in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="4104f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4104f-110">Syntax</span></span>


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4104f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4104f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4104f-112">*guestOsVersionInfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4104f-112">*guestOsVersionInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4104f-113">Puntatore a una struttura [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) .</span><span class="sxs-lookup"><span data-stu-id="4104f-113">A pointer to a [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4104f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4104f-114">Return value</span></span>

<span data-ttu-id="4104f-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="4104f-115">This method can return one of these values.</span></span>



| <span data-ttu-id="4104f-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="4104f-116">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="4104f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4104f-117">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4104f-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4104f-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="4104f-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4104f-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="4104f-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4104f-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="4104f-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="4104f-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="4104f-122"><dt>**HRESULT \_ DA \_ Win32 (Error \_ OutOfMemory)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="4104f-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="4104f-123">La memoria disponibile non è sufficiente per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4104f-123">There is not enough memory available to complete this request.</span></span><br/> |
| <dl> <span data-ttu-id="4104f-124"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4104f-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="4104f-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="4104f-125">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="4104f-126"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="4104f-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="4104f-127">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4104f-127">The VM is not running.</span></span><br/>                                         |
| <dl> <span data-ttu-id="4104f-128"><dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="4104f-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="4104f-129">I componenti di integrazione non sono installati in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4104f-129">Integration components are not installed in this VM.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="4104f-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4104f-130">Requirements</span></span>



| <span data-ttu-id="4104f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4104f-131">Requirement</span></span> | <span data-ttu-id="4104f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4104f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4104f-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4104f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4104f-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4104f-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4104f-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4104f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4104f-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4104f-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4104f-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4104f-137">End of client support</span></span><br/>    | <span data-ttu-id="4104f-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4104f-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4104f-139">Prodotto</span><span class="sxs-lookup"><span data-stu-id="4104f-139">Product</span></span><br/>                  | <span data-ttu-id="4104f-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4104f-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4104f-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4104f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4104f-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4104f-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4104f-143">IID</span><span class="sxs-lookup"><span data-stu-id="4104f-143">IID</span></span><br/>                      | <span data-ttu-id="4104f-144">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="4104f-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="4104f-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4104f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4104f-146">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="4104f-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

