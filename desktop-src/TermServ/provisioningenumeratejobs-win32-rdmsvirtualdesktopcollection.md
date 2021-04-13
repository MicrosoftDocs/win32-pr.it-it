---
title: Metodo ProvisioningEnumerateJobs della classe Win32_RDMSVirtualDesktopCollection
description: Enumera i processi di provisioning del desktop virtuale per questo servizio.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ProvisioningEnumerateJobs
- Metodo ProvisioningEnumerateJobs Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo ProvisioningEnumerateJobs
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa2b54a0599c2bbcaf6b0f9a9acb3ab3028389b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518999"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="b96fa-106">Metodo ProvisioningEnumerateJobs della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="b96fa-106">ProvisioningEnumerateJobs method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="b96fa-107">Enumera i processi di provisioning del desktop virtuale per questo servizio.</span><span class="sxs-lookup"><span data-stu-id="b96fa-107">Enumerates virtual desktop provisioning jobs for this service.</span></span>

## <a name="syntax"></a><span data-ttu-id="b96fa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b96fa-108">Syntax</span></span>


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a><span data-ttu-id="b96fa-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b96fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b96fa-110">*Tipoprocesso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b96fa-110">*JobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b96fa-111">Integer che specifica il tipo di processo da enumerare.</span><span class="sxs-lookup"><span data-stu-id="b96fa-111">An integer that specifies the type of job to enumerate.</span></span>

<span data-ttu-id="b96fa-112">Questo parametro può essere impostato su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b96fa-112">This parameter can be set to one of the following values:</span></span>

<dt>

<span data-ttu-id="b96fa-113">0</span><span class="sxs-lookup"><span data-stu-id="b96fa-113">0</span></span>
</dt> <dd>

<span data-ttu-id="b96fa-114">Processi in esecuzione</span><span class="sxs-lookup"><span data-stu-id="b96fa-114">Running jobs</span></span>

</dd> <dt>

<span data-ttu-id="b96fa-115">1</span><span class="sxs-lookup"><span data-stu-id="b96fa-115">1</span></span>
</dt> <dd>

<span data-ttu-id="b96fa-116">Processi completati</span><span class="sxs-lookup"><span data-stu-id="b96fa-116">Completed jobs</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b96fa-117">*CollectionAlias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b96fa-117">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b96fa-118">Alias dell'insieme di desktop virtuali da enumerare.</span><span class="sxs-lookup"><span data-stu-id="b96fa-118">The alias of the virtual desktop collection to enumerate.</span></span> <span data-ttu-id="b96fa-119">Il valore predefinito per questo parametro è FALSE, che specifica che tutti i processi in esecuzione devono essere enumerati.</span><span class="sxs-lookup"><span data-stu-id="b96fa-119">The default value for this parameter is FALSE, which specifies that all running jobs are to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="b96fa-120">*JobGuids* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b96fa-120">*JobGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b96fa-121">Matrice contenente i **GUID** dei processi di provisioning da enumerare.</span><span class="sxs-lookup"><span data-stu-id="b96fa-121">An array that contains the **GUIDs** of provisioning jobs to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b96fa-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b96fa-122">Return value</span></span>

<span data-ttu-id="b96fa-123">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="b96fa-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b96fa-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b96fa-124">Requirements</span></span>



| <span data-ttu-id="b96fa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b96fa-125">Requirement</span></span> | <span data-ttu-id="b96fa-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b96fa-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b96fa-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b96fa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b96fa-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b96fa-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b96fa-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b96fa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b96fa-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b96fa-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b96fa-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b96fa-131">Namespace</span></span><br/>                | <span data-ttu-id="b96fa-132">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="b96fa-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b96fa-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b96fa-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b96fa-134"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b96fa-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b96fa-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b96fa-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b96fa-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b96fa-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b96fa-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b96fa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b96fa-138">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="b96fa-138">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





