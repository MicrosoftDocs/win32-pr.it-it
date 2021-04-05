---
description: Modifica i dati dell'impostazione per il servizio.
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
ms.openlocfilehash: b680f5f46d99d46f99094e05db653083fd7ae952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752223"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="4f9bf-103">Metodo ModifyServiceSettings della classe MSVM \_ MetricService</span><span class="sxs-lookup"><span data-stu-id="4f9bf-103">ModifyServiceSettings method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="4f9bf-104">Modifica i dati dell'impostazione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f9bf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f9bf-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4f9bf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f9bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f9bf-107">*SettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f9bf-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f9bf-108">Contiene un'istanza incorporata della [**classe \_ MetricServiceSettingData di MSVM**](msvm-metricservicesettingdata.md) che contiene i dati di impostazione modificati per il servizio.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-108">Contains an embedded instance of the [**Msvm\_MetricServiceSettingData**](msvm-metricservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="4f9bf-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4f9bf-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f9bf-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f9bf-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f9bf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f9bf-111">Return value</span></span>

<span data-ttu-id="4f9bf-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-112">This method returns one of the following values.</span></span>



| <span data-ttu-id="4f9bf-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f9bf-113">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="4f9bf-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f9bf-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="4f9bf-115"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-115"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="4f9bf-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="4f9bf-117"><dt>**Parametri del metodo controllati-processo avviato**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-117"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="4f9bf-118">Parametri del metodo controllati, processo avviato.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-118">Method parameters checked, job started.</span></span><br/> |
| <dl> <span data-ttu-id="4f9bf-119"><dt>**Errore**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-119"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="4f9bf-120">non riuscito.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-120">Failed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="4f9bf-121"><dt>**Accesso negato**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-121"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="4f9bf-122">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-122">Access denied.</span></span><br/>                          |
| <dl> <span data-ttu-id="4f9bf-123"><dt>**Non supportato**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-123"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="4f9bf-124">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-124">Not supported.</span></span><br/>                          |
| <dl> <span data-ttu-id="4f9bf-125"><dt>**Stato sconosciuto**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-125"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="4f9bf-126">Lo stato è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-126">Status is unknown.</span></span><br/>                      |
| <dl> <span data-ttu-id="4f9bf-127"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-127"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="4f9bf-128">Timeout.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-128">Time-out.</span></span><br/>                               |
| <dl> <span data-ttu-id="4f9bf-129"><dt>**Parametro non valido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-129"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="4f9bf-130">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-130">Invalid parameter.</span></span><br/>                      |
| <dl> <span data-ttu-id="4f9bf-131">Il <dt>**sistema è in uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-131"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       | <span data-ttu-id="4f9bf-132">Il sistema è in uso.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-132">System is in use.</span></span><br/>                       |
| <dl> <span data-ttu-id="4f9bf-133"><dt>**Stato non valido per l'operazione**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-133"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="4f9bf-134">Stato non valido per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-134">Invalid state for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="4f9bf-135"><dt>**Tipo di dati non corretto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-135"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="4f9bf-136">Tipo di dati non corretto.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-136">Incorrect data type.</span></span><br/>                    |
| <dl> <span data-ttu-id="4f9bf-137">Il <dt>**sistema non è disponibile**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-137"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="4f9bf-138">Il sistema non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-138">System is not available.</span></span><br/>                |
| <dl> <span data-ttu-id="4f9bf-139"><dt>**Memoria insufficiente**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-139"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="4f9bf-140">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="4f9bf-140">Out of memory.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="4f9bf-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f9bf-141">Requirements</span></span>



| <span data-ttu-id="4f9bf-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f9bf-142">Requirement</span></span> | <span data-ttu-id="4f9bf-143">Valore</span><span class="sxs-lookup"><span data-stu-id="4f9bf-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f9bf-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f9bf-144">Minimum supported client</span></span><br/> | <span data-ttu-id="4f9bf-145">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4f9bf-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4f9bf-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f9bf-146">Minimum supported server</span></span><br/> | <span data-ttu-id="4f9bf-147">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4f9bf-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f9bf-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f9bf-148">Namespace</span></span><br/>                | <span data-ttu-id="4f9bf-149">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4f9bf-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4f9bf-150">MOF</span><span class="sxs-lookup"><span data-stu-id="4f9bf-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f9bf-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f9bf-152">DLL</span><span class="sxs-lookup"><span data-stu-id="4f9bf-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f9bf-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f9bf-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4f9bf-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f9bf-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f9bf-155">**\_MetricService MSVM**</span><span class="sxs-lookup"><span data-stu-id="4f9bf-155">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

