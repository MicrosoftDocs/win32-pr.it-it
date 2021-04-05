---
description: La \_ classe CIM ProcessExecutable rappresenta un collegamento tra un processo e un file di dati e indica che il file partecipa all'esecuzione del processo.
ms.assetid: 6db69bf3-b28e-4d0b-8878-558e12052767
ms.tgt_platform: multiple
title: Classe CIM_ProcessExecutable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessExecutable
- CIM_ProcessExecutable.Dependent
- CIM_ProcessExecutable.Antecedent
- CIM_ProcessExecutable.BaseAddress
- CIM_ProcessExecutable.GlobalProcessCount
- CIM_ProcessExecutable.ModuleInstance
- CIM_ProcessExecutable.ProcessCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aedb1e79ad842e4cb04746ff47bfab142a536f43
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049280"
---
# <a name="cim_processexecutable-class"></a><span data-ttu-id="92630-103">CIM \_ ProcessExecutable (classe)</span><span class="sxs-lookup"><span data-stu-id="92630-103">CIM\_ProcessExecutable class</span></span>

<span data-ttu-id="92630-104">La classe **CIM \_ ProcessExecutable** rappresenta un collegamento tra un processo e un file di dati e indica che il file partecipa all'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="92630-104">The **CIM\_ProcessExecutable** class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92630-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="92630-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="92630-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="92630-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="92630-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="92630-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="92630-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="92630-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="92630-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92630-109">Syntax</span></span>

``` syntax
[Privileges("SeDebugPrivilege"), Dynamic, Provider("CIMWin32"), UUID("{8502C542-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ProcessExecutable : CIM_Dependency
{
  CIM_Process  REF Dependent;
  CIM_DataFile REF Antecedent;
  uint64           BaseAddress;
  uint32           GlobalProcessCount;
  uint32           ModuleInstance;
  uint32           ProcessCount;
};
```

## <a name="members"></a><span data-ttu-id="92630-110">Members</span><span class="sxs-lookup"><span data-stu-id="92630-110">Members</span></span>

<span data-ttu-id="92630-111">La classe **CIM \_ ProcessExecutable** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="92630-111">The **CIM\_ProcessExecutable** class has these types of members:</span></span>

-   [<span data-ttu-id="92630-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="92630-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92630-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="92630-113">Properties</span></span>

<span data-ttu-id="92630-114">La classe **CIM \_ ProcessExecutable** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="92630-114">The **CIM\_ProcessExecutable** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92630-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="92630-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92630-116">Tipo di dati **: \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="92630-116">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="92630-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="92630-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92630-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (precedente), [**chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="92630-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="92630-119">Un [**\_ DataFile CIM**](cim-datafile.md) che descrive il file di dati che partecipa all'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="92630-119">A [**CIM\_DataFile**](cim-datafile.md) that describes the data file participating in the execution of the process.</span></span>

</dd> <dt>

<span data-ttu-id="92630-120">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="92630-120">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92630-121">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92630-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92630-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="92630-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92630-123">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="92630-123">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="92630-124">Indirizzo di base del modulo nello spazio degli indirizzi del processo associato.</span><span class="sxs-lookup"><span data-stu-id="92630-124">Base address of the module in the address space of the associated process.</span></span>

<span data-ttu-id="92630-125">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="92630-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="92630-126">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="92630-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92630-127">Tipo di dati **: \_ processo CIM**</span><span class="sxs-lookup"><span data-stu-id="92630-127">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="92630-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="92630-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92630-129">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (dipendente), [**chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="92630-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="92630-130">Un [**\_ processo CIM**](cim-process.md) che descrive il processo.</span><span class="sxs-lookup"><span data-stu-id="92630-130">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="92630-131">**GlobalProcessCount**</span><span class="sxs-lookup"><span data-stu-id="92630-131">**GlobalProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92630-132">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92630-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92630-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="92630-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92630-134">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="92630-134">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="92630-135">Numero corrente di processi in cui il file è stato caricato in memoria.</span><span class="sxs-lookup"><span data-stu-id="92630-135">Current number of processes that have the file loaded in memory.</span></span>

</dd> <dt>

<span data-ttu-id="92630-136">**ModuleInstance**</span><span class="sxs-lookup"><span data-stu-id="92630-136">**ModuleInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92630-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92630-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92630-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="92630-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92630-139">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="92630-139">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="92630-140">Handle di istanza Win32.</span><span class="sxs-lookup"><span data-stu-id="92630-140">Win32 instance handle.</span></span> <span data-ttu-id="92630-141">Questa proprietà è obsoleta e non è presente alcun valore di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="92630-141">This property is obsolete, and there is no replacement value.</span></span>

</dd> <dt>

<span data-ttu-id="92630-142">**ProcessCount**</span><span class="sxs-lookup"><span data-stu-id="92630-142">**ProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92630-143">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92630-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92630-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="92630-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92630-145">Qualificatori: [**schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="92630-145">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="92630-146">Conteggio dei riferimenti del file nel processo associato.</span><span class="sxs-lookup"><span data-stu-id="92630-146">Reference count of the file in the associated process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92630-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="92630-147">Remarks</span></span>

<span data-ttu-id="92630-148">La classe **CIM \_ ProcessExecutable** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="92630-148">The **CIM\_ProcessExecutable** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="92630-149">WMI implementa la classe **CIM \_ ProcessExecutable** .</span><span class="sxs-lookup"><span data-stu-id="92630-149">WMI implements the **CIM\_ProcessExecutable** class.</span></span> <span data-ttu-id="92630-150">La classe **CIM \_ ProcessExecutable** è una classe dinamica.</span><span class="sxs-lookup"><span data-stu-id="92630-150">The **CIM\_ProcessExecutable** class is a dynamic class.</span></span>

<span data-ttu-id="92630-151">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="92630-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="92630-152">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="92630-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="92630-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92630-153">Requirements</span></span>



| <span data-ttu-id="92630-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="92630-154">Requirement</span></span> | <span data-ttu-id="92630-155">Valore</span><span class="sxs-lookup"><span data-stu-id="92630-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92630-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92630-156">Minimum supported client</span></span><br/> | <span data-ttu-id="92630-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92630-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92630-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92630-158">Minimum supported server</span></span><br/> | <span data-ttu-id="92630-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92630-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92630-160">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="92630-160">Namespace</span></span><br/>                | <span data-ttu-id="92630-161">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="92630-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="92630-162">MOF</span><span class="sxs-lookup"><span data-stu-id="92630-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92630-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92630-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="92630-164">DLL</span><span class="sxs-lookup"><span data-stu-id="92630-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92630-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92630-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92630-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92630-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92630-167">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="92630-167">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

