---
description: Classe base per le classi del contatore delle prestazioni Win32 \_ PerfRawData e Win32 \_ PerfFormattedData.
ms.assetid: c754b619-a70f-4a56-8a43-2b36c8f8370b
ms.tgt_platform: multiple
title: Classe Win32_Perf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Perf
- Root\CIMV2.Win32_Perf.Caption
- Root\CIMV2.Win32_Perf.Description
- Root\CIMV2.Win32_Perf.Name
- Root\CIMV2.Win32_Perf.Frequency_Object
- Root\CIMV2.Win32_Perf.Frequency_PerfTime
- Root\CIMV2.Win32_Perf.Frequency_Sys100NS
- Root\CIMV2.Win32_Perf.Timestamp_Object
- Root\CIMV2.Win32_Perf.Timestamp_PerfTime
- Root\CIMV2.Win32_Perf.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 13b339e95e175e4d2dff50c0a9674f8002933c1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305154"
---
# <a name="win32_perf-class"></a><span data-ttu-id="f5714-103">\_Classe Perf Win32</span><span class="sxs-lookup"><span data-stu-id="f5714-103">Win32\_Perf class</span></span>

<span data-ttu-id="f5714-104">Classe base per le classi del contatore delle prestazioni [**Win32 \_ PerfRawData**](win32-perfrawdata.md) e [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).</span><span class="sxs-lookup"><span data-stu-id="f5714-104">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

<span data-ttu-id="f5714-105">**Win32 \_ Perf** definisce le proprietà timestamp e Frequency richieste usate negli algoritmi [**CounterType**](../wmisdk/countertype-qualifier.md) per le classi del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f5714-105">**Win32\_Perf** defines the required timestamp and frequency properties used in the [**CounterType**](../wmisdk/countertype-qualifier.md) algorithms for the performance counter classes.</span></span>

<span data-ttu-id="f5714-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f5714-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f5714-107">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f5714-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5714-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5714-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_Perf : CIM_StatisticalInformation
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

## <a name="members"></a><span data-ttu-id="f5714-109">Members</span><span class="sxs-lookup"><span data-stu-id="f5714-109">Members</span></span>

<span data-ttu-id="f5714-110">La **classe \_ Perf Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f5714-110">The **Win32\_Perf** class has these types of members:</span></span>

-   [<span data-ttu-id="f5714-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f5714-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5714-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f5714-112">Properties</span></span>

<span data-ttu-id="f5714-113">La **classe \_ Perf Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f5714-113">The **Win32\_Perf** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5714-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f5714-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5714-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5714-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5714-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5714-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5714-117">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="f5714-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f5714-118">Breve descrizione testuale per la statistica o la metrica.</span><span class="sxs-lookup"><span data-stu-id="f5714-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="f5714-119">Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="f5714-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5714-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f5714-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5714-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5714-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5714-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5714-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5714-123">Descrizione testuale della statistica o della metrica.</span><span class="sxs-lookup"><span data-stu-id="f5714-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="f5714-124">Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="f5714-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5714-125">**Frequency ( \_ oggetto)**</span><span class="sxs-lookup"><span data-stu-id="f5714-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5714-126">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f5714-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f5714-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5714-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5714-128">Frequenza in cicli al secondo della proprietà dell' **\_ oggetto timestamp** .</span><span class="sxs-lookup"><span data-stu-id="f5714-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="f5714-129">Se sottoclassato, il provider definisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="f5714-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="f5714-130">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f5714-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f5714-131">**Frequenza \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="f5714-131">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5714-132">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f5714-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f5714-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5714-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5714-134">Frequenza in cicli al secondo della proprietà **Frequency \_ PerfTime** .</span><span class="sxs-lookup"><span data-stu-id="f5714-134">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="f5714-135">È possibile ottenere un valore chiamando la funzione [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)di Windows.</span><span class="sxs-lookup"><span data-stu-id="f5714-135">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="f5714-136">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f5714-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f5714-137">**Frequenza \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="f5714-137">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5714-138">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f5714-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f5714-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5714-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5714-140">Frequenza in cicli al secondo della proprietà **timestamp \_ Sys100NS** (10 milioni).</span><span class="sxs-lookup"><span data-stu-id="f5714-140">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="f5714-141">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f5714-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f5714-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f5714-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5714-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f5714-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5714-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5714-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5714-145">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="f5714-145">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f5714-146">Etichetta con la quale è nota la statistica o la metrica.</span><span class="sxs-lookup"><span data-stu-id="f5714-146">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="f5714-147">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="f5714-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f5714-148">Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="f5714-148">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5714-149">**Timestamp ( \_ oggetto)**</span><span class="sxs-lookup"><span data-stu-id="f5714-149">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5714-150">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f5714-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f5714-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5714-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5714-152">Timestamp definito dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f5714-152">Object-defined timestamp.</span></span> <span data-ttu-id="f5714-153">Il provider definisce la proprietà.</span><span class="sxs-lookup"><span data-stu-id="f5714-153">The provider defines his property.</span></span>

<span data-ttu-id="f5714-154">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f5714-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f5714-155">**Timestamp \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="f5714-155">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5714-156">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f5714-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f5714-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5714-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5714-158">Timestamp elevato del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f5714-158">High Performance counter timestamp.</span></span> <span data-ttu-id="f5714-159">È possibile ottenere un valore chiamando la funzione [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)di Windows.</span><span class="sxs-lookup"><span data-stu-id="f5714-159">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="f5714-160">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f5714-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f5714-161">**Timestamp \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="f5714-161">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5714-162">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f5714-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f5714-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f5714-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5714-164">Valore timestamp in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="f5714-164">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="f5714-165">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f5714-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5714-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5714-166">Remarks</span></span>

<span data-ttu-id="f5714-167">La **classe \_ Perf Win32** deriva da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="f5714-167">The **Win32\_Perf** class derives from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5714-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5714-168">Requirements</span></span>



| <span data-ttu-id="f5714-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5714-169">Requirement</span></span> | <span data-ttu-id="f5714-170">Valore</span><span class="sxs-lookup"><span data-stu-id="f5714-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5714-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5714-171">Minimum supported client</span></span><br/> | <span data-ttu-id="f5714-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5714-172">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="f5714-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5714-173">Minimum supported server</span></span><br/> | <span data-ttu-id="f5714-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5714-174">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="f5714-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5714-175">Namespace</span></span><br/>                | <span data-ttu-id="f5714-176">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f5714-176">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="f5714-177">DLL</span><span class="sxs-lookup"><span data-stu-id="f5714-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5714-178"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5714-178"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5714-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5714-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5714-180">**\_STATISTICALINFORMATION CIM**</span><span class="sxs-lookup"><span data-stu-id="f5714-180">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dt>

[<span data-ttu-id="f5714-181">Classi del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="f5714-181">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="f5714-182">Accesso alle classi di prestazioni preinstallate WMI</span><span class="sxs-lookup"><span data-stu-id="f5714-182">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="f5714-183">Attività WMI: monitoraggio delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="f5714-183">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="f5714-184">Accesso ai dati sulle prestazioni nello script</span><span class="sxs-lookup"><span data-stu-id="f5714-184">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
