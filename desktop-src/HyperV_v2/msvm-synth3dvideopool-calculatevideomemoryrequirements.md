---
description: Calcola la quantità di memoria video necessaria per una macchina virtuale RemoteFX.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Metodo CalculateVideoMemoryRequirements della classe Msvm_Synth3dVideoPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129746"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a><span data-ttu-id="fb6ac-103">Metodo CalculateVideoMemoryRequirements della classe MSVM \_ Synth3dVideoPool</span><span class="sxs-lookup"><span data-stu-id="fb6ac-103">CalculateVideoMemoryRequirements method of the Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="fb6ac-104">Calcola la quantità di memoria video necessaria per una macchina virtuale RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-104">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6ac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb6ac-105">Syntax</span></span>


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a><span data-ttu-id="fb6ac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb6ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb6ac-107">*monitorResolution* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb6ac-107">*monitorResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ac-108">Risoluzione massima del monitor per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-108">The maximum monitor resolution for the virtual machine.</span></span> <span data-ttu-id="fb6ac-109">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-109">This must be one of the following values.</span></span>



| <span data-ttu-id="fb6ac-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fb6ac-110">Value</span></span>                                                                        | <span data-ttu-id="fb6ac-111">Significato</span><span class="sxs-lookup"><span data-stu-id="fb6ac-111">Meaning</span></span>                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="fb6ac-112"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-112"><dt>0</dt></span></span> </dl> | <span data-ttu-id="fb6ac-113">La risoluzione massima è 1024 768.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-113">The maximum resolution is 1024   768.</span></span><br/>  |
| <dl> <span data-ttu-id="fb6ac-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-114"><dt>1</dt></span></span> </dl> | <span data-ttu-id="fb6ac-115">La risoluzione massima è 1280 1024.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-115">The maximum resolution is 1280   1024.</span></span><br/> |
| <dl> <span data-ttu-id="fb6ac-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-116"><dt>2</dt></span></span> </dl> | <span data-ttu-id="fb6ac-117">La risoluzione massima è 1600 1200.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-117">The maximum resolution is 1600   1200.</span></span><br/> |
| <dl> <span data-ttu-id="fb6ac-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="fb6ac-119">La risoluzione massima è 1920 1200.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-119">The maximum resolution is 1920   1200.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fb6ac-120">*numberOfMonitors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb6ac-120">*numberOfMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ac-121">Numero massimo di monitoraggi per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-121">The maximum number of monitors for the virtual machine.</span></span> <span data-ttu-id="fb6ac-122">Il numero minimo di monitoraggi è uno e il valore massimo dipende dalla risoluzione massima dello schermo.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-122">The minimum number of monitors is one and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="fb6ac-123">La tabella seguente definisce il numero massimo di monitoraggi consentiti per diverse risoluzioni.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-123">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="fb6ac-124">Soluzione</span><span class="sxs-lookup"><span data-stu-id="fb6ac-124">Resolution</span></span>             | <span data-ttu-id="fb6ac-125">Numero massimo di monitoraggi</span><span class="sxs-lookup"><span data-stu-id="fb6ac-125">Maximum monitors</span></span> |
|------------------------|------------------|
| <span data-ttu-id="fb6ac-126">1024 768</span><span class="sxs-lookup"><span data-stu-id="fb6ac-126">1024   768</span></span><br/>  | <span data-ttu-id="fb6ac-127">4</span><span class="sxs-lookup"><span data-stu-id="fb6ac-127">4</span></span><br/>     |
| <span data-ttu-id="fb6ac-128">1280 1024</span><span class="sxs-lookup"><span data-stu-id="fb6ac-128">1280   1024</span></span><br/> | <span data-ttu-id="fb6ac-129">4</span><span class="sxs-lookup"><span data-stu-id="fb6ac-129">4</span></span><br/>     |
| <span data-ttu-id="fb6ac-130">1600 1200</span><span class="sxs-lookup"><span data-stu-id="fb6ac-130">1600   1200</span></span><br/> | <span data-ttu-id="fb6ac-131">3</span><span class="sxs-lookup"><span data-stu-id="fb6ac-131">3</span></span><br/>     |
| <span data-ttu-id="fb6ac-132">1920 1200</span><span class="sxs-lookup"><span data-stu-id="fb6ac-132">1920   1200</span></span><br/> | <span data-ttu-id="fb6ac-133">2</span><span class="sxs-lookup"><span data-stu-id="fb6ac-133">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="fb6ac-134">*requiredVideoMemory* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb6ac-134">*requiredVideoMemory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6ac-135">Riceve la quantità di memoria video richiesta, in byte.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-135">Receives the required amount of video memory, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb6ac-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb6ac-136">Return value</span></span>

<span data-ttu-id="fb6ac-137">Restituisce un codice di stato, che può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-137">Returns a status code, which can be one of the following values.</span></span>



