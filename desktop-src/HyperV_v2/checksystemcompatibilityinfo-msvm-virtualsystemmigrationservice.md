---
description: Verifica le informazioni di compatibilità per la compatibilità con il sistema di hosting del computer.
ms.assetid: 1991c58e-2d0b-4fc3-a04a-c18f358451f6
title: Metodo CheckSystemCompatibilityInfo della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e47b72c6cac6e8a6061b4560b77b82cb0b845a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878725"
---
# <a name="checksystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="e24b8-103">Metodo CheckSystemCompatibilityInfo della classe MSVM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="e24b8-103">CheckSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="e24b8-104">Verifica le informazioni di compatibilità per la compatibilità con il sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="e24b8-104">Checks the compatibility information for compatibility with the hosting computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e24b8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e24b8-105">Syntax</span></span>


```mof
uint32 CheckSystemCompatibilityInfo(
  [in]  uint8  CompatibilityInfo[],
  [out] string Reasons[]
);
```



## <a name="parameters"></a><span data-ttu-id="e24b8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e24b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e24b8-107">*CompatibilityInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e24b8-107">*CompatibilityInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-108">BLOB di dati ottenuti chiamando il metodo [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) sul computer host.</span><span class="sxs-lookup"><span data-stu-id="e24b8-108">A blob of data obtained by calling the [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="e24b8-109">*Motivi* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e24b8-109">*Reasons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e24b8-110">Matrice di stringhe che riceve le istanze incorporate della classe [**di \_ errore MSVM**](msvm-error.md) che rappresentano eventuali avvisi o errori.</span><span class="sxs-lookup"><span data-stu-id="e24b8-110">An array of strings that receives the embedded instances of the [**Msvm\_Error**](msvm-error.md) class that represent any warnings or errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e24b8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e24b8-111">Return value</span></span>

<span data-ttu-id="e24b8-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e24b8-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e24b8-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="e24b8-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="e24b8-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="e24b8-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="e24b8-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="e24b8-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="e24b8-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="e24b8-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e24b8-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-121">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e24b8-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="e24b8-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e24b8-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="e24b8-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e24b8-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="e24b8-126">**Non compatibile** (32784)</span><span class="sxs-lookup"><span data-stu-id="e24b8-126">**Not compatible** (32784)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e24b8-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e24b8-127">Requirements</span></span>



| <span data-ttu-id="e24b8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e24b8-128">Requirement</span></span> | <span data-ttu-id="e24b8-129">Valore</span><span class="sxs-lookup"><span data-stu-id="e24b8-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e24b8-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e24b8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e24b8-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e24b8-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e24b8-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e24b8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e24b8-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e24b8-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e24b8-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e24b8-134">Namespace</span></span><br/>                | <span data-ttu-id="e24b8-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e24b8-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e24b8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e24b8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e24b8-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e24b8-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e24b8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e24b8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e24b8-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e24b8-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e24b8-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e24b8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e24b8-141">**\_VirtualSystemMigrationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="e24b8-141">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




