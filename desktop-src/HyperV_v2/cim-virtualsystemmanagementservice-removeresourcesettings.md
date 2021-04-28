---
description: 'Metodo RemoveResourceSettings della classe CIM_VirtualSystemManagementService : rimuove le impostazioni delle risorse virtuali da una configurazione di sistema virtuale.'
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: Metodo RemoveResourceSettings della CIM_VirtualSystemManagementService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e5c7daabcdcd732c3a5693664e1768ebf66668d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112259"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="83688-103">Metodo RemoveResourceSettings della classe CIM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="83688-103">RemoveResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="83688-104">Rimuove le impostazioni delle risorse virtuali da una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="83688-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="83688-105">Se applicato a parti di una configurazione di sistema virtuale "corrente", come effetto collaterale le risorse del sistema virtuale attivo possono essere rimosse.</span><span class="sxs-lookup"><span data-stu-id="83688-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="83688-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83688-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="83688-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="83688-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83688-108">*ResourceSettings* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="83688-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83688-109">Matrice di riferimenti a istanze della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) in cui ogni istanza rappresenta le impostazioni di una risorsa virtuale all'interno di una configurazione di sistema virtuale che devono essere rimosse.</span><span class="sxs-lookup"><span data-stu-id="83688-109">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) where each instance represents the settings of a virtual resource within a virtual system configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="83688-110">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="83688-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83688-111">Se l'operazione è a esecuzione lunga, facoltativamente può essere restituito un [**processo \_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo.</span><span class="sxs-lookup"><span data-stu-id="83688-111">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83688-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83688-112">Return value</span></span>

<span data-ttu-id="83688-113">Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="83688-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="83688-114">**Completata senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="83688-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="83688-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="83688-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="83688-116">**Operazione non** riuscita (2)</span><span class="sxs-lookup"><span data-stu-id="83688-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="83688-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="83688-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="83688-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="83688-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="83688-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="83688-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="83688-120">**DmTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="83688-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="83688-121">**Parametri del metodo verificati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="83688-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="83688-122">**Metodo riservato** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="83688-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="83688-123">**Specifico del** fornitore (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="83688-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="83688-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83688-124">Requirements</span></span>



| <span data-ttu-id="83688-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="83688-125">Requirement</span></span> | <span data-ttu-id="83688-126">Valore</span><span class="sxs-lookup"><span data-stu-id="83688-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83688-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83688-127">Minimum supported client</span></span><br/> | <span data-ttu-id="83688-128">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="83688-128">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="83688-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83688-129">Minimum supported server</span></span><br/> | <span data-ttu-id="83688-130">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="83688-130">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="83688-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="83688-131">Namespace</span></span><br/>                | <span data-ttu-id="83688-132">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="83688-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="83688-133">MOF</span><span class="sxs-lookup"><span data-stu-id="83688-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83688-134"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="83688-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="83688-135">DLL</span><span class="sxs-lookup"><span data-stu-id="83688-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83688-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83688-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="83688-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83688-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83688-138">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="83688-138">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




