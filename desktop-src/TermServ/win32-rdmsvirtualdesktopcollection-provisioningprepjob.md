---
title: Metodo ProvisioningPrepJob della classe Win32_RDMSVirtualDesktopCollection
description: Consente di creare un processo di provisioning di desktop virtuale.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ProvisioningPrepJob
- Metodo ProvisioningPrepJob Servizi Desktop remoto, interfaccia Win32_RDMSVirtualDesktopCollection
- Interfaccia Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo ProvisioningPrepJob
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9727dec0e31dd199f324ed01a4510041ba3558f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964135"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="2aced-106">Metodo ProvisioningPrepJob della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="2aced-106">ProvisioningPrepJob method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="2aced-107">Consente di creare un processo di provisioning di desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="2aced-107">Creates a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aced-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2aced-108">Syntax</span></span>


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="2aced-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2aced-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aced-110">*CollectionAlias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aced-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aced-111">Alias della raccolta che ospita il desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="2aced-111">The alias of the collection that hosts the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="2aced-112">*VMHostName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aced-112">*VMHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aced-113">Nome host della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2aced-113">The virtual machine host name.</span></span>

</dd> <dt>

<span data-ttu-id="2aced-114">*VMName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aced-114">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aced-115">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2aced-115">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2aced-116">*ExportToLocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aced-116">*ExportToLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aced-117">Percorso completo della posizione in cui esportare il processo di provisioning.</span><span class="sxs-lookup"><span data-stu-id="2aced-117">The full path the location to export the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="2aced-118">*bSysPrep* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aced-118">*bSysPrep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aced-119">Indica se il processo di provisioning rappresenta una distribuzione di Sysprep.</span><span class="sxs-lookup"><span data-stu-id="2aced-119">Indicates whether the provisioning job represents a Sysprep deployment.</span></span>

</dd> <dt>

<span data-ttu-id="2aced-120">*Nomecomputer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aced-120">*MachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aced-121">Nome del computer che ospita la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2aced-121">The machine name of the computer that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2aced-122">*Nome utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aced-122">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aced-123">Nome utente dell'amministratore della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2aced-123">The user name of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2aced-124">*Password* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2aced-124">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aced-125">Password dell'amministratore della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2aced-125">The password of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2aced-126">*JobGuid* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2aced-126">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aced-127">**GUID** che identifica in modo univoco il processo di provisioning.</span><span class="sxs-lookup"><span data-stu-id="2aced-127">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aced-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2aced-128">Return value</span></span>

<span data-ttu-id="2aced-129">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="2aced-129">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aced-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2aced-130">Requirements</span></span>



| <span data-ttu-id="2aced-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2aced-131">Requirement</span></span> | <span data-ttu-id="2aced-132">Valore</span><span class="sxs-lookup"><span data-stu-id="2aced-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aced-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2aced-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2aced-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2aced-134">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2aced-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2aced-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2aced-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2aced-136">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="2aced-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2aced-137">Namespace</span></span><br/>                | <span data-ttu-id="2aced-138">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="2aced-138">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2aced-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2aced-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2aced-140"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2aced-140"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2aced-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2aced-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2aced-142"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2aced-142"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2aced-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2aced-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aced-144">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="2aced-144">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





