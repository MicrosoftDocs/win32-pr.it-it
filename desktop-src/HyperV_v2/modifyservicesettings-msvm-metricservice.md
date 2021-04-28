---
description: "Metodo ModifyServiceSettings della classe Msvm_MetricService: modifica i dati dell'impostazione per il servizio."
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Metodo ModifyServiceSettings della classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 088aec001dd63de7344256fd9e114b6ff73e4425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112179"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="80e8f-103">Metodo ModifyServiceSettings della classe Msvm \_ MetricService</span><span class="sxs-lookup"><span data-stu-id="80e8f-103">ModifyServiceSettings method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="80e8f-104">Modifica i dati dell'impostazione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="80e8f-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e8f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80e8f-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="80e8f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="80e8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80e8f-107">*Impostazione dei dati* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="80e8f-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80e8f-108">Contiene un'istanza incorporata [**della classe Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md) che contiene i dati delle impostazioni modificate per il servizio.</span><span class="sxs-lookup"><span data-stu-id="80e8f-108">Contains an embedded instance of the [**Msvm\_MetricServiceSettingData**](msvm-metricservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="80e8f-109">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="80e8f-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80e8f-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="80e8f-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80e8f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80e8f-111">Return value</span></span>

<span data-ttu-id="80e8f-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="80e8f-112">This method returns one of the following values.</span></span>



| <span data-ttu-id="80e8f-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="80e8f-113">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="80e8f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80e8f-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="80e8f-115"><dt>**Completata senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-115"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="80e8f-116">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="80e8f-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="80e8f-117"><dt>**Parametri del metodo verificati - Processo avviato**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-117"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="80e8f-118">Parametri del metodo controllati, processo avviato.</span><span class="sxs-lookup"><span data-stu-id="80e8f-118">Method parameters checked, job started.</span></span><br/> |
| <dl> <span data-ttu-id="80e8f-119"><dt>**Errore**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-119"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="80e8f-120">non riuscito.</span><span class="sxs-lookup"><span data-stu-id="80e8f-120">Failed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="80e8f-121"><dt>**Accesso negato**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-121"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="80e8f-122">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="80e8f-122">Access denied.</span></span><br/>                          |
| <dl> <span data-ttu-id="80e8f-123"><dt>**Non supportato**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-123"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="80e8f-124">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="80e8f-124">Not supported.</span></span><br/>                          |
| <dl> <span data-ttu-id="80e8f-125"><dt>**Lo stato è sconosciuto**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-125"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="80e8f-126">Lo stato è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="80e8f-126">Status is unknown.</span></span><br/>                      |
| <dl> <span data-ttu-id="80e8f-127"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-127"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="80e8f-128">Timeout.</span><span class="sxs-lookup"><span data-stu-id="80e8f-128">Time-out.</span></span><br/>                               |
| <dl> <span data-ttu-id="80e8f-129"><dt>**Parametro**</dt> <dt>32773 non valido</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-129"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="80e8f-130">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="80e8f-130">Invalid parameter.</span></span><br/>                      |
| <dl> <span data-ttu-id="80e8f-131"><dt>**Il sistema è in uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-131"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       | <span data-ttu-id="80e8f-132">Il sistema è in uso.</span><span class="sxs-lookup"><span data-stu-id="80e8f-132">System is in use.</span></span><br/>                       |
| <dl> <span data-ttu-id="80e8f-133"><dt>**Stato non valido per questa operazione**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-133"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="80e8f-134">Stato non valido per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="80e8f-134">Invalid state for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="80e8f-135"><dt>**Tipo di dati**</dt> <dt>32776 non corretto</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-135"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="80e8f-136">Tipo di dati non corretto.</span><span class="sxs-lookup"><span data-stu-id="80e8f-136">Incorrect data type.</span></span><br/>                    |
| <dl> <span data-ttu-id="80e8f-137"><dt>**Il sistema non è disponibile**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-137"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="80e8f-138">Il sistema non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="80e8f-138">System is not available.</span></span><br/>                |
| <dl> <span data-ttu-id="80e8f-139"><dt>**Memoria insufficiente**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-139"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="80e8f-140">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="80e8f-140">Out of memory.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="80e8f-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80e8f-141">Requirements</span></span>



| <span data-ttu-id="80e8f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="80e8f-142">Requirement</span></span> | <span data-ttu-id="80e8f-143">Valore</span><span class="sxs-lookup"><span data-stu-id="80e8f-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e8f-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80e8f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="80e8f-145">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="80e8f-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="80e8f-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80e8f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="80e8f-147">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="80e8f-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80e8f-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="80e8f-148">Namespace</span></span><br/>                | <span data-ttu-id="80e8f-149">Virtualizzazione \\ radice \\ V2</span><span class="sxs-lookup"><span data-stu-id="80e8f-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="80e8f-150">MOF</span><span class="sxs-lookup"><span data-stu-id="80e8f-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80e8f-151"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80e8f-152">DLL</span><span class="sxs-lookup"><span data-stu-id="80e8f-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80e8f-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80e8f-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="80e8f-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80e8f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e8f-155">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="80e8f-155">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

