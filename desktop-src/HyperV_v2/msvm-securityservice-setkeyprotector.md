---
description: 'Metodo SetKeyProtector della classe Msvm_SecurityService: imposta la protezione della chiave per un sistema virtuale.'
ms.assetid: 84c114cb-a3a0-44f2-b862-38b05b96bd46
title: Metodo SetKeyProtector della classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3b5eca7ddcc506d158175782e3e13796e56de267
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111409"
---
# <a name="setkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="07728-103">Metodo SetKeyProtector della classe Msvm \_ SecurityService</span><span class="sxs-lookup"><span data-stu-id="07728-103">SetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="07728-104">Imposta la protezione della chiave per un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="07728-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="07728-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07728-105">Syntax</span></span>


```mof
uint32 SetKeyProtector(
  [in]  string              SecuritySettingData,
  [in]  uint8               KeyProtector[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="07728-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="07728-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07728-107">*SecuritySettingData* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="07728-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07728-108">La stringa contiene un'istanza incorporata [**della classe Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) che rappresenta le impostazioni di sicurezza di un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="07728-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="07728-109">*KeyProtector* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="07728-109">*KeyProtector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07728-110">Matrice di byte non elaborata che contiene la protezione della chiave da impostare.</span><span class="sxs-lookup"><span data-stu-id="07728-110">Raw byte array that contains the key protector to set.</span></span>

</dd> <dt>

<span data-ttu-id="07728-111">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="07728-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07728-112">Parametro facoltativo per il monitoraggio dello stato dell'operazione, che viene utilizzato se non è stato possibile eseguire il metodo in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="07728-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="07728-113">Se l'operazione viene eseguita in modo asincrono, il valore restituito è 4096.</span><span class="sxs-lookup"><span data-stu-id="07728-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07728-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07728-114">Return value</span></span>

<span data-ttu-id="07728-115">In caso di esito positivo, restituisce un valore 0 o 4096. In caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="07728-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="07728-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="07728-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="07728-117">**Parametri del metodo controllati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="07728-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="07728-118">**Operazione non** riuscita (32768)</span><span class="sxs-lookup"><span data-stu-id="07728-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="07728-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="07728-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="07728-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="07728-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="07728-121">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="07728-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="07728-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="07728-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="07728-123">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="07728-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="07728-124">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="07728-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="07728-125">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="07728-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="07728-126">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="07728-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="07728-127">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="07728-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="07728-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="07728-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="07728-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07728-129">Requirements</span></span>



| <span data-ttu-id="07728-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="07728-130">Requirement</span></span> | <span data-ttu-id="07728-131">Valore</span><span class="sxs-lookup"><span data-stu-id="07728-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07728-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07728-132">Minimum supported client</span></span><br/> | <span data-ttu-id="07728-133">Windows 10, solo app desktop versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="07728-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="07728-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07728-134">Minimum supported server</span></span><br/> | <span data-ttu-id="07728-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="07728-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="07728-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07728-136">Namespace</span></span><br/>                | <span data-ttu-id="07728-137">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="07728-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="07728-138">MOF</span><span class="sxs-lookup"><span data-stu-id="07728-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07728-139"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="07728-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="07728-140">DLL</span><span class="sxs-lookup"><span data-stu-id="07728-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07728-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="07728-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="07728-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07728-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07728-143">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="07728-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




