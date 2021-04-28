---
description: 'Metodo GetErrorEx della classe Msvm_VirtualSystemReferencePointExportJob : recupera informazioni aggiuntive su un errore.'
ms.assetid: 63ce4762-e5ce-405f-b5fc-74e505b0eaf1
title: Metodo GetErrorEx della classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80e0850018b20497dbc42bbdbb802ffe4317489b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118609"
---
# <a name="geterrorex-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="2fb25-103">Metodo GetErrorEx della classe Msvm \_ VirtualSystemReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="2fb25-103">GetErrorEx method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="2fb25-104">Recupera informazioni aggiuntive su un errore.</span><span class="sxs-lookup"><span data-stu-id="2fb25-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="2fb25-105">Quando il processo è in esecuzione o è terminato senza errori, **GetErrorEx** non restituisce alcuna **istanza di GetErrorEx.**</span><span class="sxs-lookup"><span data-stu-id="2fb25-105">When the job is executing or has terminated without error, **GetErrorEx** returns no **GetErrorEx** instance.</span></span> <span data-ttu-id="2fb25-106">Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, **GetErrorEx** restituisce una o più [**istanze di Msvm \_ Error.**](msvm-error.md)</span><span class="sxs-lookup"><span data-stu-id="2fb25-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb25-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fb25-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="2fb25-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fb25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fb25-109">*Errori* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="2fb25-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fb25-110">Se lo stato operativo del processo non è "OK", questo parametro restituisce una matrice di [**istanze di Msvm \_ Error.**](msvm-error.md)</span><span class="sxs-lookup"><span data-stu-id="2fb25-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="2fb25-111">In caso contrario, se il processo è "OK", questo parametro contiene **NULL.**</span><span class="sxs-lookup"><span data-stu-id="2fb25-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fb25-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fb25-112">Return value</span></span>

<span data-ttu-id="2fb25-113">In caso di esito positivo, restituisce 0. In caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="2fb25-113">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2fb25-114">**Completata senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="2fb25-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2fb25-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="2fb25-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2fb25-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="2fb25-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2fb25-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="2fb25-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2fb25-118">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="2fb25-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2fb25-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="2fb25-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2fb25-120">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="2fb25-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2fb25-121">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="2fb25-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2fb25-122">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="2fb25-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2fb25-123">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="2fb25-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2fb25-124">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="2fb25-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2fb25-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="2fb25-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2fb25-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fb25-126">Requirements</span></span>



| <span data-ttu-id="2fb25-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fb25-127">Requirement</span></span> | <span data-ttu-id="2fb25-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2fb25-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb25-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fb25-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2fb25-130">Windows 10, solo app desktop versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="2fb25-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2fb25-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fb25-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2fb25-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2fb25-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2fb25-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2fb25-133">Namespace</span></span><br/>                | <span data-ttu-id="2fb25-134">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2fb25-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2fb25-135">MOF</span><span class="sxs-lookup"><span data-stu-id="2fb25-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fb25-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fb25-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fb25-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2fb25-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fb25-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2fb25-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2fb25-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fb25-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fb25-140">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="2fb25-140">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




