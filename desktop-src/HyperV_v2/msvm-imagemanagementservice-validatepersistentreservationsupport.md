---
description: Verifica se un file system può supportare un disco rigido virtuale con prenotazioni permanenti abilitate.
ms.assetid: c5fed9d5-0fa6-4b96-ae6e-84468b011e2a
title: Metodo ValidatePersistentReservationSupport della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidatePersistentReservationSupport
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 596e5cf840ee65dc0b3ad5315462db4666c8b262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966790"
---
# <a name="validatepersistentreservationsupport-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="3772d-103">Metodo ValidatePersistentReservationSupport della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="3772d-103">ValidatePersistentReservationSupport method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="3772d-104">Verifica se un file system può supportare un disco rigido virtuale con prenotazioni permanenti abilitate.</span><span class="sxs-lookup"><span data-stu-id="3772d-104">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="3772d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3772d-105">Syntax</span></span>


```mof
uint32 ValidatePersistentReservationSupport(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3772d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3772d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3772d-107">*Percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3772d-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3772d-108">Percorso completo che specifica il percorso di un file di immagine disco o di una directory in cui può essere inserito un file di immagine disco.</span><span class="sxs-lookup"><span data-stu-id="3772d-108">A fully-qualified path that specifies the location of a disk image file or a directory in which a disk image file might be placed.</span></span>

</dd> <dt>

<span data-ttu-id="3772d-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="3772d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3772d-110">Riferimento al processo (può essere null se l'attività è stata completata correttamente).</span><span class="sxs-lookup"><span data-stu-id="3772d-110">A reference to the job (can be null if the task is completed succesfully).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3772d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3772d-111">Return value</span></span>

<span data-ttu-id="3772d-112">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3772d-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="3772d-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="3772d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="3772d-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="3772d-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="3772d-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="3772d-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="3772d-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3772d-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="3772d-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-121">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3772d-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="3772d-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="3772d-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="3772d-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="3772d-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3772d-126">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="3772d-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3772d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3772d-127">Requirements</span></span>



| <span data-ttu-id="3772d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3772d-128">Requirement</span></span> | <span data-ttu-id="3772d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3772d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3772d-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3772d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3772d-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3772d-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3772d-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3772d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3772d-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3772d-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3772d-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3772d-134">Namespace</span></span><br/>                | <span data-ttu-id="3772d-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3772d-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3772d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3772d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3772d-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3772d-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3772d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3772d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3772d-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3772d-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3772d-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3772d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3772d-141">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="3772d-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




