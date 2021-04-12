---
description: Esporta in un file una raccolta snapshot di sistemi di computer virtuali. La raccolta di snapshot, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Metodo ExportSnapshot della classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4dd29e001c8335477451e86151d950c25edb9b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226871"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="5635f-104">Metodo ExportSnapshot della classe MSVM \_ CollectionSnapshotService</span><span class="sxs-lookup"><span data-stu-id="5635f-104">ExportSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="5635f-105">Esporta in un file una raccolta snapshot di sistemi di computer virtuali.</span><span class="sxs-lookup"><span data-stu-id="5635f-105">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="5635f-106">La raccolta di snapshot, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.</span><span class="sxs-lookup"><span data-stu-id="5635f-106">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5635f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5635f-107">Syntax</span></span>


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5635f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5635f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5635f-109">*Snapshotcollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5635f-109">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5635f-110">Riferimento a una [**\_ raccolta CIM**](cim-collection.md) che rappresenta la raccolta di snapshot da esportare.</span><span class="sxs-lookup"><span data-stu-id="5635f-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="5635f-111">*ExportDirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5635f-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5635f-112">Percorso completo della directory in cui deve essere esportata la raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="5635f-112">The fully-qualified path of the directory to which the virtual system collection is to be exported.</span></span> <span data-ttu-id="5635f-113">Se la proprietà **CreateVmExportSubdirectory** nel parametro *ExportSettingData* è impostata su **true** , è possibile riutilizzare questa directory per esportare più raccolte di sistemi virtuali e questo metodo inserisce ogni definizione di raccolta di sistema virtuale in una sottodirectory separata in questo percorso.</span><span class="sxs-lookup"><span data-stu-id="5635f-113">If the **CreateVmExportSubdirectory** property in the *ExportSettingData* parameter is set to **True** then this directory can be reused for exporting multiple virtual system collections and this method places each virtual system collection definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="5635f-114">*ExportSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5635f-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5635f-115">Istanza di [**MSVM \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) che rappresenta le impostazioni per l'operazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="5635f-115">An instance of [**Msvm\_CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="5635f-116">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="5635f-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5635f-117">Riferimento facoltativo restituito se l'operazione viene eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="5635f-117">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="5635f-118">Se presente, il riferimento restituito a un'istanza di [**CIM \_ ConcreteJob**](cim-concretejob.md) può essere usato per monitorare lo stato di avanzamento e per ottenere il risultato del metodo.</span><span class="sxs-lookup"><span data-stu-id="5635f-118">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5635f-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5635f-119">Return value</span></span>

<span data-ttu-id="5635f-120">Se questo metodo viene eseguito in modo sincrono, restituisce 0 se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5635f-120">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="5635f-121">Se questo metodo viene eseguito in modo asincrono, restituisce 4096 e il parametro di output del processo può essere usato per tenere traccia dello stato di avanzamento dell'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="5635f-121">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="5635f-122">Qualsiasi altro valore restituito indica un errore.</span><span class="sxs-lookup"><span data-stu-id="5635f-122">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="5635f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5635f-123">Requirements</span></span>



| <span data-ttu-id="5635f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5635f-124">Requirement</span></span> | <span data-ttu-id="5635f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5635f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5635f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5635f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5635f-127">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5635f-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5635f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5635f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5635f-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5635f-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5635f-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5635f-130">Namespace</span></span><br/>                | <span data-ttu-id="5635f-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5635f-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5635f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5635f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5635f-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5635f-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5635f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5635f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5635f-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5635f-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5635f-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5635f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5635f-137">**\_CollectionSnapshotService MSVM**</span><span class="sxs-lookup"><span data-stu-id="5635f-137">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




