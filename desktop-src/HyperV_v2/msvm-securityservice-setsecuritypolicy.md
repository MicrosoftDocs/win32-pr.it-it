---
description: Imposta la protezione con chiave per un sistema virtuale.
ms.assetid: 22496fde-6298-4e9d-bd0c-135dcb4ea5a5
title: Metodo SetSecurityPolicy della classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetSecurityPolicy
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 35954f27d1184b714091058a35f32a6347d4ef55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530379"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="c379c-103">Metodo SetSecurityPolicy della classe MSVM \_ SecurityService</span><span class="sxs-lookup"><span data-stu-id="c379c-103">SetSecurityPolicy method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="c379c-104">Imposta la protezione con chiave per un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="c379c-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c379c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c379c-105">Syntax</span></span>


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c379c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c379c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c379c-107">*SecuritySettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c379c-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c379c-108">La stringa contiene un'istanza incorporata della classe [**\_ SecuritySettingData MSVM**](msvm-securitysettingdata.md) che rappresenta le impostazioni di sicurezza di un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="c379c-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="c379c-109">*SecurityPolicy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c379c-109">*SecurityPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c379c-110">Matrice di byte non elaborati che contiene i criteri di sicurezza da impostare.</span><span class="sxs-lookup"><span data-stu-id="c379c-110">Raw byte array that contains the security policy to set.</span></span>

</dd> <dt>

<span data-ttu-id="c379c-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c379c-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c379c-112">Parametro facoltativo per il monitoraggio dello stato di avanzamento dell'operazione, che viene utilizzato se non è stato possibile eseguire in modo sincrono il metodo.</span><span class="sxs-lookup"><span data-stu-id="c379c-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="c379c-113">Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.</span><span class="sxs-lookup"><span data-stu-id="c379c-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c379c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c379c-114">Return value</span></span>

<span data-ttu-id="c379c-115">In caso di esito positivo, restituisce 0. in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="c379c-115">On, success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="c379c-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="c379c-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c379c-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="c379c-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c379c-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="c379c-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c379c-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="c379c-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c379c-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="c379c-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c379c-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="c379c-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c379c-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="c379c-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c379c-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c379c-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c379c-124">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c379c-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c379c-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="c379c-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c379c-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c379c-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c379c-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="c379c-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c379c-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c379c-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c379c-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c379c-129">Requirements</span></span>



| <span data-ttu-id="c379c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c379c-130">Requirement</span></span> | <span data-ttu-id="c379c-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c379c-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c379c-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c379c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c379c-133">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="c379c-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c379c-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c379c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c379c-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c379c-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c379c-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c379c-136">Namespace</span></span><br/>                | <span data-ttu-id="c379c-137">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c379c-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c379c-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c379c-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c379c-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c379c-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c379c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c379c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c379c-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c379c-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c379c-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c379c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c379c-143">**\_SecurityService MSVM**</span><span class="sxs-lookup"><span data-stu-id="c379c-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




