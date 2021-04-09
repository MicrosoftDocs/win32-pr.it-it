---
description: Aggiunge origini di avvio a una configurazione di sistema virtuale quando viene applicata a una \# configurazione del sistema virtuale &0034; state&\# 0034;.
ms.assetid: 2d091554-73d4-47c6-a0c2-97644fc9abe9
title: Metodo AddBootSourceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e20a1184e11113ba25ac060ec19dab5d2391b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128403"
---
# <a name="addbootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="5783e-103">Metodo AddBootSourceSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="5783e-103">AddBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="5783e-104">Aggiunge origini di avvio a una configurazione di sistema virtuale quando viene applicata a una configurazione di sistema virtuale "stato".</span><span class="sxs-lookup"><span data-stu-id="5783e-104">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="5783e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5783e-105">Syntax</span></span>


```mof
uint32 AddBootSourceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           BootSourceSettings[],
  [out] CIM_SettingData              REF ResultingBootSourceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5783e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5783e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5783e-107">*AffectedConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5783e-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5783e-108">[**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) che contiene la configurazione interessata.</span><span class="sxs-lookup"><span data-stu-id="5783e-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="5783e-109">*BootSourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5783e-109">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5783e-110">Matrice contenente le impostazioni dell'origine di avvio.</span><span class="sxs-lookup"><span data-stu-id="5783e-110">An array containing the boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="5783e-111">*ResultingBootSourceSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5783e-111">*ResultingBootSourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5783e-112">Se l'operazione riesce, restituisce un [**\_ SettingData CIM**](cim-settingdata.md) con le impostazioni dell'origine di avvio risultanti.</span><span class="sxs-lookup"><span data-stu-id="5783e-112">On success, returns a [**CIM\_SettingData**](cim-settingdata.md) with the resulting boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="5783e-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="5783e-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5783e-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5783e-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5783e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5783e-115">Return value</span></span>

<span data-ttu-id="5783e-116">In caso di esito positivo, restituisce 0 o 4096; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="5783e-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="5783e-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="5783e-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5783e-118">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="5783e-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5783e-119">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="5783e-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5783e-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="5783e-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5783e-121">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="5783e-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5783e-122">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="5783e-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5783e-123">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="5783e-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5783e-124">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="5783e-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="5783e-125">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5783e-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5783e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5783e-126">Requirements</span></span>



| <span data-ttu-id="5783e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5783e-127">Requirement</span></span> | <span data-ttu-id="5783e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5783e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5783e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5783e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5783e-130">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5783e-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5783e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5783e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5783e-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5783e-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5783e-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5783e-133">Namespace</span></span><br/>                | <span data-ttu-id="5783e-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5783e-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5783e-135">MOF</span><span class="sxs-lookup"><span data-stu-id="5783e-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5783e-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5783e-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5783e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5783e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5783e-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5783e-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5783e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5783e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5783e-140">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="5783e-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

