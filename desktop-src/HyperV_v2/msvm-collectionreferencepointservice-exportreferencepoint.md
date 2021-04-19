---
description: Esporta una raccolta di punti di riferimento in un file. La raccolta di punti di riferimento, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Metodo ExportReferencePoint della classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49517da44cc7955d825792afcc475c56e37fad37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319509"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="0b68e-104">Metodo ExportReferencePoint della classe MSVM \_ CollectionReferencePointService</span><span class="sxs-lookup"><span data-stu-id="0b68e-104">ExportReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="0b68e-105">Esporta una raccolta di punti di riferimento in un file.</span><span class="sxs-lookup"><span data-stu-id="0b68e-105">Exports a reference point collection to a file.</span></span> <span data-ttu-id="0b68e-106">La raccolta di punti di riferimento, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.</span><span class="sxs-lookup"><span data-stu-id="0b68e-106">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b68e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b68e-107">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  CIM_Collection  REF ReferencePointCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0b68e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b68e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b68e-109">*ReferencePointCollection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b68e-109">*ReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b68e-110">Riferimento a una [**\_ raccolta CIM**](cim-collection.md) che rappresenta la raccolta di punti di riferimento da esportare.</span><span class="sxs-lookup"><span data-stu-id="0b68e-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the reference point collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="0b68e-111">*ExportDirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b68e-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b68e-112">Percorso completo della directory in cui deve essere esportata la raccolta di punti di riferimento.</span><span class="sxs-lookup"><span data-stu-id="0b68e-112">The fully-qualified path of the directory to which the reference point collection is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="0b68e-113">*ExportSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b68e-113">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b68e-114">Istanza di [**MSVM \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) che rappresenta le impostazioni per l'operazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="0b68e-114">An instance of [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="0b68e-115">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="0b68e-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b68e-116">Riferimento facoltativo restituito se l'operazione viene eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="0b68e-116">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="0b68e-117">Se presente, il riferimento restituito a un'istanza di [**CIM \_ ConcreteJob**](cim-concretejob.md) può essere usato per monitorare lo stato di avanzamento e per ottenere il risultato del metodo.</span><span class="sxs-lookup"><span data-stu-id="0b68e-117">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b68e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b68e-118">Return value</span></span>

<span data-ttu-id="0b68e-119">Se questo metodo viene eseguito in modo sincrono, restituisce 0 se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0b68e-119">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="0b68e-120">Se questo metodo viene eseguito in modo asincrono, restituisce 4096 e il parametro di output del processo può essere usato per tenere traccia dello stato di avanzamento dell'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="0b68e-120">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="0b68e-121">Qualsiasi altro valore restituito indica un errore.</span><span class="sxs-lookup"><span data-stu-id="0b68e-121">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b68e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b68e-122">Requirements</span></span>



| <span data-ttu-id="0b68e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b68e-123">Requirement</span></span> | <span data-ttu-id="0b68e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0b68e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b68e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b68e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0b68e-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0b68e-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0b68e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b68e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0b68e-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0b68e-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0b68e-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0b68e-129">Namespace</span></span><br/>                | <span data-ttu-id="0b68e-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0b68e-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0b68e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0b68e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b68e-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b68e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b68e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0b68e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b68e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b68e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0b68e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b68e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b68e-136">**\_CollectionReferencePointService MSVM**</span><span class="sxs-lookup"><span data-stu-id="0b68e-136">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




