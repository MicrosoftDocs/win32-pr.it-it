---
description: Classe di base astratta per tutte le classi del contatore delle prestazioni raw concrete.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Classe Win32_PerfRawData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfRawData
- Win32_PerfRawData.Caption
- Win32_PerfRawData.Description
- Win32_PerfRawData.Name
- Win32_PerfRawData.Frequency_Object
- Win32_PerfRawData.Frequency_PerfTime
- Win32_PerfRawData.Frequency_Sys100NS
- Win32_PerfRawData.Timestamp_Object
- Win32_PerfRawData.Timestamp_PerfTime
- Win32_PerfRawData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: db5b74ae7508d15a48d2f71c3a586ad7e40362f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524273"
---
# <a name="win32_perfrawdata-class"></a><span data-ttu-id="5c24b-103">Win32 \_ PerfRawData (classe)</span><span class="sxs-lookup"><span data-stu-id="5c24b-103">Win32\_PerfRawData class</span></span>

<span data-ttu-id="5c24b-104">Classe di base astratta per tutte le classi del contatore delle prestazioni raw concrete.</span><span class="sxs-lookup"><span data-stu-id="5c24b-104">The abstract base class for all concrete raw performance counter classes.</span></span>

<span data-ttu-id="5c24b-105">Per essere visualizzati in monitoraggio di sistema, le classi del contatore delle prestazioni devono essere aggiunte allo \\ spazio dei nomi CIMV2 radice e derivate da **Win32 \_ PerfRawData**.</span><span class="sxs-lookup"><span data-stu-id="5c24b-105">To appear in System Monitor, performance counter classes must be added to the root\\cimv2 namespace and derived from **Win32\_PerfRawData**.</span></span> <span data-ttu-id="5c24b-106">I dati in queste classi sono forniti dal [provider del contatore delle prestazioni](../wmisdk/performance-counter-provider.md)a prestazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="5c24b-106">Data in these classes are provided by the high-performance [Performance Counter Provider](../wmisdk/performance-counter-provider.md).</span></span>

<span data-ttu-id="5c24b-107">Le proprietà seguenti vengono ereditate quando una classe viene derivata da **Win32 \_ PerfRawData**:</span><span class="sxs-lookup"><span data-stu-id="5c24b-107">The following properties are inherited when a class is derived from **Win32\_PerfRawData**:</span></span>

-   <span data-ttu-id="5c24b-108">**Timestamp \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="5c24b-108">**Timestamp\_PerfTime**</span></span>
-   <span data-ttu-id="5c24b-109">**Timestamp \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="5c24b-109">**Timestamp\_Sys100NS**</span></span>
-   <span data-ttu-id="5c24b-110">**Timestamp ( \_ oggetto)**</span><span class="sxs-lookup"><span data-stu-id="5c24b-110">**Timestamp\_Object**</span></span>
-   <span data-ttu-id="5c24b-111">**Frequenza \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="5c24b-111">**Frequency\_PerfTime**</span></span>
-   <span data-ttu-id="5c24b-112">**Frequenza \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="5c24b-112">**Frequency\_Sys100NS**</span></span>
-   <span data-ttu-id="5c24b-113">**Frequency ( \_ oggetto)**</span><span class="sxs-lookup"><span data-stu-id="5c24b-113">**Frequency\_Object**</span></span>

<span data-ttu-id="5c24b-114">In ogni caso, le proprietà devono essere compilate dal provider o la classe non può essere visualizzata in Monitor di sistema.</span><span class="sxs-lookup"><span data-stu-id="5c24b-114">In each case, the properties must be filled out by the provider or the class cannot be displayed in System Monitor.</span></span> <span data-ttu-id="5c24b-115">Queste proprietà vengono utilizzate per calcolare le formule del tipo di contatore in base ai consumer dei dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5c24b-115">These properties are used to compute counter type formulas by consumers of performance data.</span></span>

<span data-ttu-id="5c24b-116">La sintassi seguente è semplificata dal codice MOF e Mostra tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5c24b-116">The following syntax is simplified from MOF code and shows all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c24b-117">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c24b-117">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfRawData : Win32_Perf
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

## <a name="members"></a><span data-ttu-id="5c24b-118">Members</span><span class="sxs-lookup"><span data-stu-id="5c24b-118">Members</span></span>

<span data-ttu-id="5c24b-119">La classe **Win32 \_ PerfRawData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5c24b-119">The **Win32\_PerfRawData** class has these types of members:</span></span>

