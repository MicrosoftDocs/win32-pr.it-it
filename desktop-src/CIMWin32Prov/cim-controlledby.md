---
description: La \_ relazione CIM ControlledBy indica i dispositivi a cui viene eseguito il comando o a cui si accede tramite il dispositivo logico del controller.
ms.assetid: 6aa4e088-32a0-4c88-bb82-341b6ab53b4c
ms.tgt_platform: multiple
title: Classe CIM_ControlledBy (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.NegotiatedDataWidth
- CIM_ControlledBy.NegotiatedSpeed
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 315eea9fa207a92c3aa1add6fe021127dc3949d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877677"
---
# <a name="cim_controlledby-class-cimwin32-wmi-providers"></a><span data-ttu-id="72020-103">Classe CIM_ControlledBy (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="72020-103">CIM_ControlledBy class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="72020-104">La relazione **CIM \_ ControlledBy** indica i dispositivi a cui viene eseguito il comando o a cui si accede tramite il dispositivo logico del controller.</span><span class="sxs-lookup"><span data-stu-id="72020-104">The **CIM\_ControlledBy** relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72020-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="72020-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="72020-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="72020-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="72020-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="72020-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="72020-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="72020-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="72020-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72020-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  CIM_LogicalDevice REF Dependent;
  CIM_Controller    REF Antecedent;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="72020-110">Members</span><span class="sxs-lookup"><span data-stu-id="72020-110">Members</span></span>

<span data-ttu-id="72020-111">La classe **CIM \_ ControlledBy** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="72020-111">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="72020-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72020-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72020-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72020-113">Properties</span></span>

<span data-ttu-id="72020-114">La classe **CIM \_ ControlledBy** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="72020-114">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72020-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="72020-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72020-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72020-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72020-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72020-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72020-118">Indica se il controller sta attivando o accedendo attivamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72020-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="72020-119">Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller.</span><span class="sxs-lookup"><span data-stu-id="72020-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="72020-120">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="72020-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="72020-121">**Attivo** (1)</span><span class="sxs-lookup"><span data-stu-id="72020-121">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="72020-122">**Inattivo** (2)</span><span class="sxs-lookup"><span data-stu-id="72020-122">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="72020-123">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="72020-123">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72020-124">Tipo di dati **: \_ controller CIM**</span><span class="sxs-lookup"><span data-stu-id="72020-124">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="72020-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72020-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72020-126">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="72020-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="72020-127">[**\_ Controller CIM**](cim-controller.md) che rappresenta il controller.</span><span class="sxs-lookup"><span data-stu-id="72020-127">A [**CIM\_Controller**](cim-controller.md) that represents the controller.</span></span>

</dd> <dt>

<span data-ttu-id="72020-128">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="72020-128">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72020-129">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="72020-129">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="72020-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72020-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72020-131">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="72020-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="72020-132">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che rappresenta il dispositivo controllato.</span><span class="sxs-lookup"><span data-stu-id="72020-132">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the controlled device.</span></span>

</dd> <dt>

<span data-ttu-id="72020-133">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="72020-133">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72020-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72020-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72020-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72020-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72020-136">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="72020-136">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="72020-137">Quando sono possibili più larghezze di dati del bus o della connessione, questa proprietà definisce quella in uso tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="72020-137">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="72020-138">La larghezza dei dati è specificata in bit.</span><span class="sxs-lookup"><span data-stu-id="72020-138">Data width is specified in bits.</span></span> <span data-ttu-id="72020-139">Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="72020-139">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="72020-140">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="72020-140">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="72020-141">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="72020-141">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72020-142">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="72020-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="72020-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72020-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72020-144">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="72020-144">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="72020-145">Quando sono possibili più velocità di connessione o bus, questa proprietà definisce quella usata tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="72020-145">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="72020-146">La velocità è specificata in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="72020-146">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="72020-147">Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="72020-147">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="72020-148">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="72020-148">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="72020-149">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="72020-149">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="72020-150">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="72020-150">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72020-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72020-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72020-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72020-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72020-153">Numero di reimpostazioni rigide rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="72020-153">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="72020-154">Una reimpostazione hardware restituisce il dispositivo alla relativa inizializzazione o allo stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="72020-154">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="72020-155">Tutte le informazioni sullo stato del dispositivo interno e i dati vengono persi.</span><span class="sxs-lookup"><span data-stu-id="72020-155">All internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="72020-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="72020-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72020-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72020-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72020-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72020-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72020-159">Numero di reimpostazioni software rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="72020-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="72020-160">Un ripristino soft non cancella completamente i dati e lo stato corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72020-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="72020-161">La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.</span><span class="sxs-lookup"><span data-stu-id="72020-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72020-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="72020-162">Remarks</span></span>

<span data-ttu-id="72020-163">La classe **CIM \_ ControlledBy** è derivata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="72020-163">The **CIM\_ControlledBy** class is derived from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="72020-164">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="72020-164">WMI does not implement this class.</span></span> <span data-ttu-id="72020-165">Per ulteriori informazioni sulle classi derivate da **CIM \_ ControlledBy**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="72020-165">For more information about classes derived from **CIM\_ControlledBy**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="72020-166">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="72020-166">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="72020-167">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="72020-167">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="72020-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72020-168">Requirements</span></span>



| <span data-ttu-id="72020-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="72020-169">Requirement</span></span> | <span data-ttu-id="72020-170">Valore</span><span class="sxs-lookup"><span data-stu-id="72020-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72020-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72020-171">Minimum supported client</span></span><br/> | <span data-ttu-id="72020-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72020-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72020-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72020-173">Minimum supported server</span></span><br/> | <span data-ttu-id="72020-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72020-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72020-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="72020-175">Namespace</span></span><br/>                | <span data-ttu-id="72020-176">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="72020-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72020-177">MOF</span><span class="sxs-lookup"><span data-stu-id="72020-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72020-178"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72020-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72020-179">DLL</span><span class="sxs-lookup"><span data-stu-id="72020-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72020-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72020-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72020-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72020-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72020-182">**\_DEVICECONNECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="72020-182">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

