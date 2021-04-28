---
description: 'Metodo SetSecurityPolicy della classe Msvm_SecurityService: imposta la protezione della chiave per un sistema virtuale.'
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
ms.openlocfilehash: 31b03ee8a941b0715b85f6a749c4ba59ade032f7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118729"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="76954-103">Metodo SetSecurityPolicy della classe Msvm \_ SecurityService</span><span class="sxs-lookup"><span data-stu-id="76954-103">SetSecurityPolicy method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="76954-104">Imposta la protezione della chiave per un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="76954-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="76954-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76954-105">Syntax</span></span>


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="76954-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="76954-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76954-107">*SecuritySettingData* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="76954-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76954-108">La stringa contiene un'istanza incorporata [**della classe Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) che rappresenta le impostazioni di sicurezza di un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="76954-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="76954-109">*SecurityPolicy* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="76954-109">*SecurityPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76954-110">Matrice di byte non elaborata che contiene i criteri di sicurezza da impostare.</span><span class="sxs-lookup"><span data-stu-id="76954-110">Raw byte array that contains the security policy to set.</span></span>

</dd> <dt>

<span data-ttu-id="76954-111">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="76954-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76954-112">Parametro facoltativo per il monitoraggio dello stato dell'operazione, che viene utilizzato se non è stato possibile eseguire il metodo in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="76954-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="76954-113">Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.</span><span class="sxs-lookup"><span data-stu-id="76954-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76954-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76954-114">Return value</span></span>

<span data-ttu-id="76954-115">On, success, restituisce un valore 0. In caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="76954-115">On, success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="76954-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="76954-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="76954-117">**Parametri del metodo controllati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="76954-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="76954-118">**Operazione non** riuscita (32768)</span><span class="sxs-lookup"><span data-stu-id="76954-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="76954-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="76954-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="76954-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="76954-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="76954-121">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="76954-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="76954-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="76954-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="76954-123">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="76954-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="76954-124">**Il sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="76954-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="76954-125">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="76954-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="76954-126">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="76954-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="76954-127">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="76954-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="76954-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="76954-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="76954-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76954-129">Requirements</span></span>



| <span data-ttu-id="76954-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="76954-130">Requirement</span></span> | <span data-ttu-id="76954-131">Valore</span><span class="sxs-lookup"><span data-stu-id="76954-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76954-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76954-132">Minimum supported client</span></span><br/> | <span data-ttu-id="76954-133">Windows 10, solo app desktop versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="76954-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="76954-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76954-134">Minimum supported server</span></span><br/> | <span data-ttu-id="76954-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="76954-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="76954-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="76954-136">Namespace</span></span><br/>                | <span data-ttu-id="76954-137">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="76954-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="76954-138">MOF</span><span class="sxs-lookup"><span data-stu-id="76954-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76954-139"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="76954-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76954-140">DLL</span><span class="sxs-lookup"><span data-stu-id="76954-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76954-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76954-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="76954-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76954-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76954-143">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="76954-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




