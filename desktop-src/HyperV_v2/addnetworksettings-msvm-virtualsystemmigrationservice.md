---
description: Aggiunge le subnet della rete di migrazione per il servizio migrazione del sistema virtuale.
ms.assetid: b0e0f187-beeb-4fdf-a91c-f6c5500f0f6d
title: Metodo AddNetworkSettings della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.AddNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 75d168b1a49d8ac44ab66ba9da13d1e598c647b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312342"
---
# <a name="addnetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="b0e2e-103">Metodo AddNetworkSettings della classe MSVM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="b0e2e-103">AddNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="b0e2e-104">Aggiunge le subnet della rete di migrazione per il servizio migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="b0e2e-104">Adds migration network subnets for the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e2e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0e2e-105">Syntax</span></span>


```mof
uint32 AddNetworkSettings(
  [in]  string              NetworkSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b0e2e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0e2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e2e-107">*NetworkSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0e2e-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e2e-108">Matrice di istanze incorporate della classe [**\_ VirtualSystemMigrationNetworkSettingData MSVM**](msvm-virtualsystemmigrationnetworksettingdata.md) che contengono le impostazioni della rete di migrazione.</span><span class="sxs-lookup"><span data-stu-id="b0e2e-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that contain the migration network settings.</span></span>

</dd> <dt>

<span data-ttu-id="b0e2e-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="b0e2e-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e2e-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0e2e-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e2e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0e2e-111">Return value</span></span>

<span data-ttu-id="b0e2e-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b0e2e-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b0e2e-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0e2e-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b0e2e-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b0e2e-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b0e2e-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b0e2e-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b0e2e-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b0e2e-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b0e2e-121">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b0e2e-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b0e2e-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b0e2e-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b0e2e-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b0e2e-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b0e2e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0e2e-126">Requirements</span></span>



| <span data-ttu-id="b0e2e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0e2e-127">Requirement</span></span> | <span data-ttu-id="b0e2e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b0e2e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e2e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0e2e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e2e-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b0e2e-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b0e2e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0e2e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e2e-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b0e2e-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0e2e-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b0e2e-133">Namespace</span></span><br/>                | <span data-ttu-id="b0e2e-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b0e2e-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b0e2e-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b0e2e-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0e2e-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0e2e-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0e2e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b0e2e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0e2e-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b0e2e-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b0e2e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0e2e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0e2e-140">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="b0e2e-140">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="b0e2e-141">**RemoveNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="b0e2e-141">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="b0e2e-142">**\_VirtualSystemMigrationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="b0e2e-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

