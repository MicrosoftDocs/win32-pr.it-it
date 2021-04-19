---
description: Modifica le impostazioni di sicurezza correnti di una macchina virtuale.
ms.assetid: b3eedab6-fd69-4c54-a8bf-4e3b77207687
title: Metodo ModifySecuritySettings della classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.ModifySecuritySettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4422f04be1833d66280392704630fcb670eba810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320006"
---
# <a name="modifysecuritysettings-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="c145c-103">Metodo ModifySecuritySettings della classe MSVM \_ SecurityService</span><span class="sxs-lookup"><span data-stu-id="c145c-103">ModifySecuritySettings method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="c145c-104">Modifica le impostazioni di sicurezza correnti di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c145c-104">Modifies the current security settings of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c145c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c145c-105">Syntax</span></span>


```mof
uint32 ModifySecuritySettings(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c145c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c145c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c145c-107">*SecuritySettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c145c-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c145c-108">Nuovi dati dell'impostazione di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c145c-108">The new security setting data.</span></span>

</dd> <dt>

<span data-ttu-id="c145c-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c145c-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c145c-110">Parametro facoltativo per il monitoraggio dello stato di avanzamento dell'operazione, che viene utilizzato se non è stato possibile eseguire in modo sincrono il metodo.</span><span class="sxs-lookup"><span data-stu-id="c145c-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="c145c-111">Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.</span><span class="sxs-lookup"><span data-stu-id="c145c-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c145c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c145c-112">Return value</span></span>

<span data-ttu-id="c145c-113">In caso di esito positivo, restituisce 0. in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="c145c-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="c145c-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="c145c-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c145c-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="c145c-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c145c-116">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="c145c-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c145c-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="c145c-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c145c-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="c145c-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c145c-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="c145c-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c145c-120">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="c145c-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c145c-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="c145c-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c145c-122">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="c145c-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c145c-123">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="c145c-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c145c-124">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c145c-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c145c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c145c-125">Requirements</span></span>



| <span data-ttu-id="c145c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c145c-126">Requirement</span></span> | <span data-ttu-id="c145c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c145c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c145c-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c145c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c145c-129">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="c145c-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c145c-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c145c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c145c-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c145c-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c145c-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c145c-132">Namespace</span></span><br/>                | <span data-ttu-id="c145c-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c145c-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c145c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c145c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c145c-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c145c-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c145c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c145c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c145c-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c145c-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c145c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c145c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c145c-139">**\_SecurityService MSVM**</span><span class="sxs-lookup"><span data-stu-id="c145c-139">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