| <span data-ttu-id="fb6ac-138">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb6ac-138">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="fb6ac-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb6ac-139">Description</span></span>                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="fb6ac-140"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-140"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="fb6ac-141">Successo.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-141">Successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="fb6ac-142"><dt>**Parametri del metodo controllati-processo avviato**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="fb6ac-143">Il processo è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-143">Job started.</span></span><br/>                               |
| <dl> <span data-ttu-id="fb6ac-144"><dt>**Errore**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-144"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="fb6ac-145">non riuscito.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-145">Failed.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fb6ac-146"><dt>**Accesso negato**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-146"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="fb6ac-147">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-147">Access denied.</span></span><br/>                             |
| <dl> <span data-ttu-id="fb6ac-148"><dt>**Non supportato**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-148"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="fb6ac-149">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-149">Not supported.</span></span><br/>                             |
| <dl> <span data-ttu-id="fb6ac-150"><dt>**Stato sconosciuto**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-150"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="fb6ac-151">Lo stato è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-151">Status is unknown.</span></span><br/>                         |
| <dl> <span data-ttu-id="fb6ac-152"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-152"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="fb6ac-153">Timeout.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-153">Timeout.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fb6ac-154"><dt>**Parametro non valido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-154"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="fb6ac-155">Un parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-155">A parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="fb6ac-156"><dt>**Sistema in uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-156"><dt>**System is in used**</dt> <dt>32774</dt></span></span> </dl>                      | <span data-ttu-id="fb6ac-157">Il sistema è in uso.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-157">System is in use.</span></span><br/>                          |
| <dl> <span data-ttu-id="fb6ac-158"><dt>**Stato non valido per l'operazione**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-158"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="fb6ac-159">Lo stato non è valido per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-159">The state is not valid for this operation.</span></span><br/> |
| <dl> <span data-ttu-id="fb6ac-160"><dt>**Tipo di dati non corretto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-160"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="fb6ac-161">Tipo di dati non corretto.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-161">Incorrect data type.</span></span><br/>                       |
| <dl> <span data-ttu-id="fb6ac-162">Il <dt>**sistema non è disponibile**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-162"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="fb6ac-163">Il sistema non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-163">System is not available.</span></span><br/>                   |
| <dl> <span data-ttu-id="fb6ac-164"><dt>**Memoria insufficiente**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-164"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="fb6ac-165">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-165">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="fb6ac-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb6ac-166">Remarks</span></span>

<span data-ttu-id="fb6ac-167">Questo metodo viene in genere chiamato sul sistema host per determinare se l'host dispone di memoria video disponibile sufficiente per ospitare una macchina virtuale RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-167">This method is typically called on the host system to determine if the host has enough available video memory to host a RemoteFX virtual machine.</span></span> <span data-ttu-id="fb6ac-168">A tale scopo, confrontare la quantità di memoria video calcolata da questo metodo con la proprietà [**MSVM \_ PhysicalGPUInfo. AvailableVideoMemory**](msvm-physicalgpuinfo.md) per determinare se il computer host dispone di memoria video disponibile sufficiente.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-168">To do this, you compare the amount of video memory calculated by this method with the [**Msvm\_PhysicalGPUInfo.AvailableVideoMemory**](msvm-physicalgpuinfo.md) property to determine if the host machine has enough available video memory.</span></span> <span data-ttu-id="fb6ac-169">È possibile utilizzare queste informazioni per determinare se una macchina virtuale può essere spostata nel sistema host.</span><span class="sxs-lookup"><span data-stu-id="fb6ac-169">You can use this information to determine if a virtual machine can be moved to the host system.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb6ac-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb6ac-170">Requirements</span></span>



| <span data-ttu-id="fb6ac-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb6ac-171">Requirement</span></span> | <span data-ttu-id="fb6ac-172">Valore</span><span class="sxs-lookup"><span data-stu-id="fb6ac-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6ac-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb6ac-173">Minimum supported client</span></span><br/> | <span data-ttu-id="fb6ac-174">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fb6ac-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fb6ac-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb6ac-175">Minimum supported server</span></span><br/> | <span data-ttu-id="fb6ac-176">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fb6ac-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb6ac-177">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fb6ac-177">Namespace</span></span><br/>                | <span data-ttu-id="fb6ac-178">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fb6ac-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fb6ac-179">MOF</span><span class="sxs-lookup"><span data-stu-id="fb6ac-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb6ac-180"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb6ac-181">DLL</span><span class="sxs-lookup"><span data-stu-id="fb6ac-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb6ac-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fb6ac-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fb6ac-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb6ac-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6ac-184">**\_PhysicalGPUInfo MSVM**</span><span class="sxs-lookup"><span data-stu-id="fb6ac-184">**Msvm\_PhysicalGPUInfo**</span></span>](msvm-physicalgpuinfo.md)
</dt> <dt>

[<span data-ttu-id="fb6ac-185">**\_Synth3dVideoPool MSVM**</span><span class="sxs-lookup"><span data-stu-id="fb6ac-185">**Msvm\_Synth3dVideoPool**</span></span>](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




