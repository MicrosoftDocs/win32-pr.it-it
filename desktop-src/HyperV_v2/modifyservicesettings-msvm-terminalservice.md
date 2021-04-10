---
description: Modifica i dati dell'impostazione per il servizio.
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
ms.openlocfilehash: c2d6550d8b15264bf9cef126239228494996d080
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883705"
---
# <a name="modifyservicesettings-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="a6ae9-103">Metodo ModifyServiceSettings della classe MSVM \_ TerminalService</span><span class="sxs-lookup"><span data-stu-id="a6ae9-103">ModifyServiceSettings method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="a6ae9-104">Modifica i dati dell'impostazione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="a6ae9-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ae9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6ae9-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a6ae9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6ae9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ae9-107">*ServiceSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6ae9-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ae9-108">Rappresentazione di stringa della classe [**\_ TerminalServiceSettingData di MSVM**](msvm-terminalservicesettingdata.md) che contiene i dati di impostazione modificati per il servizio.</span><span class="sxs-lookup"><span data-stu-id="a6ae9-108">A string representation of the [**Msvm\_TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="a6ae9-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a6ae9-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ae9-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a6ae9-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6ae9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6ae9-111">Return value</span></span>

<span data-ttu-id="a6ae9-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a6ae9-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a6ae9-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a6ae9-114">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a6ae9-115">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a6ae9-116">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a6ae9-117">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a6ae9-118">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a6ae9-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a6ae9-120">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a6ae9-121">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a6ae9-122">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a6ae9-123">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a6ae9-124">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a6ae9-125">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a6ae9-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a6ae9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6ae9-126">Requirements</span></span>



| <span data-ttu-id="a6ae9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6ae9-127">Requirement</span></span> | <span data-ttu-id="a6ae9-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a6ae9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ae9-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6ae9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ae9-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a6ae9-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a6ae9-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6ae9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ae9-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a6ae9-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6ae9-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6ae9-133">Namespace</span></span><br/>                | <span data-ttu-id="a6ae9-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a6ae9-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a6ae9-135">MOF</span><span class="sxs-lookup"><span data-stu-id="a6ae9-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6ae9-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6ae9-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6ae9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a6ae9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6ae9-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a6ae9-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a6ae9-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6ae9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ae9-140">**\_TerminalService MSVM**</span><span class="sxs-lookup"><span data-stu-id="a6ae9-140">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

