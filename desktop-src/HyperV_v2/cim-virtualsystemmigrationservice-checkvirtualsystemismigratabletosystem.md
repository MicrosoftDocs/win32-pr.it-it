---
description: 'Altre informazioni su: Metodo CheckVirtualSystemIsMigratableToSystem della classe CIM_VirtualSystemMigrationService'
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: Metodo CheckVirtualSystemIsMigratableToSystem della classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: be85c51cb507fea3cea14f1706ffa8f67af06c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311139"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="e3bc9-103">Metodo CheckVirtualSystemIsMigratableToSystem della classe CIM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="e3bc9-103">CheckVirtualSystemIsMigratableToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="e3bc9-104">Metodo per eseguire un controllo preliminare per determinare se è probabile che un sistema virtuale venga migrato correttamente a un sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target system.</span></span> <span data-ttu-id="e3bc9-105">Questo metodo non garantisce che una migrazione successiva avrà sempre esito positivo, a causa della disponibilità dinamica delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span> <span data-ttu-id="e3bc9-106">Descrizione del codice restituito:</span><span class="sxs-lookup"><span data-stu-id="e3bc9-106">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="e3bc9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3bc9-107">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="e3bc9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3bc9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3bc9-109">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3bc9-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3bc9-110">[**CIM \_**](cim-computersystem.md) Istanza di ComputerSystem che fa riferimento al sistema del computer virtuale di origine da migrare.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-110">[**CIM\_ComputerSystem**](cim-computersystem.md) instance referencing the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e3bc9-111">*DestinationSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3bc9-111">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3bc9-112">[**CIM \_**](cim-system.md) Istanza di sistema che fa riferimento al sistema di destinazione su cui eseguire la migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-112">[**CIM\_System**](cim-system.md) instance referencing the destination system onto which to migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="e3bc9-113">*MigrationSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3bc9-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3bc9-114">Stringa contenente un'istanza incorporata della classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) che rappresenta le impostazioni di migrazione applicabili all'operazione di migrazione.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="e3bc9-115">*NewSystemSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3bc9-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3bc9-116">Stringa contenente un'istanza incorporata della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che rappresenta le nuove proprietà applicabili al sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e3bc9-117">*NewResourceSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3bc9-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3bc9-118">Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali nell'ambito del sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e3bc9-119">*IsMigratable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e3bc9-119">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3bc9-120">Risultato del controllo della migrazione che indica se è possibile eseguire la migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-120">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3bc9-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3bc9-121">Return value</span></span>

<span data-ttu-id="e3bc9-122">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="e3bc9-123">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3bc9-123">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="e3bc9-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3bc9-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e3bc9-125"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e3bc9-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="e3bc9-126">Controllo eseguito; risultato restituito tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="e3bc9-126">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="e3bc9-127"><dt>**Non supportato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e3bc9-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="e3bc9-128">Metodo non supportato dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-128">Method not supported by implementation.</span></span> <span data-ttu-id="e3bc9-129">Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="e3bc9-129">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="e3bc9-130"><dt>**Operazione non riuscita**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e3bc9-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="e3bc9-131">Controllo non riuscito per motivi non specificati.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-131">Check failed for unspecified reasons.</span></span> <span data-ttu-id="e3bc9-132">Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="e3bc9-132">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="e3bc9-133"><dt>**Timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e3bc9-133"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="e3bc9-134">Timeout del controllo. Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="e3bc9-134">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="e3bc9-135"><dt>**Parametro 4 non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e3bc9-135"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="e3bc9-136">Uno o più parametri non sono formalmente validi.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-136">One or more parameters are formally invalid.</span></span> <span data-ttu-id="e3bc9-137">Il valore del parametro *DestinationSystem* , ad esempio, non è costituito da un percorso di oggetto valido.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-137">For example, the value of the *DestinationSystem* parameter does not comprise a valid object path.</span></span> <span data-ttu-id="e3bc9-138">Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="e3bc9-138">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="e3bc9-139"><dt>**Stato non valido**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e3bc9-139"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="e3bc9-140">Il sistema virtuale di origine, il sistema host di origine o il sistema host di destinazione si trovano in uno stato che consente l'avvio della migrazione del sistema virtuale richiesta. potrebbe trattarsi di una condizione temporanea.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-140">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="e3bc9-141">Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="e3bc9-141">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="e3bc9-142"><dt>**Parametri incompatibili**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e3bc9-142"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="e3bc9-143">Uno o più parametri di input sono incompatibili come set o per quanto riguarda l'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e3bc9-143">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="e3bc9-144">Il valore del parametro *NewSettingData* , ad esempio, contiene proprietà che non sono supportate dal sistema host di destinazione identificato dal valore del parametro *DestinationSystem* .</span><span class="sxs-lookup"><span data-stu-id="e3bc9-144">For example the value of the *NewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span> <span data-ttu-id="e3bc9-145">Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="e3bc9-145">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="e3bc9-146"><dt>**DMTF riservato**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="e3bc9-146"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="e3bc9-147"><dt>**Metodo riservato**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="e3bc9-147"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="e3bc9-148">32768 <dt>**specifici del fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="e3bc9-148"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="e3bc9-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3bc9-149">Requirements</span></span>



| <span data-ttu-id="e3bc9-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3bc9-150">Requirement</span></span> | <span data-ttu-id="e3bc9-151">Valore</span><span class="sxs-lookup"><span data-stu-id="e3bc9-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3bc9-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3bc9-152">Minimum supported client</span></span><br/> | <span data-ttu-id="e3bc9-153">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e3bc9-153">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e3bc9-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3bc9-154">Minimum supported server</span></span><br/> | <span data-ttu-id="e3bc9-155">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e3bc9-155">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e3bc9-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e3bc9-156">Namespace</span></span><br/>                | <span data-ttu-id="e3bc9-157">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e3bc9-157">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e3bc9-158">MOF</span><span class="sxs-lookup"><span data-stu-id="e3bc9-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3bc9-159"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3bc9-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3bc9-160">DLL</span><span class="sxs-lookup"><span data-stu-id="e3bc9-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3bc9-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e3bc9-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e3bc9-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3bc9-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3bc9-163">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e3bc9-163">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




