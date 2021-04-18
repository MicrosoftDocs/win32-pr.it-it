---
description: Crea un file di disco rigido virtuale.
ms.assetid: 6c136000-1df2-4456-833c-094671408338
title: Metodo CreateVirtualHardDisk della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b80a309274eb51ad7aff768898a9c3bd211f37cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315513"
---
# <a name="createvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="dc4bb-103">Metodo CreateVirtualHardDisk della classe MSVM \_ servizio</span><span class="sxs-lookup"><span data-stu-id="dc4bb-103">CreateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="dc4bb-104">Crea un file di disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="dc4bb-104">Creates a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc4bb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc4bb-105">Syntax</span></span>


```mof
uint32 CreateVirtualHardDisk(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="dc4bb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc4bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc4bb-107">*VirtualDiskSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc4bb-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc4bb-108">Stringa contenente un'istanza incorporata della classe [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) utilizzata per definire gli attributi del disco rigido virtuale da creare.</span><span class="sxs-lookup"><span data-stu-id="dc4bb-108">String that contains an embedded instance of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that is used to define attributes of the virtual hard disk to be created.</span></span>

</dd> <dt>

<span data-ttu-id="dc4bb-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="dc4bb-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc4bb-110">Riferimento al processo (può essere **null** se l'attività è stata completata).</span><span class="sxs-lookup"><span data-stu-id="dc4bb-110">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc4bb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc4bb-111">Return value</span></span>

<span data-ttu-id="dc4bb-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="dc4bb-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dc4bb-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-121">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="dc4bb-126">**File non trovato** (32779)</span><span class="sxs-lookup"><span data-stu-id="dc4bb-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="dc4bb-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc4bb-127">Remarks</span></span>

<span data-ttu-id="dc4bb-128">L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="dc4bb-128">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dc4bb-129">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dc4bb-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc4bb-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc4bb-130">Requirements</span></span>



| <span data-ttu-id="dc4bb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc4bb-131">Requirement</span></span> | <span data-ttu-id="dc4bb-132">Valore</span><span class="sxs-lookup"><span data-stu-id="dc4bb-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc4bb-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc4bb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dc4bb-134">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dc4bb-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dc4bb-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc4bb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dc4bb-136">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dc4bb-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dc4bb-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dc4bb-137">Namespace</span></span><br/>                | <span data-ttu-id="dc4bb-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="dc4bb-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dc4bb-139">MOF</span><span class="sxs-lookup"><span data-stu-id="dc4bb-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc4bb-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc4bb-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc4bb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="dc4bb-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc4bb-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc4bb-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dc4bb-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc4bb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc4bb-144">**\_Servizio MSVM**</span><span class="sxs-lookup"><span data-stu-id="dc4bb-144">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

