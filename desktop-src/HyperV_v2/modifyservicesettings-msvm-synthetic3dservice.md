---
description: Modifica i dati dell'impostazione per il servizio sintetico 3D.
ms.assetid: 951ba829-2821-4621-800f-4e1a967b41f5
title: Metodo ModifyServiceSettings della classe Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 76f6fe18dea67231c9d722352df516bf97c35ac0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485556"
---
# <a name="modifyservicesettings-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="ea185-103">Metodo ModifyServiceSettings della classe MSVM \_ Synthetic3DService</span><span class="sxs-lookup"><span data-stu-id="ea185-103">ModifyServiceSettings method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="ea185-104">Modifica i dati dell'impostazione per il servizio sintetico 3D.</span><span class="sxs-lookup"><span data-stu-id="ea185-104">Modifies the setting data for the synthetic 3-D service.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea185-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea185-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ea185-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea185-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea185-107">*SettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea185-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea185-108">Rappresentazione di stringa della classe [**\_ Synthetic3DServiceSettingData di MSVM**](msvm-synthetic3dservicesettingdata.md) che contiene i dati di impostazione modificati per il servizio.</span><span class="sxs-lookup"><span data-stu-id="ea185-108">A string representation of the [**Msvm\_Synthetic3DServiceSettingData**](msvm-synthetic3dservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="ea185-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ea185-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea185-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea185-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea185-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea185-111">Return value</span></span>

<span data-ttu-id="ea185-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea185-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ea185-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ea185-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ea185-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="ea185-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ea185-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="ea185-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ea185-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="ea185-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ea185-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="ea185-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ea185-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="ea185-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ea185-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="ea185-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ea185-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ea185-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ea185-121">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ea185-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ea185-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="ea185-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ea185-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ea185-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ea185-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="ea185-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ea185-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ea185-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ea185-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea185-126">Requirements</span></span>



| <span data-ttu-id="ea185-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea185-127">Requirement</span></span> | <span data-ttu-id="ea185-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ea185-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea185-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea185-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ea185-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ea185-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ea185-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea185-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ea185-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ea185-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ea185-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ea185-133">Namespace</span></span><br/>                | <span data-ttu-id="ea185-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ea185-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ea185-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ea185-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea185-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea185-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea185-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ea185-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea185-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ea185-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ea185-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea185-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea185-140">**\_Synthetic3DService MSVM**</span><span class="sxs-lookup"><span data-stu-id="ea185-140">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

