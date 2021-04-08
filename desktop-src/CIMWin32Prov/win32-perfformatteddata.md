---
description: Classe di base astratta per le classi di dati calcolate preinstallate.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Classe Win32_PerfFormattedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: c28d0366c80e8838b36e17cd0fa1074b6ad33629
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966290"
---
# <a name="win32_perfformatteddata-class"></a><span data-ttu-id="8fb14-103">Win32 \_ PerfFormattedData (classe)</span><span class="sxs-lookup"><span data-stu-id="8fb14-103">Win32\_PerfFormattedData class</span></span>

<span data-ttu-id="8fb14-104">Classe di base astratta per le classi di dati calcolate preinstallate.</span><span class="sxs-lookup"><span data-stu-id="8fb14-104">An abstract base class for the preinstalled, calculated data classes.</span></span> <span data-ttu-id="8fb14-105">Un esempio di tale classe è [**Win32 \_ PerfFormattedData \_ perfdisk \_ disco logico**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="8fb14-105">An example of such a class is [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="8fb14-106">Queste classi contengono i valori calcolati forniti dalle [prestazioni provider di dati formattate](../wmisdk/formatted-performance-data-provider.md)ad alte prestazioni.</span><span class="sxs-lookup"><span data-stu-id="8fb14-106">These classes contain calculated values provided by the high-performance [Formatted Performance Data Provider](../wmisdk/formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="8fb14-107">La sintassi seguente è semplificata dal codice MOF e Mostra tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8fb14-107">The following syntax is simplified from MOF code and shows all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb14-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fb14-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a><span data-ttu-id="8fb14-109">Members</span><span class="sxs-lookup"><span data-stu-id="8fb14-109">Members</span></span>

<span data-ttu-id="8fb14-110">La classe **Win32 \_ PerfFormattedData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8fb14-110">The **Win32\_PerfFormattedData** class has these types of members:</span></span>

-   [<span data-ttu-id="8fb14-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8fb14-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8fb14-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8fb14-112">Properties</span></span>

<span data-ttu-id="8fb14-113">La classe **Win32 \_ PerfFormattedData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8fb14-113">The **Win32\_PerfFormattedData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8fb14-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="8fb14-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb14-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8fb14-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fb14-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8fb14-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fb14-117">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="8fb14-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8fb14-118">Breve descrizione testuale per la statistica o la metrica.</span><span class="sxs-lookup"><span data-stu-id="8fb14-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="8fb14-119">Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="8fb14-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fb14-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8fb14-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb14-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8fb14-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fb14-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8fb14-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fb14-123">Descrizione testuale della statistica o della metrica.</span><span class="sxs-lookup"><span data-stu-id="8fb14-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="8fb14-124">Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="8fb14-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fb14-125">**Frequency ( \_ oggetto)**</span><span class="sxs-lookup"><span data-stu-id="8fb14-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb14-126">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8fb14-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8fb14-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8fb14-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fb14-128">Frequenza in cicli al secondo della proprietà dell' **\_ oggetto timestamp** .</span><span class="sxs-lookup"><span data-stu-id="8fb14-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="8fb14-129">Se sottoclassato, il provider definisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8fb14-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="8fb14-130">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8fb14-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="8fb14-131">Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="8fb14-131">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fb14-132">**Frequenza \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="8fb14-132">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb14-133">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8fb14-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8fb14-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8fb14-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fb14-135">Frequenza in cicli al secondo della proprietà **Frequency \_ PerfTime** .</span><span class="sxs-lookup"><span data-stu-id="8fb14-135">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="8fb14-136">È possibile ottenere un valore chiamando la funzione [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)di Windows.</span><span class="sxs-lookup"><span data-stu-id="8fb14-136">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="8fb14-137">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8fb14-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="8fb14-138">Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="8fb14-138">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fb14-139">**Frequenza \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="8fb14-139">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb14-140">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8fb14-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8fb14-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8fb14-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fb14-142">Frequenza in cicli al secondo della proprietà **timestamp \_ Sys100NS** (10 milioni).</span><span class="sxs-lookup"><span data-stu-id="8fb14-142">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="8fb14-143">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8fb14-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="8fb14-144">Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="8fb14-144">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fb14-145">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8fb14-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb14-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8fb14-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fb14-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8fb14-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fb14-148">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="8fb14-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8fb14-149">Etichetta con la quale è nota la statistica o la metrica.</span><span class="sxs-lookup"><span data-stu-id="8fb14-149">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="8fb14-150">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="8fb14-150">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8fb14-151">Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="8fb14-151">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fb14-152">**Timestamp ( \_ oggetto)**</span><span class="sxs-lookup"><span data-stu-id="8fb14-152">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb14-153">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8fb14-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8fb14-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8fb14-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fb14-155">Timestamp definito dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8fb14-155">Object-defined timestamp.</span></span> <span data-ttu-id="8fb14-156">Il provider definisce la proprietà.</span><span class="sxs-lookup"><span data-stu-id="8fb14-156">The provider defines his property.</span></span>

<span data-ttu-id="8fb14-157">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8fb14-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="8fb14-158">Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="8fb14-158">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fb14-159">**Timestamp \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="8fb14-159">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb14-160">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8fb14-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8fb14-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8fb14-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fb14-162">Timestamp elevato del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="8fb14-162">High Performance counter timestamp.</span></span> <span data-ttu-id="8fb14-163">È possibile ottenere un valore chiamando la funzione [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)di Windows.</span><span class="sxs-lookup"><span data-stu-id="8fb14-163">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="8fb14-164">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8fb14-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="8fb14-165">Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="8fb14-165">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fb14-166">**Timestamp \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="8fb14-166">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fb14-167">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8fb14-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8fb14-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8fb14-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8fb14-169">Valore timestamp in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="8fb14-169">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="8fb14-170">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8fb14-170">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="8fb14-171">Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="8fb14-171">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fb14-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fb14-172">Remarks</span></span>

<span data-ttu-id="8fb14-173">La classe **Win32 \_ PerfFormattedData** è derivata da [**\_ Perf Win32**](win32-perf.md), derivata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="8fb14-173">The **Win32\_PerfFormattedData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span> <span data-ttu-id="8fb14-174">La classe si trova nello spazio dei nomi **\\ CIMV2 radice** .</span><span class="sxs-lookup"><span data-stu-id="8fb14-174">The class is found in the **root\\cimv2** namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb14-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fb14-175">Requirements</span></span>



| <span data-ttu-id="8fb14-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fb14-176">Requirement</span></span> | <span data-ttu-id="8fb14-177">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb14-177">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb14-178">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fb14-178">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb14-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fb14-179">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="8fb14-180">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fb14-180">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb14-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fb14-181">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="8fb14-182">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8fb14-182">Namespace</span></span><br/>                | <span data-ttu-id="8fb14-183">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8fb14-183">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="8fb14-184">MOF</span><span class="sxs-lookup"><span data-stu-id="8fb14-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fb14-185"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fb14-185"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="8fb14-186">DLL</span><span class="sxs-lookup"><span data-stu-id="8fb14-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fb14-187"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fb14-187"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fb14-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fb14-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb14-189">**\_Prestazioni Win32**</span><span class="sxs-lookup"><span data-stu-id="8fb14-189">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="8fb14-190">Classi del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="8fb14-190">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="8fb14-191">Accesso alle classi di prestazioni preinstallate WMI</span><span class="sxs-lookup"><span data-stu-id="8fb14-191">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="8fb14-192">Attività WMI: monitoraggio delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="8fb14-192">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="8fb14-193">Accesso ai dati sulle prestazioni nello script</span><span class="sxs-lookup"><span data-stu-id="8fb14-193">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
