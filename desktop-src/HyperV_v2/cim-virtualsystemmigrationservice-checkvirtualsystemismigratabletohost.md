---
description: Metodo per eseguire un controllo preliminare per determinare se è probabile che un sistema virtuale venga migrato correttamente a un host di destinazione specificato da un nome di rete o un indirizzo IP.
ms.assetid: bfcd4063-30fe-4d18-9df9-7b84a680814c
title: Metodo CheckVirtualSystemIsMigratableToHost della classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5769691a792b8f74225b640b0058ad4bd0e27c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311140"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="5de7b-103">Metodo CheckVirtualSystemIsMigratableToHost della classe CIM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="5de7b-103">CheckVirtualSystemIsMigratableToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="5de7b-104">Metodo per eseguire un controllo preliminare per determinare se è probabile che un sistema virtuale venga migrato correttamente a un host di destinazione specificato da un nome di rete o un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="5de7b-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target host specified by a network name or IP address.</span></span> <span data-ttu-id="5de7b-105">Questo metodo non garantisce che una migrazione successiva avrà sempre esito positivo, a causa della disponibilità dinamica delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5de7b-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span>

<span data-ttu-id="5de7b-106">Descrizione del codice restituito:</span><span class="sxs-lookup"><span data-stu-id="5de7b-106">Return code description:</span></span>

<span data-ttu-id="5de7b-107">Nota: questo metodo è concepito come una soluzione di transizione solo fino a quando non è disponibile la modellazione del supporto cluster.</span><span class="sxs-lookup"><span data-stu-id="5de7b-107">Note: This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="5de7b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5de7b-108">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="5de7b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5de7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5de7b-110">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5de7b-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de7b-111">Riferimento [**CIM \_ ComputerSystem**](cim-computersystem.md) al sistema del computer virtuale di origine da migrare.</span><span class="sxs-lookup"><span data-stu-id="5de7b-111">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="5de7b-112">*DestinationHost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5de7b-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de7b-113">Sistema host di destinazione per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="5de7b-113">Target host system for the migration.</span></span>

<span data-ttu-id="5de7b-114">I formati accettabili per questo parametro vengono trasmessi tramite valori di elementi della  \[ \] proprietà della matrice DestinationHostFormatsSupported nell'istanza del [**\_ VirtualSystemMigrationCapabilities CIM**](cim-virtualsystemmigrationcapabilities.md) associata tramite l'associazione [**CIM \_ ElementCapabilities**](cim-elementcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="5de7b-114">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="5de7b-115">*MigrationSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5de7b-115">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de7b-116">Stringa contenente un'istanza incorporata della classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) che rappresenta le impostazioni di migrazione applicabili all'operazione di migrazione.</span><span class="sxs-lookup"><span data-stu-id="5de7b-116">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="5de7b-117">*NewSystemSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5de7b-117">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de7b-118">Stringa contenente un'istanza incorporata della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che rappresenta le nuove proprietà applicabili al sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="5de7b-118">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="5de7b-119">*NewResourceSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5de7b-119">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de7b-120">Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali nell'ambito del sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="5de7b-120">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="5de7b-121">*IsMigratable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5de7b-121">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5de7b-122">Risultato del controllo della migrazione che indica se è possibile eseguire la migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="5de7b-122">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5de7b-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5de7b-123">Return value</span></span>

<span data-ttu-id="5de7b-124">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="5de7b-124">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="5de7b-125">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="5de7b-125">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="5de7b-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5de7b-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5de7b-127"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5de7b-127"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="5de7b-128">Controllo eseguito; risultato restituito tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="5de7b-128">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="5de7b-129"><dt>**Non supportato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5de7b-129"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="5de7b-130">Metodo non supportato dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="5de7b-130">Method not supported by implementation.</span></span> <span data-ttu-id="5de7b-131">Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="5de7b-131">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="5de7b-132"><dt>**Operazione non riuscita**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5de7b-132"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="5de7b-133">Controllo non riuscito per motivi non specificati.</span><span class="sxs-lookup"><span data-stu-id="5de7b-133">Check failed for unspecified reasons.</span></span> <span data-ttu-id="5de7b-134">Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="5de7b-134">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="5de7b-135"><dt>**Timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5de7b-135"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="5de7b-136">Timeout del controllo. Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="5de7b-136">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="5de7b-137"><dt>**Parametro 4 non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5de7b-137"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="5de7b-138">Uno o più parametri non sono formalmente validi.</span><span class="sxs-lookup"><span data-stu-id="5de7b-138">One or more parameters are formally invalid.</span></span> <span data-ttu-id="5de7b-139">Il valore del parametro *DestinationHost* , ad esempio, potrebbe essere stato specificato in un formato non supportato.</span><span class="sxs-lookup"><span data-stu-id="5de7b-139">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span> <span data-ttu-id="5de7b-140">Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="5de7b-140">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="5de7b-141"><dt>**Stato non valido**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5de7b-141"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="5de7b-142">Il sistema virtuale di origine, il sistema host di origine o il sistema host di destinazione si trovano in uno stato che consente l'avvio della migrazione del sistema virtuale richiesta. potrebbe trattarsi di una condizione temporanea.</span><span class="sxs-lookup"><span data-stu-id="5de7b-142">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="5de7b-143">Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="5de7b-143">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="5de7b-144"><dt>**Parametri incompatibili**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5de7b-144"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="5de7b-145">Uno o più parametri di input sono incompatibili come set o per quanto riguarda l'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5de7b-145">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="5de7b-146">Il valore del parametro *MigrationNewSettingData* , ad esempio, contiene proprietà che non sono supportate dal sistema host di destinazione identificato dal valore del parametro *DestinationHost* .</span><span class="sxs-lookup"><span data-stu-id="5de7b-146">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span> <span data-ttu-id="5de7b-147">Nessun risultato segnalato tramite il valore del \[ parametro out \] *IsMigratable* .</span><span class="sxs-lookup"><span data-stu-id="5de7b-147">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="5de7b-148"><dt>**DMTF riservato**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="5de7b-148"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="5de7b-149"><dt>**Metodo riservato**</dt> <dt>4097.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="5de7b-149"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="5de7b-150">32768 <dt>**specifici del fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="5de7b-150"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="5de7b-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5de7b-151">Requirements</span></span>



| <span data-ttu-id="5de7b-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="5de7b-152">Requirement</span></span> | <span data-ttu-id="5de7b-153">Valore</span><span class="sxs-lookup"><span data-stu-id="5de7b-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5de7b-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5de7b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="5de7b-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5de7b-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5de7b-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5de7b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="5de7b-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5de7b-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5de7b-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5de7b-158">Namespace</span></span><br/>                | <span data-ttu-id="5de7b-159">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5de7b-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5de7b-160">MOF</span><span class="sxs-lookup"><span data-stu-id="5de7b-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5de7b-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5de7b-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5de7b-162">DLL</span><span class="sxs-lookup"><span data-stu-id="5de7b-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5de7b-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5de7b-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5de7b-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5de7b-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de7b-165">**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="5de7b-165">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




