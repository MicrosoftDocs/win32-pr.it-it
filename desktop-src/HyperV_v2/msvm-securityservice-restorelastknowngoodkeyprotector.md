---
description: Ripristina l'ultima protezione con chiave corretta nota.
ms.assetid: 0d1ea5d8-d25e-400c-be65-afe1bd65b1f0
title: Metodo RestoreLastKnownGoodKeyProtector della classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.RestoreLastKnownGoodKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e82fb3b40f4b85e74f92ed2690a411932af2eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320007"
---
# <a name="restorelastknowngoodkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="dd0ef-103">Metodo RestoreLastKnownGoodKeyProtector della classe MSVM \_ SecurityService</span><span class="sxs-lookup"><span data-stu-id="dd0ef-103">RestoreLastKnownGoodKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="dd0ef-104">Ripristina l'ultima protezione con chiave corretta nota.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-104">Restores back to the last known good key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd0ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd0ef-105">Syntax</span></span>


```mof
uint32 RestoreLastKnownGoodKeyProtector(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="dd0ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd0ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd0ef-107">*SecuritySettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd0ef-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd0ef-108">La stringa contiene un'istanza incorporata della classe [**\_ SecuritySettingData MSVM**](msvm-securitysettingdata.md) che rappresenta le impostazioni di sicurezza di un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ef-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="dd0ef-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd0ef-110">Parametro facoltativo per il monitoraggio dello stato di avanzamento dell'operazione, che viene utilizzato se non è stato possibile eseguire in modo sincrono il metodo.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="dd0ef-111">Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd0ef-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd0ef-112">Return value</span></span>

<span data-ttu-id="dd0ef-113">In caso di esito positivo, restituisce 0 o 4096; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-113">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="dd0ef-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd0ef-115">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dd0ef-116">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dd0ef-117">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dd0ef-118">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dd0ef-119">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dd0ef-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dd0ef-121">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dd0ef-122">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dd0ef-123">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dd0ef-124">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dd0ef-125">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dd0ef-126">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dd0ef-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd0ef-127">Requirements</span></span>



| <span data-ttu-id="dd0ef-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd0ef-128">Requirement</span></span> | <span data-ttu-id="dd0ef-129">Valore</span><span class="sxs-lookup"><span data-stu-id="dd0ef-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0ef-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd0ef-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dd0ef-131">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd0ef-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dd0ef-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd0ef-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dd0ef-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dd0ef-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="dd0ef-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dd0ef-134">Namespace</span></span><br/>                | <span data-ttu-id="dd0ef-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="dd0ef-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dd0ef-136">MOF</span><span class="sxs-lookup"><span data-stu-id="dd0ef-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd0ef-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd0ef-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd0ef-138">DLL</span><span class="sxs-lookup"><span data-stu-id="dd0ef-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd0ef-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd0ef-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd0ef-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd0ef-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd0ef-141">**\_SecurityService MSVM**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




