---
description: La \_ classe CIM DeviceErrorCounts è una classe statistica che contiene contatori correlati agli errori per un dispositivo logico. I tipi di errore sono definiti da CCITT (REC X. 733) e ISO (IEC 10164-4).
ms.assetid: d65cbc78-40f2-4846-bd47-76e04b2f588b
ms.tgt_platform: multiple
title: Classe CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts
- CIM_DeviceErrorCounts.Caption
- CIM_DeviceErrorCounts.Description
- CIM_DeviceErrorCounts.CriticalErrorCount
- CIM_DeviceErrorCounts.DeviceCreationClassName
- CIM_DeviceErrorCounts.DeviceID
- CIM_DeviceErrorCounts.Name
- CIM_DeviceErrorCounts.IndeterminateErrorCount
- CIM_DeviceErrorCounts.MajorErrorCount
- CIM_DeviceErrorCounts.MinorErrorCount
- CIM_DeviceErrorCounts.SystemCreationClassName
- CIM_DeviceErrorCounts.SystemName
- CIM_DeviceErrorCounts.WarningCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1602e68b7254811ba8c09726feda8baa7bf23d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966231"
---
# <a name="cim_deviceerrorcounts-class"></a><span data-ttu-id="be0da-104">CIM \_ DeviceErrorCounts (classe)</span><span class="sxs-lookup"><span data-stu-id="be0da-104">CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="be0da-105">La classe **CIM \_ DeviceErrorCounts** è una classe statistica che contiene contatori correlati agli errori per un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="be0da-105">The **CIM\_DeviceErrorCounts** class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="be0da-106">I tipi di errore sono definiti da CCITT (REC X. 733) e ISO (IEC 10164-4).</span><span class="sxs-lookup"><span data-stu-id="be0da-106">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be0da-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="be0da-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="be0da-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="be0da-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="be0da-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="be0da-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="be0da-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="be0da-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="be0da-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be0da-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{117FDB8C-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceErrorCounts : CIM_StatisticalInformation
{
  string Caption;
  string Description;
  uint64 CriticalErrorCount;
  string DeviceCreationClassName;
  string DeviceID;
  string Name;
  uint64 IndeterminateErrorCount;
  uint64 MajorErrorCount;
  uint64 MinorErrorCount;
  string SystemCreationClassName;
  string SystemName;
  uint64 WarningCount;
};
```

## <a name="members"></a><span data-ttu-id="be0da-112">Members</span><span class="sxs-lookup"><span data-stu-id="be0da-112">Members</span></span>

<span data-ttu-id="be0da-113">La classe **CIM \_ DeviceErrorCounts** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="be0da-113">The **CIM\_DeviceErrorCounts** class has these types of members:</span></span>

-   [<span data-ttu-id="be0da-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="be0da-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="be0da-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="be0da-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="be0da-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="be0da-116">Methods</span></span>

<span data-ttu-id="be0da-117">La classe **CIM \_ DeviceErrorCounts** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="be0da-117">The **CIM\_DeviceErrorCounts** class has these methods.</span></span>



| <span data-ttu-id="be0da-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="be0da-118">Method</span></span>                                                                     | <span data-ttu-id="be0da-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be0da-119">Description</span></span>                                                               |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="be0da-120">**ResetCounter**</span><span class="sxs-lookup"><span data-stu-id="be0da-120">**ResetCounter**</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md) | <span data-ttu-id="be0da-121">Reimposta i contatori degli errori e degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="be0da-121">Resets the error and warning counters.</span></span> <span data-ttu-id="be0da-122">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="be0da-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="be0da-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="be0da-123">Properties</span></span>

<span data-ttu-id="be0da-124">La classe **CIM \_ DeviceErrorCounts** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="be0da-124">The **CIM\_DeviceErrorCounts** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be0da-125">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="be0da-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0da-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="be0da-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be0da-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be0da-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be0da-128">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="be0da-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="be0da-129">Breve descrizione testuale per la statistica o la metrica.</span><span class="sxs-lookup"><span data-stu-id="be0da-129">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="be0da-130">Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="be0da-130">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="be0da-131">**CriticalErrorCount**</span><span class="sxs-lookup"><span data-stu-id="be0da-131">**CriticalErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0da-132">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be0da-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be0da-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be0da-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be0da-134">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="be0da-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="be0da-135">Conteggio degli errori critici.</span><span class="sxs-lookup"><span data-stu-id="be0da-135">Count of the critical errors.</span></span>

<span data-ttu-id="be0da-136">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="be0da-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="be0da-137">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="be0da-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0da-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="be0da-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be0da-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be0da-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be0da-140">Descrizione testuale della statistica o della metrica.</span><span class="sxs-lookup"><span data-stu-id="be0da-140">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="be0da-141">Questa proprietà viene ereditata da [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="be0da-141">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="be0da-142">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="be0da-142">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0da-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="be0da-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be0da-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be0da-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be0da-145">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="be0da-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="be0da-146">Proprietà **CreationClassName** del dispositivo di ambito.</span><span class="sxs-lookup"><span data-stu-id="be0da-146">The scoping device's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="be0da-147">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="be0da-147">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0da-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="be0da-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be0da-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be0da-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be0da-150">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="be0da-150">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="be0da-151">Identificatore del dispositivo di ambito.</span><span class="sxs-lookup"><span data-stu-id="be0da-151">The scoping device's identifier.</span></span>

</dd> <dt>

<span data-ttu-id="be0da-152">**IndeterminateErrorCount**</span><span class="sxs-lookup"><span data-stu-id="be0da-152">**IndeterminateErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0da-153">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be0da-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be0da-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be0da-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be0da-155">Conteggio degli errori indeterminati.</span><span class="sxs-lookup"><span data-stu-id="be0da-155">Count of the indeterminate errors.</span></span>

<span data-ttu-id="be0da-156">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="be0da-156">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="be0da-157">**MajorErrorCount**</span><span class="sxs-lookup"><span data-stu-id="be0da-157">**MajorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0da-158">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be0da-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be0da-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be0da-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be0da-160">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="be0da-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="be0da-161">Conteggio degli errori principali.</span><span class="sxs-lookup"><span data-stu-id="be0da-161">Count of the major errors.</span></span>

<span data-ttu-id="be0da-162">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="be0da-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="be0da-163">**MinorErrorCount**</span><span class="sxs-lookup"><span data-stu-id="be0da-163">**MinorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0da-164">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be0da-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be0da-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be0da-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be0da-166">Conteggio degli errori secondari.</span><span class="sxs-lookup"><span data-stu-id="be0da-166">Count of the minor errors.</span></span>

<span data-ttu-id="be0da-167">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="be0da-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="be0da-168">**Nome**</span><span class="sxs-lookup"><span data-stu-id="be0da-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0da-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="be0da-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be0da-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be0da-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be0da-171">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="be0da-171">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="be0da-172">La proprietà nome ereditato funge da parte della chiave per l'istanza **di \_ DeviceErrorCounts CIM** .</span><span class="sxs-lookup"><span data-stu-id="be0da-172">The inherited Name property serves as part of the key for the **CIM\_DeviceErrorCounts** instance.</span></span> <span data-ttu-id="be0da-173">L'ambito dell'oggetto è costituito dal dispositivo logico a cui si applicano le statistiche.</span><span class="sxs-lookup"><span data-stu-id="be0da-173">The object is scoped by the logical device to which the statistics apply.</span></span>

</dd> <dt>

<span data-ttu-id="be0da-174">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="be0da-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0da-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="be0da-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be0da-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be0da-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be0da-177">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**SystemCreationClassName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="be0da-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="be0da-178">**CreationClassName** del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="be0da-178">Scoping system's **CreationClassName**.</span></span>

</dd> <dt>

<span data-ttu-id="be0da-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="be0da-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0da-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="be0da-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="be0da-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be0da-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be0da-182">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**SystemName**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="be0da-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="be0da-183">Proprietà **Name** del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="be0da-183">Scoping system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="be0da-184">**WarningCount**</span><span class="sxs-lookup"><span data-stu-id="be0da-184">**WarningCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be0da-185">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be0da-185">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be0da-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="be0da-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be0da-187">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Stato operativo DMTF \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="be0da-187">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="be0da-188">Conteggio degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="be0da-188">Count of the warnings.</span></span>

<span data-ttu-id="be0da-189">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="be0da-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be0da-190">Commenti</span><span class="sxs-lookup"><span data-stu-id="be0da-190">Remarks</span></span>

<span data-ttu-id="be0da-191">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="be0da-191">WMI does not implement this class.</span></span>

<span data-ttu-id="be0da-192">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="be0da-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="be0da-193">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="be0da-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="be0da-194">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be0da-194">Requirements</span></span>



| <span data-ttu-id="be0da-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="be0da-195">Requirement</span></span> | <span data-ttu-id="be0da-196">Valore</span><span class="sxs-lookup"><span data-stu-id="be0da-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be0da-197">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be0da-197">Minimum supported client</span></span><br/> | <span data-ttu-id="be0da-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be0da-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be0da-199">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be0da-199">Minimum supported server</span></span><br/> | <span data-ttu-id="be0da-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be0da-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be0da-201">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="be0da-201">Namespace</span></span><br/>                | <span data-ttu-id="be0da-202">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="be0da-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="be0da-203">MOF</span><span class="sxs-lookup"><span data-stu-id="be0da-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be0da-204"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be0da-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="be0da-205">DLL</span><span class="sxs-lookup"><span data-stu-id="be0da-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be0da-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be0da-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be0da-207">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be0da-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be0da-208">**\_STATISTICALINFORMATION CIM**</span><span class="sxs-lookup"><span data-stu-id="be0da-208">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> </dl>

 

