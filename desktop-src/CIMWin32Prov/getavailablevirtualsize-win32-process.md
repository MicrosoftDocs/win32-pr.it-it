---
description: Recupera le dimensioni correnti, in byte, dello spazio degli indirizzi virtuali libero disponibile per il processo.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Metodo GetAvailableVirtualSize della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304689"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a><span data-ttu-id="8f78b-103">Metodo GetAvailableVirtualSize della classe di \_ processo Win32</span><span class="sxs-lookup"><span data-stu-id="8f78b-103">GetAvailableVirtualSize method of the Win32\_Process class</span></span>

<span data-ttu-id="8f78b-104">Recupera le dimensioni correnti, in byte, dello spazio degli indirizzi virtuali libero disponibile per il processo.</span><span class="sxs-lookup"><span data-stu-id="8f78b-104">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f78b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f78b-105">Syntax</span></span>


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a><span data-ttu-id="8f78b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f78b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f78b-107">*AvailableVirtualSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8f78b-107">*AvailableVirtualSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f78b-108">Il parametro *AvailableVirtualSize* restituisce lo spazio degli indirizzi virtuali libero disponibile per questo processo.</span><span class="sxs-lookup"><span data-stu-id="8f78b-108">The *AvailableVirtualSize* parameter returns the free virtual address space available to this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f78b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f78b-109">Return value</span></span>

<span data-ttu-id="8f78b-110">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8f78b-110">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="8f78b-111">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="8f78b-111">Any other number indicates an error.</span></span> <span data-ttu-id="8f78b-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8f78b-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8f78b-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8f78b-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8f78b-114">**Operazione completata**</span><span class="sxs-lookup"><span data-stu-id="8f78b-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="8f78b-115">0</span><span class="sxs-lookup"><span data-stu-id="8f78b-115">0</span></span>

<span data-ttu-id="8f78b-116">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="8f78b-116">The operation completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="8f78b-117">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="8f78b-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8f78b-118">2</span><span class="sxs-lookup"><span data-stu-id="8f78b-118">2</span></span>

<span data-ttu-id="8f78b-119">L'utente non ha accesso alle informazioni richieste</span><span class="sxs-lookup"><span data-stu-id="8f78b-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="8f78b-120">**Privilegio insufficiente**</span><span class="sxs-lookup"><span data-stu-id="8f78b-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="8f78b-121">3</span><span class="sxs-lookup"><span data-stu-id="8f78b-121">3</span></span>

<span data-ttu-id="8f78b-122">L'utente non dispone di privilegi sufficienti.</span><span class="sxs-lookup"><span data-stu-id="8f78b-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="8f78b-123">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="8f78b-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8f78b-124">8</span><span class="sxs-lookup"><span data-stu-id="8f78b-124">8</span></span>

<span data-ttu-id="8f78b-125">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="8f78b-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8f78b-126">**Impossibile trovare il percorso**</span><span class="sxs-lookup"><span data-stu-id="8f78b-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="8f78b-127">9</span><span class="sxs-lookup"><span data-stu-id="8f78b-127">9</span></span>

<span data-ttu-id="8f78b-128">Il percorso specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="8f78b-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="8f78b-129">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="8f78b-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8f78b-130">21</span><span class="sxs-lookup"><span data-stu-id="8f78b-130">21</span></span>

<span data-ttu-id="8f78b-131">Il parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="8f78b-131">The specified parameter is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="8f78b-132">**Altri**</span><span class="sxs-lookup"><span data-stu-id="8f78b-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8f78b-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="8f78b-133">22 4294967295</span></span>

<span data-ttu-id="8f78b-134">Per i valori diversi da quelli elencati, fare riferimento alla documentazione relativa ai [codici di errore di sistema](/windows/desktop/Debug/system-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="8f78b-134">For values other than those listed, refer to the [System Error Codes](/windows/desktop/Debug/system-error-codes) documentation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f78b-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f78b-135">Requirements</span></span>



| <span data-ttu-id="8f78b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f78b-136">Requirement</span></span> | <span data-ttu-id="8f78b-137">Valore</span><span class="sxs-lookup"><span data-stu-id="8f78b-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f78b-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f78b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8f78b-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8f78b-139">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="8f78b-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f78b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8f78b-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8f78b-141">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="8f78b-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8f78b-142">Namespace</span></span><br/>                | <span data-ttu-id="8f78b-143">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8f78b-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f78b-144">MOF</span><span class="sxs-lookup"><span data-stu-id="8f78b-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f78b-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f78b-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f78b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8f78b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f78b-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f78b-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f78b-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f78b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f78b-149">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="8f78b-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

