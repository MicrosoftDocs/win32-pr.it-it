---
title: Metodo GetProvisioningProperties della classe Win32_RDMSCollectionProperties
description: Recupera le proprietà di provisioning dell'insieme di desktop virtuali.
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetProvisioningProperties
- Metodo GetProvisioningProperties Servizi Desktop remoto, classe Win32_RDMSCollectionProperties
- Classe Win32_RDMSCollectionProperties Servizi Desktop remoto, metodo GetProvisioningProperties
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ca58f82d2918441e5da3cf53d442497c1a6a2eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301994"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a><span data-ttu-id="6e225-106">Metodo GetProvisioningProperties della \_ classe RDMSCollectionProperties Win32</span><span class="sxs-lookup"><span data-stu-id="6e225-106">GetProvisioningProperties method of the Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="6e225-107">Recupera le proprietà di provisioning dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="6e225-107">Retrieves the provisioning properties of the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e225-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e225-108">Syntax</span></span>


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a><span data-ttu-id="6e225-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e225-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e225-110">*PoolVhdType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e225-110">*PoolVhdType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e225-111">Specifica il formato del disco rigido virtuale (VHD) del pool di macchine virtuali nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6e225-111">Specifies the VHD (virtual hard disk) format of the virtual machine pool in the collection.</span></span>

<dt>

<span data-ttu-id="6e225-112">Clone</span><span class="sxs-lookup"><span data-stu-id="6e225-112">Clone</span></span>
</dt> <dd>

<span data-ttu-id="6e225-113">VHD clonato.</span><span class="sxs-lookup"><span data-stu-id="6e225-113">A cloned VHD.</span></span>

</dd> <dt>

<span data-ttu-id="6e225-114">DiffDisk</span><span class="sxs-lookup"><span data-stu-id="6e225-114">DiffDisk</span></span>
</dt> <dd>

<span data-ttu-id="6e225-115">Disco rigido virtuale differenze.</span><span class="sxs-lookup"><span data-stu-id="6e225-115">A differencing VHD.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6e225-116">*MasterVmLocation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e225-116">*MasterVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e225-117">Riceve il percorso dell'immagine della macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="6e225-117">Receives the path to the master VM image.</span></span>

</dd> <dt>

<span data-ttu-id="6e225-118">*NamePrefix* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e225-118">*NamePrefix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e225-119">Riceve il prefisso del nome da accodare all'inizio dei nomi delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="6e225-119">Receives the name prefix to append to the beginning of virtual machine names.</span></span>

</dd> <dt>

<span data-ttu-id="6e225-120">*NameStartIndex* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e225-120">*NameStartIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e225-121">Indice iniziale.</span><span class="sxs-lookup"><span data-stu-id="6e225-121">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="6e225-122">*LocalVmLocation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e225-122">*LocalVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e225-123">Riceve il percorso locale delle macchine virtuali nei server Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="6e225-123">Receives the local path to the virtual machines on the Hyper-V servers.</span></span> <span data-ttu-id="6e225-124">Se questo parametro è impostato su **null** o se è vuoto, verrà usata la directory predefinita della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e225-124">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="6e225-125">*LocalGoldVmLocation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e225-125">*LocalGoldVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e225-126">Riceve il percorso locale dell'immagine del disco rigido virtuale dorato quando il parametro *PoolVhdTpe* è impostato su "DiffDisk".</span><span class="sxs-lookup"><span data-stu-id="6e225-126">Receives the local path to the golden VHD image when the *PoolVhdTpe* parameter is set to "DiffDisk".</span></span> <span data-ttu-id="6e225-127">Se questo parametro è impostato su **null** o se è vuoto, verrà usata la directory predefinita della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6e225-127">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="6e225-128">*RunFromSMB* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e225-128">*RunFromSMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e225-129">Riceve un valore che indica se eseguire la raccolta da una condivisione SMB (Server Message Block).</span><span class="sxs-lookup"><span data-stu-id="6e225-129">Receives a value that indicates whether to run the collection from an Server Message Block (SMB) share.</span></span> <span data-ttu-id="6e225-130">**True** per eseguire le macchine virtuali da una condivisione SBM; in caso contrario **False**.</span><span class="sxs-lookup"><span data-stu-id="6e225-130">**TRUE** to run the virtual machines from an SBM share; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6e225-131">*SMBLocation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e225-131">*SMBLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e225-132">Riceve il percorso della condivisione SMB se è abilitata la condivisione SMB.</span><span class="sxs-lookup"><span data-stu-id="6e225-132">Receives the path to the SMB share if SMB sharing is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="6e225-133">*SMBStreaming* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e225-133">*SMBStreaming* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e225-134">Riceve un valore che indica se il flusso SMB è abilitato.</span><span class="sxs-lookup"><span data-stu-id="6e225-134">Receives a value that indicates whether SMB streaming is enabled.</span></span> <span data-ttu-id="6e225-135">**True** se è abilitata la condivisione SMB. in caso contrario **False**.</span><span class="sxs-lookup"><span data-stu-id="6e225-135">**TRUE** if SMB sharing is enabled; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6e225-136">*VmDomain* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e225-136">*VmDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e225-137">Riceve il nome di dominio delle macchine virtuali nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6e225-137">Receives the domain name of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="6e225-138">*VmOU* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e225-138">*VmOU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e225-139">Riceve l'unità organizzativa Active Directory delle macchine virtuali nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6e225-139">Receives the Active Directory organization unit (OU) of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="6e225-140">*ProductKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e225-140">*ProductKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e225-141">Riceve i codici Product Key del sistema operativo per le macchine virtuali nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="6e225-141">Receives the OS product keys for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e225-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e225-142">Return value</span></span>

<span data-ttu-id="6e225-143">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="6e225-143">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e225-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e225-144">Requirements</span></span>



| <span data-ttu-id="6e225-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e225-145">Requirement</span></span> | <span data-ttu-id="6e225-146">Valore</span><span class="sxs-lookup"><span data-stu-id="6e225-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e225-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e225-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6e225-148">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6e225-148">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6e225-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e225-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6e225-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e225-150">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6e225-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6e225-151">Namespace</span></span><br/>                | <span data-ttu-id="6e225-152">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="6e225-152">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6e225-153">MOF</span><span class="sxs-lookup"><span data-stu-id="6e225-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e225-154"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e225-154"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e225-155">DLL</span><span class="sxs-lookup"><span data-stu-id="6e225-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e225-156"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e225-156"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6e225-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e225-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e225-158">**\_RDMSCollectionProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="6e225-158">**Win32\_RDMSCollectionProperties**</span></span>](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





