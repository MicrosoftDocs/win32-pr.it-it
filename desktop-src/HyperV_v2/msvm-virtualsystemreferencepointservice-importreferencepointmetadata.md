---
description: Importa i metadati del punto di riferimento del sistema virtuale.
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Metodo ImportReferencePointMetadata della classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c66a374247d324f5df192114d0b66adc3a17c5b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968954"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="08a25-103">Metodo ImportReferencePointMetadata della classe MSVM \_ VirtualSystemReferencePointService</span><span class="sxs-lookup"><span data-stu-id="08a25-103">ImportReferencePointMetadata method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="08a25-104">Importa i metadati del punto di riferimento del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="08a25-104">Imports reference point metadata of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a25-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08a25-105">Syntax</span></span>


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="08a25-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="08a25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a25-107">*AffectedSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08a25-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a25-108">Riferimento a un [**\_ ComputerSystem MSVM**](msvm-computersystem.md) che descrive il sistema interessato.</span><span class="sxs-lookup"><span data-stu-id="08a25-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) describing the affected system.</span></span>

</dd> <dt>

<span data-ttu-id="08a25-109">*ConfigFilePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08a25-109">*ConfigFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a25-110">Percorso completo del file di configurazione da cui verranno importati i metadati del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="08a25-110">The fully-qualified path of the config file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="08a25-111">*RuntimeStateFilePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08a25-111">*RuntimeStateFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08a25-112">Percorso completo del file di stato di runtime da cui verranno importati i metadati del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="08a25-112">The fully-qualified path of the runtime state file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="08a25-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="08a25-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08a25-114">Parametro facoltativo per il monitoraggio dello stato di avanzamento dell'operazione, che viene utilizzato se non è stato possibile eseguire in modo sincrono il metodo.</span><span class="sxs-lookup"><span data-stu-id="08a25-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="08a25-115">Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.</span><span class="sxs-lookup"><span data-stu-id="08a25-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a25-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08a25-116">Return value</span></span>

<span data-ttu-id="08a25-117">Restituisce 0 (nessun errore) o uno dei messaggi di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="08a25-117">Returns either 0 (no error) or one of the following error messages:</span></span>

<dl> <dt>

<span data-ttu-id="08a25-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="08a25-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08a25-119">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="08a25-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="08a25-120">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="08a25-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="08a25-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="08a25-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="08a25-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="08a25-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="08a25-123">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="08a25-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="08a25-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="08a25-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="08a25-125">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="08a25-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="08a25-126">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="08a25-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="08a25-127">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="08a25-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="08a25-128">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="08a25-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="08a25-129">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="08a25-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="08a25-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="08a25-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="08a25-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08a25-131">Requirements</span></span>



| <span data-ttu-id="08a25-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="08a25-132">Requirement</span></span> | <span data-ttu-id="08a25-133">Valore</span><span class="sxs-lookup"><span data-stu-id="08a25-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a25-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08a25-134">Minimum supported client</span></span><br/> | <span data-ttu-id="08a25-135">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="08a25-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="08a25-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08a25-136">Minimum supported server</span></span><br/> | <span data-ttu-id="08a25-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="08a25-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="08a25-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="08a25-138">Namespace</span></span><br/>                | <span data-ttu-id="08a25-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="08a25-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="08a25-140">MOF</span><span class="sxs-lookup"><span data-stu-id="08a25-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08a25-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08a25-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08a25-142">DLL</span><span class="sxs-lookup"><span data-stu-id="08a25-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08a25-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08a25-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="08a25-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08a25-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a25-145">**\_VirtualSystemReferencePointService MSVM**</span><span class="sxs-lookup"><span data-stu-id="08a25-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




