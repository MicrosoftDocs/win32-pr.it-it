---
description: Modifica i dati dell'impostazione per il servizio di migrazione.
ms.assetid: 5162fe88-dd39-4fe0-b8e9-e9b70c2b6a5c
title: Metodo ModifyServiceSettings della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e1e9dc96196752ec4408939adc418e7c43bc0c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315489"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="85cd8-103">Metodo ModifyServiceSettings della classe MSVM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="85cd8-103">ModifyServiceSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="85cd8-104">Modifica i dati dell'impostazione per il servizio di migrazione.</span><span class="sxs-lookup"><span data-stu-id="85cd8-104">Modifies the setting data for the migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="85cd8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85cd8-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="85cd8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85cd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85cd8-107">*ServiceSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85cd8-108">Istanza incorporata della classe [**\_ VirtualSystemManagementServiceSettingData MSVM**](msvm-virtualsystemmanagementservicesettingdata.md) che contiene le nuove impostazioni del servizio.</span><span class="sxs-lookup"><span data-stu-id="85cd8-108">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the new service settings.</span></span>

</dd> <dt>

<span data-ttu-id="85cd8-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85cd8-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85cd8-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85cd8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85cd8-111">Return value</span></span>

<span data-ttu-id="85cd8-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="85cd8-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="85cd8-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="85cd8-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85cd8-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="85cd8-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="85cd8-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="85cd8-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="85cd8-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="85cd8-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="85cd8-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="85cd8-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="85cd8-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="85cd8-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="85cd8-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="85cd8-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="85cd8-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="85cd8-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="85cd8-121">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="85cd8-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="85cd8-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="85cd8-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="85cd8-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="85cd8-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="85cd8-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="85cd8-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="85cd8-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="85cd8-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="85cd8-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85cd8-126">Requirements</span></span>



| <span data-ttu-id="85cd8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="85cd8-127">Requirement</span></span> | <span data-ttu-id="85cd8-128">Valore</span><span class="sxs-lookup"><span data-stu-id="85cd8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85cd8-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85cd8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="85cd8-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="85cd8-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85cd8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="85cd8-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="85cd8-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85cd8-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="85cd8-133">Namespace</span></span><br/>                | <span data-ttu-id="85cd8-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="85cd8-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="85cd8-135">MOF</span><span class="sxs-lookup"><span data-stu-id="85cd8-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85cd8-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85cd8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="85cd8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85cd8-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85cd8-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="85cd8-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85cd8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85cd8-140">**\_VirtualSystemMigrationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="85cd8-140">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

