---
description: Genera un BLOB opaco di dati che contiene informazioni sulla compatibilità per il sistema specificato.
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: Metodo GetSystemCompatibilityInfo della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b0326dfb39123e508e9c5fefbd0404288cb97b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306046"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="35093-103">Metodo GetSystemCompatibilityInfo della classe MSVM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="35093-103">GetSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="35093-104">Genera un BLOB opaco di dati che contiene informazioni sulla compatibilità per il sistema specificato.</span><span class="sxs-lookup"><span data-stu-id="35093-104">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span> <span data-ttu-id="35093-105">Questo metodo viene utilizzato insieme al metodo [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) per determinare se è possibile eseguire una migrazione rapida o in tempo reale di una macchina virtuale a un altro computer host senza tentare effettivamente la migrazione.</span><span class="sxs-lookup"><span data-stu-id="35093-105">This method is used in conjunction with the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method to determine whether a quick or live migration of a virtual machine to another hosting computer system is possible without actually attempting the migration.</span></span>

## <a name="syntax"></a><span data-ttu-id="35093-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35093-106">Syntax</span></span>


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a><span data-ttu-id="35093-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="35093-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35093-108">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35093-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35093-109">Riferimento a una classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale per cui recuperare le informazioni sulla compatibilità.</span><span class="sxs-lookup"><span data-stu-id="35093-109">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to retrieve compatibility information for.</span></span> <span data-ttu-id="35093-110">Se questo parametro si riferisce al sistema di hosting, i dati restituiti nel parametro *CompatibilityInfo* possono essere utilizzati per determinare se è possibile eseguire rapidamente la migrazione di una delle macchine virtuali nel computer host a un altro computer host.</span><span class="sxs-lookup"><span data-stu-id="35093-110">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityInfo* parameter can be used to determine whether any of the virtual machines on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="35093-111">*CompatibilityInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="35093-111">*CompatibilityInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35093-112">BLOB opaco di dati che può essere passato al metodo [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) su un altro computer di hosting per confermare la compatibilità.</span><span class="sxs-lookup"><span data-stu-id="35093-112">An opaque blob of data that can be passed to the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on another hosting computer system to confirm compatibility.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35093-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35093-113">Return value</span></span>

<span data-ttu-id="35093-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="35093-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="35093-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="35093-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="35093-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="35093-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="35093-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="35093-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="35093-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="35093-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="35093-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="35093-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="35093-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="35093-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="35093-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="35093-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="35093-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="35093-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="35093-123">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="35093-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="35093-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="35093-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="35093-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="35093-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="35093-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="35093-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="35093-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="35093-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="35093-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35093-128">Requirements</span></span>



| <span data-ttu-id="35093-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="35093-129">Requirement</span></span> | <span data-ttu-id="35093-130">Valore</span><span class="sxs-lookup"><span data-stu-id="35093-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35093-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35093-131">Minimum supported client</span></span><br/> | <span data-ttu-id="35093-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="35093-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="35093-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35093-133">Minimum supported server</span></span><br/> | <span data-ttu-id="35093-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="35093-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35093-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35093-135">Namespace</span></span><br/>                | <span data-ttu-id="35093-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="35093-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="35093-137">MOF</span><span class="sxs-lookup"><span data-stu-id="35093-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35093-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35093-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35093-139">DLL</span><span class="sxs-lookup"><span data-stu-id="35093-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35093-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35093-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="35093-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35093-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35093-142">**\_VirtualSystemMigrationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="35093-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




