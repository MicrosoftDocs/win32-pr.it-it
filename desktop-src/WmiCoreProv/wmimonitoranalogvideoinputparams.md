---
description: Rappresenta i parametri di input video analogici di un monitor del computer.
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: Classe WmiMonitorAnalogVideoInputParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967852"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a><span data-ttu-id="bcb9a-103">Classe WmiMonitorAnalogVideoInputParams</span><span class="sxs-lookup"><span data-stu-id="bcb9a-103">WmiMonitorAnalogVideoInputParams class</span></span>

<span data-ttu-id="bcb9a-104">La classe WMI **WmiMonitorAnalogVideoInputParams** rappresenta i parametri di input video analogici di un monitor computer.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-104">The **WmiMonitorAnalogVideoInputParams** WMI class represents the analog video input parameters of a computer monitor.</span></span> <span data-ttu-id="bcb9a-105">I dati in questa classe corrispondono ai dati nella definizione del video di input di video Electronics Standard Association (VESA) Enhanced Extended Display Data (E-EDID) standard.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="bcb9a-106">Un'istanza di questa classe è disponibile solo se il valore della proprietà **VideoInputType** della classe [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) è "analogico".</span><span class="sxs-lookup"><span data-stu-id="bcb9a-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Analog".</span></span>

## <a name="syntax"></a><span data-ttu-id="bcb9a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcb9a-107">Syntax</span></span>

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a><span data-ttu-id="bcb9a-108">Members</span><span class="sxs-lookup"><span data-stu-id="bcb9a-108">Members</span></span>

<span data-ttu-id="bcb9a-109">La classe **WmiMonitorAnalogVideoInputParams** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bcb9a-109">The **WmiMonitorAnalogVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="bcb9a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bcb9a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bcb9a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bcb9a-111">Properties</span></span>

<span data-ttu-id="bcb9a-112">La classe **WmiMonitorAnalogVideoInputParams** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-112">The **WmiMonitorAnalogVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bcb9a-113">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcb9a-114">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bcb9a-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bcb9a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcb9a-116">Indica il monitoraggio attivo.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="bcb9a-117">**CompositeSyncSupported**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-117">**CompositeSyncSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcb9a-118">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bcb9a-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bcb9a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcb9a-120">Indica se la sincronizzazione composita è supportata.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-120">Indicates whether composite sync is supported.</span></span>



| <span data-ttu-id="bcb9a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bcb9a-121">Value</span></span>                                                                              | <span data-ttu-id="bcb9a-122">Significato</span><span class="sxs-lookup"><span data-stu-id="bcb9a-122">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="bcb9a-123"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-123"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-124">La sincronizzazione composita sulla linea di sincronizzazione orizzontale è supportata.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-124">Composite sync on horizontal sync line is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="bcb9a-125"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-125"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-126">La sincronizzazione composita sulla linea di sincronizzazione orizzontale non è supportata.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-126">Composite sync on horizontal sync line is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bcb9a-127">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-127">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcb9a-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcb9a-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bcb9a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcb9a-130">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bcb9a-131">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-131">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="bcb9a-132">**SeparateSyncsSupported**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-132">**SeparateSyncsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcb9a-133">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bcb9a-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bcb9a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcb9a-135">Indica se sono supportate sincronizzazioni separate.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-135">Indicates whether separate syncs are supported.</span></span>



| <span data-ttu-id="bcb9a-136">Valore</span><span class="sxs-lookup"><span data-stu-id="bcb9a-136">Value</span></span>                                                                              | <span data-ttu-id="bcb9a-137">Significato</span><span class="sxs-lookup"><span data-stu-id="bcb9a-137">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bcb9a-138"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-138"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-139">Sono supportate le sincronizzazioni separate.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-139">Separate syncs are supported.</span></span><br/>     |
| <dl> <span data-ttu-id="bcb9a-140"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-140"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-141">Le sincronizzazioni separate non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-141">Separate syncs are not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bcb9a-142">**SerrationOfVsyncRequired**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-142">**SerrationOfVsyncRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcb9a-143">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bcb9a-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bcb9a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcb9a-145">Indica se è necessaria la seghettazione dell'impulso di sincronizzazione verticale.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-145">Indicates whether vertical sync pulse serration is required.</span></span>



