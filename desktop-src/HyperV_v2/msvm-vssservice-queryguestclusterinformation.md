---
description: Esecuzione di query sulle informazioni del cluster dall'host Hyper-V al Guest.
ms.assetid: 28983984-a2af-4eab-8b1f-2f7d6a3d70ea
title: Metodo QueryGuestClusterInformation della classe Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService.QueryGuestClusterInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 36f88441729cc1e6e36bcad9ca84b46049bce2a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525177"
---
# <a name="queryguestclusterinformation-method-of-the-msvm_vssservice-class"></a><span data-ttu-id="eb354-103">Metodo QueryGuestClusterInformation della classe MSVM \_ VssService</span><span class="sxs-lookup"><span data-stu-id="eb354-103">QueryGuestClusterInformation method of the Msvm\_VssService class</span></span>

<span data-ttu-id="eb354-104">Esecuzione di query sulle informazioni del cluster dall'host Hyper-V al Guest.</span><span class="sxs-lookup"><span data-stu-id="eb354-104">Querying cluster information from the Hyper-V host to the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb354-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb354-105">Syntax</span></span>


```mof
uint32 QueryGuestClusterInformation(
  [out] Msvm_GuestClusterInformation GuestClusterInformation
);
```



## <a name="parameters"></a><span data-ttu-id="eb354-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb354-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb354-107">*GuestClusterInformation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="eb354-107">*GuestClusterInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb354-108">Se l'operazione ha esito positivo, contiene un [**\_ GuestClusterInformation MSVM**](msvm-guestclusterinformation.md) che descrive il cluster guest.</span><span class="sxs-lookup"><span data-stu-id="eb354-108">On success, contains an [**Msvm\_GuestClusterInformation**](msvm-guestclusterinformation.md) that describes the guest cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb354-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb354-109">Return value</span></span>

<span data-ttu-id="eb354-110">In caso di esito positivo, restituisce 0 (completa senza errori) o 4096 (processo avviato); in caso contrario, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="eb354-110">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="eb354-111">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="eb354-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eb354-112">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="eb354-112">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="eb354-113">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="eb354-113">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="eb354-114">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="eb354-114">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="eb354-115">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="eb354-115">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="eb354-116">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="eb354-116">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="eb354-117">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="eb354-117">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="eb354-118">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="eb354-118">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="eb354-119">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="eb354-119">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="eb354-120">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="eb354-120">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="eb354-121">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="eb354-121">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="eb354-122">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="eb354-122">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="eb354-123">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="eb354-123">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="eb354-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb354-124">Requirements</span></span>



| <span data-ttu-id="eb354-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb354-125">Requirement</span></span> | <span data-ttu-id="eb354-126">Valore</span><span class="sxs-lookup"><span data-stu-id="eb354-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb354-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb354-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eb354-128">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="eb354-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="eb354-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb354-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eb354-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="eb354-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="eb354-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eb354-131">Namespace</span></span><br/>                | <span data-ttu-id="eb354-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="eb354-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eb354-133">MOF</span><span class="sxs-lookup"><span data-stu-id="eb354-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb354-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb354-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb354-135">DLL</span><span class="sxs-lookup"><span data-stu-id="eb354-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb354-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb354-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eb354-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb354-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb354-138">**\_VssService MSVM**</span><span class="sxs-lookup"><span data-stu-id="eb354-138">**Msvm\_VssService**</span></span>](msvm-vssservice.md)
</dt> </dl>

 

 




