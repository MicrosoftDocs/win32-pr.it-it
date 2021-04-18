---
description: Modifica i dati delle impostazioni di merge del disco.
ms.assetid: 91775dc5-105a-4e38-a334-fb34dd4e59f8
title: Metodo ModifyDiskMergeSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyDiskMergeSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe737c084b4c1c76a411ce1d2eba513554b40f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313862"
---
# <a name="modifydiskmergesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="955c4-103">Metodo ModifyDiskMergeSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="955c4-103">ModifyDiskMergeSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="955c4-104">Modifica i dati delle impostazioni di merge del disco.</span><span class="sxs-lookup"><span data-stu-id="955c4-104">Modifies the disk merge setting data.</span></span>

## <a name="syntax"></a><span data-ttu-id="955c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="955c4-105">Syntax</span></span>


```mof
uint32 ModifyDiskMergeSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="955c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="955c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="955c4-107">*SettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="955c4-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="955c4-108">Istanza incorporata della classe [**\_ DiskMergeSettingData MSVM**](msvm-diskmergesettingdata.md) che contiene i dati di impostazione modificati per la funzione di merge del disco.</span><span class="sxs-lookup"><span data-stu-id="955c4-108">An embedded instance of the [**Msvm\_DiskMergeSettingData**](msvm-diskmergesettingdata.md) class that contains modified setting data for the disk merge function.</span></span>

</dd> <dt>

<span data-ttu-id="955c4-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="955c4-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="955c4-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="955c4-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="955c4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="955c4-111">Return value</span></span>

<span data-ttu-id="955c4-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="955c4-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="955c4-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="955c4-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="955c4-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="955c4-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="955c4-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="955c4-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="955c4-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="955c4-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="955c4-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="955c4-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="955c4-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="955c4-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="955c4-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="955c4-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="955c4-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="955c4-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="955c4-121">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="955c4-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="955c4-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="955c4-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="955c4-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="955c4-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="955c4-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="955c4-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="955c4-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="955c4-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="955c4-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="955c4-126">Requirements</span></span>



| <span data-ttu-id="955c4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="955c4-127">Requirement</span></span> | <span data-ttu-id="955c4-128">Valore</span><span class="sxs-lookup"><span data-stu-id="955c4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="955c4-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="955c4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="955c4-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="955c4-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="955c4-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="955c4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="955c4-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="955c4-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="955c4-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="955c4-133">Namespace</span></span><br/>                | <span data-ttu-id="955c4-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="955c4-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="955c4-135">MOF</span><span class="sxs-lookup"><span data-stu-id="955c4-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="955c4-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="955c4-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="955c4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="955c4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="955c4-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="955c4-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="955c4-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="955c4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="955c4-140">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="955c4-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

