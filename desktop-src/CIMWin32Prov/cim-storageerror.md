---
description: La \_ classe CIM StorageError rappresenta i blocchi di supporti o di spazio di memoria di cui è stato eseguito il mapping fuori uso a causa di errori. La chiave della classe è la proprietà IndirizzoIniziale dei byte in errore.
ms.assetid: e786aa39-4718-416b-b659-bf4b8d3e2851
ms.tgt_platform: multiple
title: Classe CIM_StorageError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageError
- CIM_StorageError.DeviceCreationClassName
- CIM_StorageError.DeviceID
- CIM_StorageError.EndingAddress
- CIM_StorageError.StartingAddress
- CIM_StorageError.SystemCreationClassName
- CIM_StorageError.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f5b197a5c82e61e054f5875fad466cac808ec38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304581"
---
# <a name="cim_storageerror-class"></a><span data-ttu-id="dc874-104">CIM \_ StorageError (classe)</span><span class="sxs-lookup"><span data-stu-id="dc874-104">CIM\_StorageError class</span></span>

<span data-ttu-id="dc874-105">La classe **CIM \_ StorageError** rappresenta i blocchi di supporti o di spazio di memoria di cui è stato eseguito il mapping fuori uso a causa di errori.</span><span class="sxs-lookup"><span data-stu-id="dc874-105">The **CIM\_StorageError** class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="dc874-106">La chiave della classe è la proprietà **IndirizzoIniziale** dei byte in errore.</span><span class="sxs-lookup"><span data-stu-id="dc874-106">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dc874-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="dc874-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dc874-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dc874-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dc874-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="dc874-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dc874-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="dc874-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc874-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc874-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{71312AB6-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_StorageError
{
  string DeviceCreationClassName;
  string DeviceID;
  uint64 EndingAddress;
  uint64 StartingAddress;
  string SystemCreationClassName;
  string SystemName;
};
```

## <a name="members"></a><span data-ttu-id="dc874-112">Members</span><span class="sxs-lookup"><span data-stu-id="dc874-112">Members</span></span>

<span data-ttu-id="dc874-113">La classe **CIM \_ StorageError** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dc874-113">The **CIM\_StorageError** class has these types of members:</span></span>

-   [<span data-ttu-id="dc874-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dc874-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc874-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dc874-115">Properties</span></span>

<span data-ttu-id="dc874-116">La classe **CIM \_ StorageError** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dc874-116">The **CIM\_StorageError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc874-117">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dc874-117">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc874-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc874-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc874-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc874-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc874-120">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="dc874-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="dc874-121">Nome della classe di creazione dell'ambito di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dc874-121">Scoping storage extent's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="dc874-122">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="dc874-122">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc874-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc874-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc874-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc874-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc874-125">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**DeviceID**")</span><span class="sxs-lookup"><span data-stu-id="dc874-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**DeviceID**")</span></span>
</dt> </dl>

<span data-ttu-id="dc874-126">Identificatore del dispositivo dell'ambito di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dc874-126">Scoping storage extent's device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="dc874-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="dc874-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc874-128">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc874-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc874-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc874-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc874-130">Indirizzo finale dei byte in errore.</span><span class="sxs-lookup"><span data-stu-id="dc874-130">Ending address of the bytes in error.</span></span>

<span data-ttu-id="dc874-131">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dc874-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dc874-132">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="dc874-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc874-133">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc874-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc874-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc874-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc874-135">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dc874-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dc874-136">Indirizzo iniziale dei byte in errore.</span><span class="sxs-lookup"><span data-stu-id="dc874-136">Starting address of the bytes in error.</span></span>

<span data-ttu-id="dc874-137">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dc874-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dc874-138">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dc874-138">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc874-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc874-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc874-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc874-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc874-141">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**SystemCreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="dc874-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemCreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="dc874-142">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="dc874-142">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="dc874-143">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dc874-143">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc874-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc874-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc874-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc874-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc874-146">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**SystemName**")</span><span class="sxs-lookup"><span data-stu-id="dc874-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemName**")</span></span>
</dt> </dl>

<span data-ttu-id="dc874-147">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="dc874-147">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc874-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc874-148">Remarks</span></span>

<span data-ttu-id="dc874-149">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="dc874-149">WMI does not implement this class.</span></span>

<span data-ttu-id="dc874-150">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="dc874-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dc874-151">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="dc874-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc874-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc874-152">Requirements</span></span>



| <span data-ttu-id="dc874-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc874-153">Requirement</span></span> | <span data-ttu-id="dc874-154">Valore</span><span class="sxs-lookup"><span data-stu-id="dc874-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc874-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc874-155">Minimum supported client</span></span><br/> | <span data-ttu-id="dc874-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc874-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc874-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc874-157">Minimum supported server</span></span><br/> | <span data-ttu-id="dc874-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc874-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc874-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dc874-159">Namespace</span></span><br/>                | <span data-ttu-id="dc874-160">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="dc874-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dc874-161">MOF</span><span class="sxs-lookup"><span data-stu-id="dc874-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc874-162"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc874-162"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc874-163">DLL</span><span class="sxs-lookup"><span data-stu-id="dc874-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc874-164"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc874-164"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