-   [<span data-ttu-id="5c24b-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c24b-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c24b-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c24b-121">Properties</span></span>

<span data-ttu-id="5c24b-122">La classe **Win32 \_ PerfRawData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5c24b-122">The **Win32\_PerfRawData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c24b-123">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5c24b-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24b-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c24b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c24b-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c24b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c24b-126">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="5c24b-126">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5c24b-127">Breve descrizione testuale per la statistica o la metrica.</span><span class="sxs-lookup"><span data-stu-id="5c24b-127">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="5c24b-128">Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="5c24b-128">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c24b-129">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5c24b-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24b-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c24b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c24b-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c24b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c24b-132">Descrizione testuale della statistica o della metrica.</span><span class="sxs-lookup"><span data-stu-id="5c24b-132">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="5c24b-133">Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="5c24b-133">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c24b-134">**Frequency ( \_ oggetto)**</span><span class="sxs-lookup"><span data-stu-id="5c24b-134">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24b-135">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5c24b-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c24b-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c24b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c24b-137">Frequenza in cicli al secondo della proprietà dell' **\_ oggetto timestamp** .</span><span class="sxs-lookup"><span data-stu-id="5c24b-137">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="5c24b-138">Se sottoclassato, il provider definisce questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5c24b-138">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="5c24b-139">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c24b-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="5c24b-140">Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="5c24b-140">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c24b-141">**Frequenza \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="5c24b-141">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24b-142">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5c24b-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c24b-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c24b-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c24b-144">Frequenza in cicli al secondo della proprietà **Frequency \_ PerfTime** .</span><span class="sxs-lookup"><span data-stu-id="5c24b-144">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="5c24b-145">È possibile ottenere un valore chiamando la funzione [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)di Windows.</span><span class="sxs-lookup"><span data-stu-id="5c24b-145">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="5c24b-146">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c24b-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="5c24b-147">Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="5c24b-147">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c24b-148">**Frequenza \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="5c24b-148">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24b-149">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5c24b-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c24b-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c24b-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c24b-151">Frequenza in cicli al secondo della proprietà **timestamp \_ Sys100NS** (10 milioni).</span><span class="sxs-lookup"><span data-stu-id="5c24b-151">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="5c24b-152">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c24b-152">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="5c24b-153">Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="5c24b-153">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c24b-154">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5c24b-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24b-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c24b-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c24b-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c24b-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c24b-157">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="5c24b-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5c24b-158">Etichetta con la quale è nota la statistica o la metrica.</span><span class="sxs-lookup"><span data-stu-id="5c24b-158">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="5c24b-159">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="5c24b-159">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5c24b-160">Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="5c24b-160">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c24b-161">**Timestamp ( \_ oggetto)**</span><span class="sxs-lookup"><span data-stu-id="5c24b-161">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24b-162">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5c24b-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c24b-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c24b-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c24b-164">Timestamp definito dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c24b-164">Object-defined timestamp.</span></span> <span data-ttu-id="5c24b-165">Il provider definisce la proprietà.</span><span class="sxs-lookup"><span data-stu-id="5c24b-165">The provider defines his property.</span></span>

<span data-ttu-id="5c24b-166">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c24b-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="5c24b-167">Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="5c24b-167">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c24b-168">**Timestamp \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="5c24b-168">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24b-169">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5c24b-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c24b-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c24b-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c24b-171">Timestamp elevato del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5c24b-171">High Performance counter timestamp.</span></span> <span data-ttu-id="5c24b-172">È possibile ottenere un valore chiamando la funzione [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)di Windows.</span><span class="sxs-lookup"><span data-stu-id="5c24b-172">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="5c24b-173">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c24b-173">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="5c24b-174">Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="5c24b-174">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c24b-175">**Timestamp \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="5c24b-175">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c24b-176">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5c24b-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5c24b-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c24b-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c24b-178">Valore timestamp in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="5c24b-178">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="5c24b-179">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c24b-179">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="5c24b-180">Questa proprietà viene ereditata [**da \_ Perf Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="5c24b-180">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c24b-181">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c24b-181">Remarks</span></span>

<span data-ttu-id="5c24b-182">La classe **Win32 \_ PerfRawData** è derivata da [**\_ Perf Win32**](win32-perf.md), derivata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="5c24b-182">The **Win32\_PerfRawData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

<span data-ttu-id="5c24b-183">Tutte le classi derivate da [**\_ Perf Win32**](win32-perf.md) sono progettate per essere utilizzate con un oggetto di [*aggiornamento*](../wmisdk/gloss-r.md) .</span><span class="sxs-lookup"><span data-stu-id="5c24b-183">All classes derived from [**Win32\_Perf**](win32-perf.md) are designed to be used with a [*refresher*](../wmisdk/gloss-r.md) object.</span></span> <span data-ttu-id="5c24b-184">Per ulteriori informazioni su come creare e utilizzare un oggetto di aggiornamento nel linguaggio di programmazione C++, vedere [accesso ai dati sulle prestazioni in c++](../wmisdk/accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="5c24b-184">For more information about how to create and use a refresher object in the C++ programming language, see [Accessing Performance Data in C++](../wmisdk/accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="5c24b-185">Per ulteriori informazioni su come creare e utilizzare un oggetto di aggiornamento in un linguaggio di programmazione script, vedere [aggiornamento di dati WMI negli script](../wmisdk/refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="5c24b-185">For more information about how to create and use a refresher object in a script programming language, see [Refreshing WMI Data in Scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c24b-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c24b-186">Requirements</span></span>



| <span data-ttu-id="5c24b-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c24b-187">Requirement</span></span> | <span data-ttu-id="5c24b-188">Valore</span><span class="sxs-lookup"><span data-stu-id="5c24b-188">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c24b-189">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c24b-189">Minimum supported client</span></span><br/> | <span data-ttu-id="5c24b-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c24b-190">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="5c24b-191">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c24b-191">Minimum supported server</span></span><br/> | <span data-ttu-id="5c24b-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c24b-192">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="5c24b-193">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5c24b-193">Namespace</span></span><br/>                | <span data-ttu-id="5c24b-194">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5c24b-194">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="5c24b-195">MOF</span><span class="sxs-lookup"><span data-stu-id="5c24b-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c24b-196"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c24b-196"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="5c24b-197">DLL</span><span class="sxs-lookup"><span data-stu-id="5c24b-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c24b-198"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c24b-198"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c24b-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c24b-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c24b-200">**\_Prestazioni Win32**</span><span class="sxs-lookup"><span data-stu-id="5c24b-200">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="5c24b-201">Classi del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="5c24b-201">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="5c24b-202">Accesso alle classi di prestazioni preinstallate WMI</span><span class="sxs-lookup"><span data-stu-id="5c24b-202">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="5c24b-203">Attività WMI: monitoraggio delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="5c24b-203">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="5c24b-204">Accesso ai dati sulle prestazioni nello script</span><span class="sxs-lookup"><span data-stu-id="5c24b-204">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
