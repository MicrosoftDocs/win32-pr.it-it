---
description: Recupera le dimensioni totali dei file di sistema della macchina virtuale.
ms.assetid: 492aa0df-1562-4d83-a0ea-43776b12c1b1
title: Metodo GetSizeOfSystemFiles della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSizeOfSystemFiles
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ed9fcf93093e17c2989121bf33ee5f5fbf09bab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752218"
---
# <a name="getsizeofsystemfiles-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="df7a3-103">Metodo GetSizeOfSystemFiles della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="df7a3-103">GetSizeOfSystemFiles method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="df7a3-104">Recupera le dimensioni totali dei file di sistema della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="df7a3-104">Retrieves the total size of the system files of virtual machine.</span></span> <span data-ttu-id="df7a3-105">Sono inclusi i file di configurazione e di stato salvato.</span><span class="sxs-lookup"><span data-stu-id="df7a3-105">These include the configuration and saved state files.</span></span>

## <a name="syntax"></a><span data-ttu-id="df7a3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df7a3-106">Syntax</span></span>


```mof
uint32 GetSizeOfSystemFiles(
  [in]  CIM_VirtualSystemSettingData REF Vssd,
  [out] uint64                           Size
);
```



## <a name="parameters"></a><span data-ttu-id="df7a3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="df7a3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df7a3-108">*VSSD* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df7a3-108">*Vssd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df7a3-109">Riferimento all'istanza [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) di cui devono essere recuperate le dimensioni dei file di sistema.</span><span class="sxs-lookup"><span data-stu-id="df7a3-109">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance whose system files size are to be retrieved.</span></span> <span data-ttu-id="df7a3-110">Questa istanza può rappresentare l'istanza corrente della macchina virtuale o un'istanza di uno snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="df7a3-110">This instance may represent either the current instantiation of the virtual machine, or an instance of a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="df7a3-111">*Dimensioni* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="df7a3-111">*Size* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df7a3-112">Dimensioni totali, in byte, dei file di sistema.</span><span class="sxs-lookup"><span data-stu-id="df7a3-112">The total size, in bytes, of system files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df7a3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df7a3-113">Return value</span></span>

<span data-ttu-id="df7a3-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="df7a3-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="df7a3-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="df7a3-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="df7a3-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="df7a3-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="df7a3-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="df7a3-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="df7a3-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="df7a3-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="df7a3-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="df7a3-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="df7a3-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="df7a3-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="df7a3-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="df7a3-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="df7a3-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="df7a3-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="df7a3-123">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="df7a3-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="df7a3-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="df7a3-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="df7a3-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="df7a3-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="df7a3-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="df7a3-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="df7a3-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="df7a3-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="df7a3-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df7a3-128">Requirements</span></span>



| <span data-ttu-id="df7a3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="df7a3-129">Requirement</span></span> | <span data-ttu-id="df7a3-130">Valore</span><span class="sxs-lookup"><span data-stu-id="df7a3-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df7a3-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df7a3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="df7a3-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="df7a3-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="df7a3-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df7a3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="df7a3-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="df7a3-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df7a3-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="df7a3-135">Namespace</span></span><br/>                | <span data-ttu-id="df7a3-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="df7a3-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="df7a3-137">MOF</span><span class="sxs-lookup"><span data-stu-id="df7a3-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df7a3-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df7a3-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="df7a3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="df7a3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df7a3-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="df7a3-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="df7a3-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df7a3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df7a3-142">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="df7a3-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

