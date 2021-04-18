---
description: Esporta il punto di riferimento del sistema virtuale.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Metodo ExportReferencePoint della classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bedd051123e4f75d7438b2e3831a84204ff4aec3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320638"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="21116-103">Metodo ExportReferencePoint della classe MSVM \_ VirtualSystemReferencePointService</span><span class="sxs-lookup"><span data-stu-id="21116-103">ExportReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="21116-104">Esporta il punto di riferimento del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="21116-104">Exports the reference point of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="21116-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21116-105">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="21116-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="21116-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21116-107">*ReferencePoint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21116-107">*ReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21116-108">Riferimento all'istanza di [**\_ VirtualSystemReferencePoint MSVM**](msvm-virtualsystemreferencepoint.md) che rappresenta il punto di riferimento da esportare.</span><span class="sxs-lookup"><span data-stu-id="21116-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="21116-109">*ExportDirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21116-109">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21116-110">Percorso completo della directory in cui deve essere esportato il punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="21116-110">The fully-qualified path of the directory to which the reference point is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="21116-111">*ExportSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21116-111">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21116-112">Istanza di [**MSVM \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) che rappresenta le impostazioni per l'operazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="21116-112">An instance of [**Msvm\_VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="21116-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="21116-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21116-114">Parametro facoltativo per il monitoraggio dello stato di avanzamento dell'operazione, che viene utilizzato se non è stato possibile eseguire in modo sincrono il metodo.</span><span class="sxs-lookup"><span data-stu-id="21116-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="21116-115">Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.</span><span class="sxs-lookup"><span data-stu-id="21116-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21116-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21116-116">Return value</span></span>

<span data-ttu-id="21116-117">In caso di esito positivo, restituisce 0 (completa senza errori) o 4096 (processo avviato); in caso contrario, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="21116-117">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="21116-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="21116-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="21116-119">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="21116-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="21116-120">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="21116-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="21116-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="21116-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="21116-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="21116-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="21116-123">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="21116-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="21116-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="21116-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="21116-125">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="21116-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="21116-126">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="21116-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="21116-127">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="21116-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="21116-128">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="21116-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="21116-129">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="21116-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="21116-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="21116-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="21116-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21116-131">Requirements</span></span>



| <span data-ttu-id="21116-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="21116-132">Requirement</span></span> | <span data-ttu-id="21116-133">Valore</span><span class="sxs-lookup"><span data-stu-id="21116-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21116-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21116-134">Minimum supported client</span></span><br/> | <span data-ttu-id="21116-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="21116-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="21116-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21116-136">Minimum supported server</span></span><br/> | <span data-ttu-id="21116-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="21116-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="21116-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21116-138">Namespace</span></span><br/>                | <span data-ttu-id="21116-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="21116-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="21116-140">MOF</span><span class="sxs-lookup"><span data-stu-id="21116-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21116-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21116-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="21116-142">DLL</span><span class="sxs-lookup"><span data-stu-id="21116-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21116-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="21116-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="21116-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21116-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21116-145">**\_VirtualSystemReferencePointService MSVM**</span><span class="sxs-lookup"><span data-stu-id="21116-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




