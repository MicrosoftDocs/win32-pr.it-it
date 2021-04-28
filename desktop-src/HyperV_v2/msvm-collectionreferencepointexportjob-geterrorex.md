---
description: 'Metodo GetErrorEx della classe Msvm_CollectionReferencePointExportJob: recupera informazioni aggiuntive su un errore.'
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
ms.openlocfilehash: 3b84c41776c081c302078773d9402145b0fe41e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112089"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="2f71d-103">Metodo GetErrorEx della classe Msvm \_ CollectionReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="2f71d-103">GetErrorEx method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="2f71d-104">Recupera informazioni aggiuntive su un errore.</span><span class="sxs-lookup"><span data-stu-id="2f71d-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="2f71d-105">Quando il processo è in esecuzione o è terminato senza errori, **GetErrorEx** non restituisce alcuna [**istanza di Msvm \_ Error.**](msvm-error.md)</span><span class="sxs-lookup"><span data-stu-id="2f71d-105">When the job is executing or has terminated without error, **GetErrorEx** returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="2f71d-106">Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, **GetErrorEx** restituisce una o più **istanze di Msvm \_ Error.**</span><span class="sxs-lookup"><span data-stu-id="2f71d-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more **Msvm\_Error** instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f71d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f71d-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="2f71d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f71d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f71d-109">*Errori* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="2f71d-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f71d-110">Se lo stato operativo del processo non è "OK", questo parametro restituisce una matrice di [**istanze di Msvm \_ Error.**](msvm-error.md)</span><span class="sxs-lookup"><span data-stu-id="2f71d-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="2f71d-111">In caso contrario, se il processo è "OK", questo parametro contiene **NULL.**</span><span class="sxs-lookup"><span data-stu-id="2f71d-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f71d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f71d-112">Return value</span></span>

<span data-ttu-id="2f71d-113">In caso di esito positivo, restituisce 0. In caso contrario, restituisce uno dei valori di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f71d-113">On success, returns 0; otherwise, returns one of the following error values:</span></span>

<dl> <dt>

<span data-ttu-id="2f71d-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="2f71d-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2f71d-115">**Operazione non** riuscita (32768)</span><span class="sxs-lookup"><span data-stu-id="2f71d-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2f71d-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="2f71d-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2f71d-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="2f71d-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2f71d-118">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="2f71d-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2f71d-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="2f71d-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2f71d-120">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="2f71d-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2f71d-121">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="2f71d-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2f71d-122">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="2f71d-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2f71d-123">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="2f71d-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2f71d-124">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="2f71d-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2f71d-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="2f71d-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2f71d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f71d-126">Requirements</span></span>



| <span data-ttu-id="2f71d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f71d-127">Requirement</span></span> | <span data-ttu-id="2f71d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2f71d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f71d-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f71d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2f71d-130">Windows 10, solo app desktop versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f71d-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2f71d-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f71d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2f71d-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2f71d-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2f71d-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2f71d-133">Namespace</span></span><br/>                | <span data-ttu-id="2f71d-134">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2f71d-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2f71d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="2f71d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f71d-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f71d-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f71d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2f71d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f71d-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f71d-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2f71d-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f71d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f71d-140">**Msvm \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="2f71d-140">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