| <span data-ttu-id="bcb9a-146">Valore</span><span class="sxs-lookup"><span data-stu-id="bcb9a-146">Value</span></span>                                                                              | <span data-ttu-id="bcb9a-147">Significato</span><span class="sxs-lookup"><span data-stu-id="bcb9a-147">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bcb9a-148"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-148"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-149">La seghettazione dell'impulso di sincronizzazione verticale è obbligatoria quando si usa la sincronizzazione composita o il video Sync-on-Green.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-149">Serration of the vertical sync pulse is required when composite sync or sync-on-green video is used.</span></span><br/>     |
| <dl> <span data-ttu-id="bcb9a-150"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-150"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-151">La seghettazione dell'impulso di sincronizzazione verticale non è necessaria quando si usa la sincronizzazione composita o il video Sync-on-Green.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-151">Serration of the vertical sync pulse is not required when composite sync or sync-on-green video is used.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bcb9a-152">**SetupExpected**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-152">**SetupExpected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcb9a-153">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bcb9a-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bcb9a-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcb9a-155">Indica se è previsto il programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-155">Indicates whether setup is expected.</span></span>



| <span data-ttu-id="bcb9a-156">Valore</span><span class="sxs-lookup"><span data-stu-id="bcb9a-156">Value</span></span>                                                                              | <span data-ttu-id="bcb9a-157">Significato</span><span class="sxs-lookup"><span data-stu-id="bcb9a-157">Meaning</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bcb9a-158"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-158"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-159">Il monitoraggio prevede una configurazione vuota o un piedistallo per ogni livello di segnale standard appropriato.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-159">Monitor expects a blank-to-blank setup or pedestal per appropriate Signal Level Standard.</span></span><br/>                      |
| <dl> <span data-ttu-id="bcb9a-160"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-160"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-161">Il monitoraggio non prevede una configurazione o un piedistallo da zero a vuoto in base allo standard del livello di segnale appropriato.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-161">Monitor does not expect a blank-to-blank setup or pedestal according to the appropriate signal level standard.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bcb9a-162">**SignalLevelStandard**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-162">**SignalLevelStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcb9a-163">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bcb9a-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bcb9a-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcb9a-165">Livello di segnale standard per le connessioni a Enhanced Video Connector (EVC).</span><span class="sxs-lookup"><span data-stu-id="bcb9a-165">Signal level standard for Enhanced video connector (EVC) connections.</span></span>



| <span data-ttu-id="bcb9a-166">Valore</span><span class="sxs-lookup"><span data-stu-id="bcb9a-166">Value</span></span>                                                                              | <span data-ttu-id="bcb9a-167">Significato</span><span class="sxs-lookup"><span data-stu-id="bcb9a-167">Meaning</span></span>                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="bcb9a-168"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-168"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-169">0.7, 0.3 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="bcb9a-169">0.7,0.3\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="bcb9a-170"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-170"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-171">0.714, 0.286 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="bcb9a-171">0.714,0.286\[V\]</span></span><br/> |
| <dl> <span data-ttu-id="bcb9a-172"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-172"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-173">1.0, 0.4 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="bcb9a-173">1.0,0.4\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="bcb9a-174"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-174"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-175">0.7, 0,0 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="bcb9a-175">0.7,0.0\[V\]</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="bcb9a-176">**SyncOnGreenVideoSupported**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-176">**SyncOnGreenVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcb9a-177">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bcb9a-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bcb9a-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bcb9a-179">Indica se la sincronizzazione in verde è supportata.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-179">Indicates whether sync on green is supported.</span></span>



| <span data-ttu-id="bcb9a-180">Valore</span><span class="sxs-lookup"><span data-stu-id="bcb9a-180">Value</span></span>                                                                              | <span data-ttu-id="bcb9a-181">Significato</span><span class="sxs-lookup"><span data-stu-id="bcb9a-181">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="bcb9a-182"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-183">La sincronizzazione su un video verde è supportata.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-183">Sync on green video is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="bcb9a-184"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="bcb9a-185">La sincronizzazione su un video verde non è supportata.</span><span class="sxs-lookup"><span data-stu-id="bcb9a-185">Sync on green video is not supported.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcb9a-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcb9a-186">Requirements</span></span>



| <span data-ttu-id="bcb9a-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcb9a-187">Requirement</span></span> | <span data-ttu-id="bcb9a-188">Valore</span><span class="sxs-lookup"><span data-stu-id="bcb9a-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb9a-189">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcb9a-189">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb9a-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcb9a-190">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bcb9a-191">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcb9a-191">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb9a-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcb9a-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bcb9a-193">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bcb9a-193">Namespace</span></span><br/>                | <span data-ttu-id="bcb9a-194">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="bcb9a-194">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="bcb9a-195">MOF</span><span class="sxs-lookup"><span data-stu-id="bcb9a-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcb9a-196"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-196"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcb9a-197">DLL</span><span class="sxs-lookup"><span data-stu-id="bcb9a-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcb9a-198"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcb9a-198"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcb9a-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcb9a-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb9a-200">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="bcb9a-200">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




