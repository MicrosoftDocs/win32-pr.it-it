---
description: Rimuove le subnet della rete di migrazione dal servizio di migrazione del sistema virtuale.
ms.assetid: 6ae8de07-552b-4525-8806-bfb9da73bd42
title: Metodo RemoveNetworkSettings della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.RemoveNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66b7a9fd1ce29d9dd645242ec7cda346f79a6f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307871"
---
# <a name="removenetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="0f878-103">Metodo RemoveNetworkSettings della classe MSVM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="0f878-103">RemoveNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="0f878-104">Rimuove le subnet della rete di migrazione dal servizio di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="0f878-104">Removes migration network subnets from the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f878-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f878-105">Syntax</span></span>


```mof
uint32 RemoveNetworkSettings(
  [in]  Msvm_VirtualSystemMigrationNetworkSettingData REF NetworkSettings[],
  [out] CIM_ConcreteJob                               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0f878-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f878-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f878-107">*NetworkSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f878-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f878-108">Matrice di istanze incorporate della classe [**\_ VirtualSystemMigrationNetworkSettingData MSVM**](msvm-virtualsystemmigrationnetworksettingdata.md) che rappresentano le subnet di rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0f878-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that represent the network subnets to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="0f878-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="0f878-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f878-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f878-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f878-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f878-111">Return value</span></span>

<span data-ttu-id="0f878-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0f878-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0f878-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="0f878-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0f878-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="0f878-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0f878-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="0f878-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0f878-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="0f878-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0f878-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="0f878-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0f878-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="0f878-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0f878-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="0f878-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0f878-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="0f878-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0f878-121">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="0f878-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0f878-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="0f878-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0f878-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="0f878-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0f878-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="0f878-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0f878-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="0f878-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0f878-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f878-126">Requirements</span></span>



| <span data-ttu-id="0f878-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f878-127">Requirement</span></span> | <span data-ttu-id="0f878-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0f878-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f878-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f878-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0f878-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0f878-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0f878-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f878-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0f878-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0f878-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f878-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0f878-133">Namespace</span></span><br/>                | <span data-ttu-id="0f878-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0f878-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0f878-135">MOF</span><span class="sxs-lookup"><span data-stu-id="0f878-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f878-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f878-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f878-137">DLL</span><span class="sxs-lookup"><span data-stu-id="0f878-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f878-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f878-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f878-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f878-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f878-140">**AddNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="0f878-140">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="0f878-141">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="0f878-141">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="0f878-142">**\_VirtualSystemMigrationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="0f878-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

