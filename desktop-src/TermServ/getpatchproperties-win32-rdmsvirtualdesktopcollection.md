---
title: Metodo GetPatchProperties della classe Win32_RDMSVirtualDesktopCollection
description: Recupera le proprietà di un processo di provisioning degli aggiornamenti software per le macchine virtuali in un insieme di desktop virtuali.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetPatchProperties
- Metodo GetPatchProperties Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo GetPatchProperties
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f0ca45c97512818aa5f8a9ea851d18fa5554c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518184"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="8b7a6-106">Metodo GetPatchProperties della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="8b7a6-106">GetPatchProperties method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="8b7a6-107">Recupera le proprietà di un processo di provisioning degli aggiornamenti software per le macchine virtuali in un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-107">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b7a6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b7a6-108">Syntax</span></span>


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a><span data-ttu-id="8b7a6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b7a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b7a6-110">*StartTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b7a6-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7a6-111">Data e ora in cui installare gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-111">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="8b7a6-112">*ForceLogOffTime* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b7a6-112">*ForceLogOffTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7a6-113">Data e ora in cui il sistema disconnetterà gli utenti delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-113">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="8b7a6-114">*JobGuid* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b7a6-114">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7a6-115">**GUID** che identifica in modo univoco il processo di provisioning.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-115">A **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="8b7a6-116">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="8b7a6-116">*State* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7a6-117">Stato del processo di provisioning.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-117">The state of the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b7a6-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b7a6-118">Return value</span></span>

<span data-ttu-id="8b7a6-119">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b7a6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b7a6-120">Requirements</span></span>



| <span data-ttu-id="8b7a6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b7a6-121">Requirement</span></span> | <span data-ttu-id="8b7a6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8b7a6-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b7a6-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b7a6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8b7a6-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8b7a6-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8b7a6-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b7a6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8b7a6-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b7a6-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="8b7a6-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8b7a6-127">Namespace</span></span><br/>                | <span data-ttu-id="8b7a6-128">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="8b7a6-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8b7a6-129">MOF</span><span class="sxs-lookup"><span data-stu-id="8b7a6-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b7a6-130"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b7a6-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b7a6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8b7a6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b7a6-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b7a6-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8b7a6-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b7a6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b7a6-134">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="8b7a6-134">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





