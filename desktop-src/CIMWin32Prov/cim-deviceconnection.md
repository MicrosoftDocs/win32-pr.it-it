---
description: La \_ classe di associazione CIM DeviceConnection rappresenta due o più dispositivi connessi.
ms.assetid: 82095cd6-1843-4db2-9fe8-3e225611bd3b
ms.tgt_platform: multiple
title: Classe CIM_DeviceConnection (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.NegotiatedDataWidth
- CIM_DeviceConnection.NegotiatedSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8179287686439ea31c19d700a785de7fff47659
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225688"
---
# <a name="cim_deviceconnection-class-cimwin32-wmi-providers"></a><span data-ttu-id="d9d74-103">Classe CIM_DeviceConnection (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="d9d74-103">CIM_DeviceConnection class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="d9d74-104">La classe di associazione **CIM \_ DeviceConnection** rappresenta due o più dispositivi connessi.</span><span class="sxs-lookup"><span data-stu-id="d9d74-104">The **CIM\_DeviceConnection** association class represents two or more connected devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9d74-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="d9d74-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d9d74-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d9d74-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d9d74-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d9d74-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d9d74-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d9d74-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d74-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9d74-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
};
```

## <a name="members"></a><span data-ttu-id="d9d74-110">Members</span><span class="sxs-lookup"><span data-stu-id="d9d74-110">Members</span></span>

<span data-ttu-id="d9d74-111">La classe **CIM \_ DeviceConnection** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d9d74-111">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="d9d74-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d9d74-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9d74-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d9d74-113">Properties</span></span>

<span data-ttu-id="d9d74-114">La classe **CIM \_ DeviceConnection** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d9d74-114">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9d74-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="d9d74-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9d74-116">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="d9d74-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="d9d74-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d9d74-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9d74-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="d9d74-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d9d74-119">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d9d74-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a logical device.</span></span>

</dd> <dt>

<span data-ttu-id="d9d74-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="d9d74-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9d74-121">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="d9d74-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="d9d74-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d9d74-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9d74-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="d9d74-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d9d74-124">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive un secondo dispositivo logico connesso al dispositivo precedente.</span><span class="sxs-lookup"><span data-stu-id="d9d74-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a second logical device connected to the Antecedent device.</span></span>

</dd> <dt>

<span data-ttu-id="d9d74-125">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="d9d74-125">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9d74-126">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9d74-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9d74-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d9d74-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9d74-128">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="d9d74-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="d9d74-129">Quando sono possibili più larghezze di dati del bus o della connessione, questa proprietà definisce quella in uso tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="d9d74-129">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="d9d74-130">La larghezza dei dati è specificata in bit.</span><span class="sxs-lookup"><span data-stu-id="d9d74-130">Data width is specified in bits.</span></span> <span data-ttu-id="d9d74-131">Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="d9d74-131">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="d9d74-132">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="d9d74-132">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9d74-133">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d9d74-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d9d74-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d9d74-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9d74-135">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="d9d74-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="d9d74-136">Quando sono possibili più velocità di connessione o bus, questa proprietà definisce quella usata tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="d9d74-136">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="d9d74-137">La velocità è specificata in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="d9d74-137">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="d9d74-138">Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="d9d74-138">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="d9d74-139">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d9d74-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9d74-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9d74-140">Remarks</span></span>

<span data-ttu-id="d9d74-141">La classe **CIM \_ DeviceConnection** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d9d74-141">The **CIM\_DeviceConnection** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="d9d74-142">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="d9d74-142">WMI does not implement this class.</span></span> <span data-ttu-id="d9d74-143">Per ulteriori informazioni sulle classi derivate da **CIM \_ DeviceConnection**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d9d74-143">For more information about classes derived from **CIM\_DeviceConnection**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d9d74-144">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="d9d74-144">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d9d74-145">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="d9d74-145">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9d74-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9d74-146">Requirements</span></span>



| <span data-ttu-id="d9d74-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9d74-147">Requirement</span></span> | <span data-ttu-id="d9d74-148">Valore</span><span class="sxs-lookup"><span data-stu-id="d9d74-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d74-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9d74-149">Minimum supported client</span></span><br/> | <span data-ttu-id="d9d74-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9d74-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9d74-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9d74-151">Minimum supported server</span></span><br/> | <span data-ttu-id="d9d74-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9d74-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9d74-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d9d74-153">Namespace</span></span><br/>                | <span data-ttu-id="d9d74-154">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d9d74-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d9d74-155">MOF</span><span class="sxs-lookup"><span data-stu-id="d9d74-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9d74-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9d74-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9d74-157">DLL</span><span class="sxs-lookup"><span data-stu-id="d9d74-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9d74-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9d74-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9d74-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9d74-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9d74-160">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="d9d74-160">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

