---
description: Metodo per spostare, migrare o rilocare un sistema virtuale in un sistema di destinazione.
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: Metodo MigrateVirtualSystemToSystem della classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1459d80785725914cbaa5dda5b81e8d2fabad5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881218"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="67448-103">Metodo MigrateVirtualSystemToSystem della classe CIM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="67448-103">MigrateVirtualSystemToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="67448-104">Metodo per spostare, migrare o rilocare un sistema virtuale in un sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="67448-104">Method to move, migrate or relocate a virtual system to a target system.</span></span>

<span data-ttu-id="67448-105">Descrizione del codice restituito:</span><span class="sxs-lookup"><span data-stu-id="67448-105">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="67448-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67448-106">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="67448-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="67448-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67448-108">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67448-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67448-109">Sistema del computer virtuale di origine da migrare.</span><span class="sxs-lookup"><span data-stu-id="67448-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="67448-110">*DestinationSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67448-110">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67448-111">Messere di sistema host di destinazione migrare il sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="67448-111">Destination host system whereto migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="67448-112">*MigrationSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67448-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67448-113">Stringa contenente un'istanza incorporata della classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) che rappresenta le impostazioni di migrazione applicabili all'operazione di migrazione.</span><span class="sxs-lookup"><span data-stu-id="67448-113">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="67448-114">*NewSystemSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67448-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67448-115">Stringa contenente un'istanza incorporata della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che rappresenta le nuove proprietà applicabili al sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="67448-115">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="67448-116">*NewResourceSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67448-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67448-117">Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali nell'ambito del sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="67448-117">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="67448-118">*NewComputerSystem* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="67448-118">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67448-119">Riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta il sistema di computer virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="67448-119">Reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class representing the virtual computer system after it has been migrated.</span></span>

</dd> <dt>

<span data-ttu-id="67448-120">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="67448-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67448-121">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito facoltativamente un [**\_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo.</span><span class="sxs-lookup"><span data-stu-id="67448-121">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67448-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67448-122">Return value</span></span>

<span data-ttu-id="67448-123">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="67448-123">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="67448-124">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="67448-124">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="67448-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67448-125">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="67448-126"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="67448-126"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="67448-127">Migrazione del sistema virtuale completata.</span><span class="sxs-lookup"><span data-stu-id="67448-127">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="67448-128"><dt>**Non supportato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="67448-128"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="67448-129">Metodo non supportato dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="67448-129">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="67448-130"><dt>**Operazione non riuscita**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="67448-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="67448-131">La migrazione del sistema virtuale non è riuscita per motivi non specificati.</span><span class="sxs-lookup"><span data-stu-id="67448-131">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="67448-132"><dt>**Timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="67448-132"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="67448-133">Timeout della migrazione del sistema virtuale; lo stato del sistema virtuale è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="67448-133">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="67448-134"><dt>**Parametro 4 non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="67448-134"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="67448-135">Uno o più parametri non sono formalmente validi, ad esempio, il valore del parametro di sistema di destinazione non contiene un percorso di oggetto valido.</span><span class="sxs-lookup"><span data-stu-id="67448-135">One or more parameters are formally invalid For example, the value of the Destination System parameter does not contain a valid object path.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="67448-136"><dt>**Stato non valido**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="67448-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="67448-137">Il sistema virtuale di origine, il sistema host di origine o il sistema host di destinazione si trovano in uno stato che consente l'avvio della migrazione del sistema virtuale richiesta. potrebbe trattarsi di una condizione temporanea.</span><span class="sxs-lookup"><span data-stu-id="67448-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="67448-138"><dt>**Parametri incompatibili**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="67448-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="67448-139">Uno o più parametri di input sono incompatibili come set o per quanto riguarda l'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="67448-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="67448-140">Il valore del parametro *MigrationNewSettingData* , ad esempio, contiene proprietà che non sono supportate dal sistema host di destinazione identificato dal valore del parametro *DestinationSystem* .</span><span class="sxs-lookup"><span data-stu-id="67448-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="67448-141"><dt>**DMTF riservato**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="67448-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="67448-142"><dt>**Parametri del metodo controllati-processo avviato**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="67448-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="67448-143"><dt>**Metodo riservato**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="67448-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="67448-144">32768 <dt>**specifici del fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="67448-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="67448-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67448-145">Requirements</span></span>



| <span data-ttu-id="67448-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="67448-146">Requirement</span></span> | <span data-ttu-id="67448-147">Valore</span><span class="sxs-lookup"><span data-stu-id="67448-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67448-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67448-148">Minimum supported client</span></span><br/> | <span data-ttu-id="67448-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="67448-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="67448-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67448-150">Minimum supported server</span></span><br/> | <span data-ttu-id="67448-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="67448-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="67448-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="67448-152">Namespace</span></span><br/>                | <span data-ttu-id="67448-153">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="67448-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="67448-154">MOF</span><span class="sxs-lookup"><span data-stu-id="67448-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67448-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67448-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67448-156">DLL</span><span class="sxs-lookup"><span data-stu-id="67448-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67448-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67448-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67448-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67448-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67448-159">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="67448-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




