---
description: Recupera un errore.
ms.assetid: 7c47acae-d398-4698-81db-e3c8a812f339
title: Metodo GetError della classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ea92bd08a2b65466d11e41bb459200610a89677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058150"
---
# <a name="geterror-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="cfd71-103">Metodo GetError della \_ classe CollectionReferencePointExportJob di MSVM</span><span class="sxs-lookup"><span data-stu-id="cfd71-103">GetError method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="cfd71-104">Recupera un errore.</span><span class="sxs-lookup"><span data-stu-id="cfd71-104">Retrieves an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfd71-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cfd71-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="cfd71-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfd71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfd71-107">*Errore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cfd71-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfd71-108">In seguito all'esito positivo, contiene una descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="cfd71-108">On success, contains a description of the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfd71-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfd71-109">Return value</span></span>

<span data-ttu-id="cfd71-110">0 in caso di esito positivo; in caso contrario, un errore.</span><span class="sxs-lookup"><span data-stu-id="cfd71-110">0 on success; otherwise, an error.</span></span>

<dl> <dt>

<span data-ttu-id="cfd71-111">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="cfd71-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cfd71-112">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="cfd71-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cfd71-113">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="cfd71-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cfd71-114">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="cfd71-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cfd71-115">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="cfd71-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cfd71-116">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="cfd71-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cfd71-117">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="cfd71-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cfd71-118">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="cfd71-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cfd71-119">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="cfd71-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cfd71-120">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="cfd71-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cfd71-121">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="cfd71-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cfd71-122">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="cfd71-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cfd71-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfd71-123">Requirements</span></span>



| <span data-ttu-id="cfd71-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfd71-124">Requirement</span></span> | <span data-ttu-id="cfd71-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cfd71-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfd71-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfd71-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cfd71-127">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="cfd71-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cfd71-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfd71-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cfd71-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cfd71-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cfd71-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cfd71-130">Namespace</span></span><br/>                | <span data-ttu-id="cfd71-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="cfd71-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cfd71-132">MOF</span><span class="sxs-lookup"><span data-stu-id="cfd71-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfd71-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfd71-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfd71-134">DLL</span><span class="sxs-lookup"><span data-stu-id="cfd71-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfd71-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cfd71-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cfd71-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfd71-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfd71-137">**\_CollectionReferencePointExportJob MSVM**</span><span class="sxs-lookup"><span data-stu-id="cfd71-137">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




