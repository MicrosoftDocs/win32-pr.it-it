---
description: Aggiunge le impostazioni del servizio Guest a una configurazione di sistema virtuale.
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: Metodo AddGuestServiceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5bcdfd8c159e92efe633c04e22af5bceb9d003e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525207"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="7b526-103">Metodo AddGuestServiceSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="7b526-103">AddGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7b526-104">Aggiunge le impostazioni del servizio Guest a una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="7b526-104">Adds guest service settings to a virtual system configuration.</span></span>

<span data-ttu-id="7b526-105">Quando applicato alle parti di una configurazione di sistema virtuale "corrente", è possibile che vengano modificati i servizi guest di un effetto collaterale del sistema virtuale attivo.</span><span class="sxs-lookup"><span data-stu-id="7b526-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b526-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b526-106">Syntax</span></span>


```mof
uint32 AddGuestServiceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           GuestServiceSettings[],
  [out] CIM_SettingData              REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7b526-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b526-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b526-108">*AffectedConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b526-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b526-109">Riferimento a un [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) che descrive la configurazione interessata.</span><span class="sxs-lookup"><span data-stu-id="7b526-109">Reference to a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that describes the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7b526-110">*GuestServiceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b526-110">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b526-111">Matrice contenente le impostazioni del servizio Guest.</span><span class="sxs-lookup"><span data-stu-id="7b526-111">An array containing the guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="7b526-112">*ResultingGuestServiceSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7b526-112">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b526-113">Se l'operazione ha esito positivo, contiene un riferimento a un [**\_ SettingData CIM**](cim-settingdata.md) che descrive le impostazioni del servizio Guest risultante.</span><span class="sxs-lookup"><span data-stu-id="7b526-113">On success, contains a reference to a [**CIM\_SettingData**](cim-settingdata.md) that describes the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="7b526-114">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="7b526-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b526-115">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7b526-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b526-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b526-116">Return value</span></span>

<span data-ttu-id="7b526-117">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b526-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7b526-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="7b526-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7b526-119">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="7b526-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7b526-120">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="7b526-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7b526-121">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="7b526-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7b526-122">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="7b526-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7b526-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7b526-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7b526-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="7b526-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7b526-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7b526-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7b526-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7b526-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7b526-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b526-127">Requirements</span></span>



| <span data-ttu-id="7b526-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b526-128">Requirement</span></span> | <span data-ttu-id="7b526-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7b526-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b526-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b526-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7b526-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7b526-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7b526-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b526-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7b526-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7b526-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7b526-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7b526-134">Namespace</span></span><br/>                | <span data-ttu-id="7b526-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7b526-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7b526-136">MOF</span><span class="sxs-lookup"><span data-stu-id="7b526-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b526-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b526-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b526-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7b526-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b526-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b526-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7b526-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b526-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b526-141">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="7b526-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

