---
description: 'Metodo ModifyServiceSettings della classe Msvm_TerminalService: modifica i dati di impostazione per il servizio.'
ms.assetid: 76669180-fa95-4d6e-b89a-53e45da664c4
title: Metodo ModifyServiceSettings della classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 930b29c5c07c755b493a0aabad88ae776c0803e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119329"
---
# <a name="modifyservicesettings-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="80447-103">Metodo ModifyServiceSettings della classe Msvm \_ TerminalService</span><span class="sxs-lookup"><span data-stu-id="80447-103">ModifyServiceSettings method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="80447-104">Modifica i dati delle impostazioni per il servizio.</span><span class="sxs-lookup"><span data-stu-id="80447-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="80447-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80447-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="80447-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="80447-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80447-107">*ServiceSettingData* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="80447-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80447-108">Rappresentazione di stringa della [**classe Msvm \_ TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) che contiene i dati delle impostazioni modificate per il servizio.</span><span class="sxs-lookup"><span data-stu-id="80447-108">A string representation of the [**Msvm\_TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="80447-109">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="80447-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80447-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="80447-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80447-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80447-111">Return value</span></span>

<span data-ttu-id="80447-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="80447-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="80447-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="80447-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="80447-114">**Parametri del metodo controllati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="80447-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="80447-115">**Operazione non** riuscita (32768)</span><span class="sxs-lookup"><span data-stu-id="80447-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="80447-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="80447-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="80447-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="80447-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="80447-118">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="80447-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="80447-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="80447-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="80447-120">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="80447-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="80447-121">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="80447-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="80447-122">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="80447-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="80447-123">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="80447-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="80447-124">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="80447-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="80447-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="80447-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="80447-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80447-126">Requirements</span></span>



| <span data-ttu-id="80447-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="80447-127">Requirement</span></span> | <span data-ttu-id="80447-128">Valore</span><span class="sxs-lookup"><span data-stu-id="80447-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80447-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80447-129">Minimum supported client</span></span><br/> | <span data-ttu-id="80447-130">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="80447-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="80447-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80447-131">Minimum supported server</span></span><br/> | <span data-ttu-id="80447-132">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="80447-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80447-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="80447-133">Namespace</span></span><br/>                | <span data-ttu-id="80447-134">Virtualizzazione \\ radice \\ V2</span><span class="sxs-lookup"><span data-stu-id="80447-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="80447-135">MOF</span><span class="sxs-lookup"><span data-stu-id="80447-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80447-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="80447-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80447-137">DLL</span><span class="sxs-lookup"><span data-stu-id="80447-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80447-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80447-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="80447-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80447-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80447-140">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="80447-140">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

