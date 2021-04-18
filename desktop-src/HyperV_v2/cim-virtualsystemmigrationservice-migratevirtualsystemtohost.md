---
description: Metodo per spostare, migrare o rilocare un sistema virtuale in un host di destinazione specificato da un nome di rete o un indirizzo IP.
ms.assetid: 09fdc0b2-641c-47f5-b270-e26e3acf7ea5
title: Metodo MigrateVirtualSystemToHost della classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1a90e3adadbb5efc5f9cae3b7710e07c1e05000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311138"
---
# <a name="migratevirtualsystemtohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="20ed6-103">Metodo MigrateVirtualSystemToHost della classe CIM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="20ed6-103">MigrateVirtualSystemToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="20ed6-104">Metodo per spostare, migrare o rilocare un sistema virtuale in un host di destinazione specificato da un nome di rete o un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="20ed6-104">Method to move, migrate or relocate a virtual system to a target host specified by a network name or IP address.</span></span>

> [!Note]  
> <span data-ttu-id="20ed6-105">Questo metodo è concepito come una soluzione di transizione solo fino a quando non è disponibile la modellazione del supporto cluster.</span><span class="sxs-lookup"><span data-stu-id="20ed6-105">This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="20ed6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20ed6-106">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="20ed6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="20ed6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20ed6-108">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20ed6-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ed6-109">Sistema del computer virtuale di origine da migrare.</span><span class="sxs-lookup"><span data-stu-id="20ed6-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="20ed6-110">*DestinationHost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20ed6-110">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ed6-111">Sistema host di destinazione per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="20ed6-111">Target host system for the migration.</span></span>

<span data-ttu-id="20ed6-112">I formati accettabili per questo parametro vengono trasmessi tramite valori di elementi della  \[ \] proprietà della matrice DestinationHostFormatsSupported nell'istanza del [**\_ VirtualSystemMigrationCapabilities CIM**](cim-virtualsystemmigrationcapabilities.md) associata tramite l'associazione [**CIM \_ ElementCapabilities**](cim-elementcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="20ed6-112">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="20ed6-113">*MigrationSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20ed6-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ed6-114">Stringa contenente un'istanza incorporata della classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) che rappresenta le impostazioni di migrazione applicabili all'operazione di migrazione.</span><span class="sxs-lookup"><span data-stu-id="20ed6-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="20ed6-115">*NewSystemSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20ed6-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ed6-116">Stringa contenente un'istanza incorporata della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che rappresenta le nuove proprietà applicabili al sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="20ed6-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="20ed6-117">*NewResourceSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20ed6-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ed6-118">Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali nell'ambito del sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="20ed6-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="20ed6-119">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="20ed6-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20ed6-120">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito facoltativamente un [**\_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo.</span><span class="sxs-lookup"><span data-stu-id="20ed6-120">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20ed6-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20ed6-121">Return value</span></span>

<span data-ttu-id="20ed6-122">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="20ed6-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="20ed6-123">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="20ed6-123">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="20ed6-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20ed6-124">Description</span></span>                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20ed6-125"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="20ed6-126">Migrazione del sistema virtuale completata.</span><span class="sxs-lookup"><span data-stu-id="20ed6-126">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="20ed6-127"><dt>**Non supportato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="20ed6-128">Metodo non supportato dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="20ed6-128">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="20ed6-129"><dt>**Operazione non riuscita**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-129"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="20ed6-130">La migrazione del sistema virtuale non è riuscita per motivi non specificati.</span><span class="sxs-lookup"><span data-stu-id="20ed6-130">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="20ed6-131"><dt>**Timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-131"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="20ed6-132">Timeout della migrazione del sistema virtuale; lo stato del sistema virtuale è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="20ed6-132">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="20ed6-133"><dt>**Parametro 4 non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-133"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="20ed6-134">Uno o più parametri non sono formalmente validi.</span><span class="sxs-lookup"><span data-stu-id="20ed6-134">One or more parameters are formally invalid.</span></span> <span data-ttu-id="20ed6-135">Il valore del parametro *DestinationHost* , ad esempio, potrebbe essere stato specificato in un formato non supportato.</span><span class="sxs-lookup"><span data-stu-id="20ed6-135">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="20ed6-136"><dt>**Stato non valido**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="20ed6-137">Il sistema virtuale di origine, il sistema host di origine o il sistema host di destinazione si trovano in uno stato che consente l'avvio della migrazione del sistema virtuale richiesta. potrebbe trattarsi di una condizione temporanea.</span><span class="sxs-lookup"><span data-stu-id="20ed6-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="20ed6-138"><dt>**Parametri incompatibili**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="20ed6-139">Uno o più parametri di input sono incompatibili come set o per quanto riguarda l'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="20ed6-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="20ed6-140">Il valore del parametro *MigrationNewSettingData* , ad esempio, contiene proprietà che non sono supportate dal sistema host di destinazione identificato dal valore del parametro *DestinationHost* .</span><span class="sxs-lookup"><span data-stu-id="20ed6-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="20ed6-141"><dt>**DMTF riservato**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="20ed6-142"><dt>**Parametri del metodo controllati-processo avviato**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="20ed6-143"><dt>**Metodo riservato**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="20ed6-144">32768 <dt>**specifici del fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="20ed6-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20ed6-145">Requirements</span></span>



| <span data-ttu-id="20ed6-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="20ed6-146">Requirement</span></span> | <span data-ttu-id="20ed6-147">Valore</span><span class="sxs-lookup"><span data-stu-id="20ed6-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ed6-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20ed6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="20ed6-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="20ed6-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="20ed6-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20ed6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="20ed6-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="20ed6-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="20ed6-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="20ed6-152">Namespace</span></span><br/>                | <span data-ttu-id="20ed6-153">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="20ed6-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="20ed6-154">MOF</span><span class="sxs-lookup"><span data-stu-id="20ed6-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20ed6-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20ed6-156">DLL</span><span class="sxs-lookup"><span data-stu-id="20ed6-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20ed6-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20ed6-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="20ed6-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20ed6-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ed6-159">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="20ed6-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




