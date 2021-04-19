---
title: Metodo SetVirtualDesktopState della classe Win32_RDMSVirtualDesktop
description: Aggiorna lo stato del desktop virtuale.
ms.assetid: 8f4f3d31-0434-4018-a33a-2ffd62c09669
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetVirtualDesktopState
- Metodo SetVirtualDesktopState Servizi Desktop remoto, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Servizi Desktop remoto, metodo SetVirtualDesktopState
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetVirtualDesktopState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af913e29857a59cacf283bff6a1642e0ea4cef9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301856"
---
# <a name="setvirtualdesktopstate-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="86042-106">Metodo SetVirtualDesktopState della \_ classe RDMSVirtualDesktop Win32</span><span class="sxs-lookup"><span data-stu-id="86042-106">SetVirtualDesktopState method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="86042-107">Aggiorna lo stato del desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="86042-107">Updates the state of the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="86042-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86042-108">Syntax</span></span>


```mof
uint32 SetVirtualDesktopState(
  [in] uint32 VMState
);
```



## <a name="parameters"></a><span data-ttu-id="86042-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="86042-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86042-110">*VMState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86042-110">*VMState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86042-111">Valore che specifica il nuovo stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="86042-111">A value that specifies the new state of the virtual machine.</span></span>

<span data-ttu-id="86042-112">Questo parametro può scommettere su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="86042-112">This parameter can bet set to one of the following values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="86042-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0 (impostazione predefinita))</span><span class="sxs-lookup"><span data-stu-id="86042-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0 (Default))</span></span>


</dt> <dd>

<span data-ttu-id="86042-114">Non è stato possibile determinare lo stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="86042-114">The state of the virtual machine could not be determined.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="86042-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="86042-115"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="86042-116">La macchina virtuale è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="86042-116">The virtual machine is running.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="86042-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="86042-117"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="86042-118">La macchina virtuale è disattivata.</span><span class="sxs-lookup"><span data-stu-id="86042-118">The virtual machine is turned off.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="86042-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Sospeso** (32768)</span><span class="sxs-lookup"><span data-stu-id="86042-119"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="86042-120">La macchina virtuale è sospesa.</span><span class="sxs-lookup"><span data-stu-id="86042-120">The virtual machine is paused.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="86042-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Sospeso** (32769)</span><span class="sxs-lookup"><span data-stu-id="86042-121"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="86042-122">La macchina virtuale si trova in uno stato salvato.</span><span class="sxs-lookup"><span data-stu-id="86042-122">The virtual machine is in a saved state.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="86042-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** di (32770)</span><span class="sxs-lookup"><span data-stu-id="86042-123"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="86042-124">Avvio della macchina virtuale in corso.</span><span class="sxs-lookup"><span data-stu-id="86042-124">The virtual machine is starting.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="86042-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Salvataggio** (32773)</span><span class="sxs-lookup"><span data-stu-id="86042-125"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="86042-126">Lo stato della macchina virtuale è salvato.</span><span class="sxs-lookup"><span data-stu-id="86042-126">The virtual machine is saving its state.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="86042-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (32774)</span><span class="sxs-lookup"><span data-stu-id="86042-127"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (32774)</span></span>


</dt> <dd>

<span data-ttu-id="86042-128">La macchina virtuale è disattivata.</span><span class="sxs-lookup"><span data-stu-id="86042-128">The virtual machine is turning off.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="86042-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Sospensione** (32776)</span><span class="sxs-lookup"><span data-stu-id="86042-129"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="86042-130">La macchina virtuale è in pausa.</span><span class="sxs-lookup"><span data-stu-id="86042-130">The virtual machine is pausing.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="86042-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Ripresa** in (32777)</span><span class="sxs-lookup"><span data-stu-id="86042-131"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="86042-132">La macchina virtuale riprende da uno stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="86042-132">The virtual machine is resuming from a paused state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86042-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86042-133">Return value</span></span>

<span data-ttu-id="86042-134">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="86042-134">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="86042-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86042-135">Requirements</span></span>



| <span data-ttu-id="86042-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="86042-136">Requirement</span></span> | <span data-ttu-id="86042-137">Valore</span><span class="sxs-lookup"><span data-stu-id="86042-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="86042-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86042-138">Minimum supported client</span></span><br/> | <span data-ttu-id="86042-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="86042-139">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="86042-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86042-140">Minimum supported server</span></span><br/> | <span data-ttu-id="86042-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="86042-141">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="86042-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="86042-142">Namespace</span></span><br/>                | <span data-ttu-id="86042-143">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="86042-143">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="86042-144">MOF</span><span class="sxs-lookup"><span data-stu-id="86042-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86042-145"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86042-145"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="86042-146">DLL</span><span class="sxs-lookup"><span data-stu-id="86042-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86042-147"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86042-147"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="86042-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86042-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86042-149">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="86042-149">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





