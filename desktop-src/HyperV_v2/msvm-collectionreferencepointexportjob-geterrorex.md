---
description: Recupera informazioni aggiuntive su un errore.
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Metodo GetErrorEx della classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c056f7c8a05d8d06d136219fb55699ed5e146bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319518"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="cb232-103">Metodo GetErrorEx della classe MSVM \_ CollectionReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="cb232-103">GetErrorEx method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="cb232-104">Recupera informazioni aggiuntive su un errore.</span><span class="sxs-lookup"><span data-stu-id="cb232-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="cb232-105">Quando il processo è in esecuzione o è terminato senza errori, **GetErrorEx** non restituisce alcuna istanza di [**\_ errore MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="cb232-105">When the job is executing or has terminated without error, **GetErrorEx** returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="cb232-106">Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, **GetErrorEx** restituisce una o più istanze di **\_ errore MSVM** .</span><span class="sxs-lookup"><span data-stu-id="cb232-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more **Msvm\_Error** instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb232-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb232-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="cb232-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb232-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb232-109">*Errori* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="cb232-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb232-110">Se lo stato operativo del processo non è "OK", questo parametro restituisce una matrice di istanze [**di \_ errore MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="cb232-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="cb232-111">In caso contrario, se il processo è "OK", questo parametro contiene **null**.</span><span class="sxs-lookup"><span data-stu-id="cb232-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb232-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb232-112">Return value</span></span>

<span data-ttu-id="cb232-113">In caso di esito positivo, restituisce 0; in caso contrario, restituisce uno dei valori di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb232-113">On success, returns 0; otherwise, returns one of the following error values:</span></span>

<dl> <dt>

<span data-ttu-id="cb232-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="cb232-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cb232-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="cb232-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cb232-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="cb232-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cb232-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="cb232-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cb232-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="cb232-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cb232-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="cb232-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cb232-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="cb232-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cb232-121">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="cb232-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cb232-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="cb232-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cb232-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="cb232-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cb232-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="cb232-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cb232-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="cb232-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cb232-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb232-126">Requirements</span></span>



| <span data-ttu-id="cb232-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb232-127">Requirement</span></span> | <span data-ttu-id="cb232-128">Valore</span><span class="sxs-lookup"><span data-stu-id="cb232-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb232-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb232-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cb232-130">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb232-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cb232-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb232-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cb232-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cb232-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cb232-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cb232-133">Namespace</span></span><br/>                | <span data-ttu-id="cb232-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="cb232-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cb232-135">MOF</span><span class="sxs-lookup"><span data-stu-id="cb232-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb232-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb232-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb232-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cb232-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb232-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cb232-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cb232-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb232-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb232-140">**\_CollectionReferencePointExportJob MSVM**</span><span class="sxs-lookup"><span data-stu-id="cb232-140">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




