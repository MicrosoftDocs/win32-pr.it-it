---
description: Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce alcuna \_ istanza di errore MSVM.
ms.assetid: 119E7EFD-78C9-46F1-8A53-C51A7A34B32E
title: Metodo GetErrorEx della classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26d5aff37631de00cffccd49cf54f0ba09ce5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307740"
---
# <a name="geterrorex-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="3ae44-103">Metodo GetErrorEx della classe MSVM \_ StorageJob</span><span class="sxs-lookup"><span data-stu-id="3ae44-103">GetErrorEx method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="3ae44-104">Quando il processo è in esecuzione o è terminato senza errori, questo metodo non restituisce alcuna istanza di [**\_ errore MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="3ae44-104">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="3ae44-105">Tuttavia, se il processo non è riuscito a causa di un problema interno o perché il processo è stato terminato da un client, vengono restituite una o più istanze di **\_ errore MSVM** .</span><span class="sxs-lookup"><span data-stu-id="3ae44-105">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae44-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ae44-106">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="3ae44-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ae44-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ae44-108">*Errori* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="3ae44-108">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae44-109">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="3ae44-109">Type: **string\[\]**</span></span>

<span data-ttu-id="3ae44-110">Se lo stato operativo del processo non è "OK", questo metodo restituisce una matrice di istanze [**di \_ errore MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="3ae44-110">If the operational status of the job is not "OK", this method returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="3ae44-111">In caso contrario, se il processo è "OK", viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="3ae44-111">Otherwise, if the job is "OK", **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ae44-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ae44-112">Return value</span></span>

<span data-ttu-id="3ae44-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ae44-113">Type: **uint32**</span></span>

<span data-ttu-id="3ae44-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3ae44-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3ae44-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="3ae44-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ae44-116">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="3ae44-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3ae44-117">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="3ae44-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3ae44-118">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="3ae44-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3ae44-119">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="3ae44-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3ae44-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="3ae44-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3ae44-121">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="3ae44-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3ae44-122">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3ae44-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3ae44-123">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="3ae44-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3ae44-124">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="3ae44-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3ae44-125">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="3ae44-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3ae44-126">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="3ae44-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3ae44-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ae44-127">Remarks</span></span>

<span data-ttu-id="3ae44-128">L'accesso alla [**classe \_ StorageJob di MSVM**](msvm-storagejob.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="3ae44-128">Access to the [**Msvm\_StorageJob**](msvm-storagejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3ae44-129">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3ae44-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ae44-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ae44-130">Requirements</span></span>



| <span data-ttu-id="3ae44-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ae44-131">Requirement</span></span> | <span data-ttu-id="3ae44-132">Valore</span><span class="sxs-lookup"><span data-stu-id="3ae44-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae44-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ae44-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae44-134">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3ae44-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3ae44-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ae44-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae44-136">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3ae44-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ae44-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3ae44-137">Namespace</span></span><br/>                | <span data-ttu-id="3ae44-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3ae44-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3ae44-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3ae44-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ae44-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ae44-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ae44-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3ae44-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ae44-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ae44-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ae44-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ae44-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ae44-144">**\_StorageJob MSVM**</span><span class="sxs-lookup"><span data-stu-id="3ae44-144">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

