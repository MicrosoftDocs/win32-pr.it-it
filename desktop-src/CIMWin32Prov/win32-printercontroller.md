---
description: La \_ classe WMI dell'associazione PrinterController Win32 mette in relazione una stampante e il dispositivo locale a cui è connessa la stampante. Si noti che questa classe restituisce solo le istanze per le stampanti locali.
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Classe Win32_PrinterController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee38b827aed2dfffe1e7ef4f5049b16eee50791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877822"
---
# <a name="win32_printercontroller-class"></a><span data-ttu-id="15894-104">Win32 \_ PrinterController (classe)</span><span class="sxs-lookup"><span data-stu-id="15894-104">Win32\_PrinterController class</span></span>

<span data-ttu-id="15894-105">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PrinterController Win32** mette in relazione una stampante e il dispositivo locale a cui è connessa la stampante.</span><span class="sxs-lookup"><span data-stu-id="15894-105">The **Win32\_PrinterController** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and the local device to which the printer is connected.</span></span> <span data-ttu-id="15894-106">Si noti che questa classe restituisce solo le istanze per le stampanti locali.</span><span class="sxs-lookup"><span data-stu-id="15894-106">Note that this class only returns instances for local printers.</span></span>

<span data-ttu-id="15894-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="15894-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="15894-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="15894-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="15894-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15894-109">Syntax</span></span>

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="15894-110">Members</span><span class="sxs-lookup"><span data-stu-id="15894-110">Members</span></span>

<span data-ttu-id="15894-111">La classe **Win32 \_ PrinterController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="15894-111">The **Win32\_PrinterController** class has these types of members:</span></span>

-   [<span data-ttu-id="15894-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15894-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15894-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15894-113">Properties</span></span>

<span data-ttu-id="15894-114">La classe **Win32 \_ PrinterController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="15894-114">The **Win32\_PrinterController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15894-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="15894-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15894-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15894-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15894-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15894-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15894-118">Stato dell'accesso del controller al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15894-118">State of the controller access to the device.</span></span> <span data-ttu-id="15894-119">Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller.</span><span class="sxs-lookup"><span data-stu-id="15894-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="15894-120">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="15894-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="15894-121"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="15894-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="15894-122">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="15894-122">Unknown</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="15894-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="15894-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="15894-124">Attivo</span><span class="sxs-lookup"><span data-stu-id="15894-124">Active</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="15894-125"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="15894-125"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="15894-126">Inattivo</span><span class="sxs-lookup"><span data-stu-id="15894-126">Inactive</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="15894-127">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="15894-127">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15894-128">Tipo di dati **: \_ controller CIM**</span><span class="sxs-lookup"><span data-stu-id="15894-128">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="15894-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15894-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15894-130">Qualificatori: [ **chiave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="15894-130">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="15894-131">Riferimento all'istanza [**del \_ controller CIM**](cim-controller.md) che rappresenta il dispositivo locale associato a questa stampante.</span><span class="sxs-lookup"><span data-stu-id="15894-131">Reference to the [**CIM\_Controller**](cim-controller.md) instance representing the local device associated with this printer.</span></span>

<span data-ttu-id="15894-132">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="15894-132">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="15894-133">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="15894-133">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15894-134">Tipo di dati **: \_ stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="15894-134">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="15894-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15894-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15894-136">Qualificatori: [ **chiave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="15894-136">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="15894-137">Riferimento all'istanza [**della \_ stampante Win32**](win32-printer.md) che rappresenta la stampante associata alla periferica locale.</span><span class="sxs-lookup"><span data-stu-id="15894-137">Reference to the [**Win32\_Printer**](win32-printer.md) instance representing the printer associated with the local device.</span></span>

<span data-ttu-id="15894-138">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="15894-138">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="15894-139">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="15894-139">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15894-140">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15894-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15894-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15894-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15894-142">Larghezza dei dati in uso tra dispositivi (se sono possibili più larghezze di dati del bus o della connessione).</span><span class="sxs-lookup"><span data-stu-id="15894-142">Data width in use between devices (when several bus or connection data widths are possible).</span></span> <span data-ttu-id="15894-143">La larghezza dei dati è specificata in bit.</span><span class="sxs-lookup"><span data-stu-id="15894-143">Data width is specified in bits.</span></span> <span data-ttu-id="15894-144">Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="15894-144">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="15894-145">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="15894-145">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="15894-146">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="15894-146">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15894-147">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="15894-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="15894-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15894-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15894-149">Velocità di utilizzo tra i dispositivi (quando sono possibili più velocità del bus o di connessione).</span><span class="sxs-lookup"><span data-stu-id="15894-149">Speed in use between devices (when several bus or connection speeds are possible).</span></span> <span data-ttu-id="15894-150">La velocità è specificata in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="15894-150">Speed is specified in bits per second.</span></span> <span data-ttu-id="15894-151">Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="15894-151">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="15894-152">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="15894-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="15894-153">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="15894-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="15894-154">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="15894-154">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15894-155">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15894-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15894-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15894-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15894-157">Numero di reimpostazioni rigide rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="15894-157">Number of hard resets issued by the controller.</span></span>

<span data-ttu-id="15894-158">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="15894-158">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="15894-159">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="15894-159">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15894-160">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15894-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15894-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="15894-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15894-162">Numero di reimpostazioni software rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="15894-162">Number of soft resets issued by the controller.</span></span>

<span data-ttu-id="15894-163">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="15894-163">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15894-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="15894-164">Remarks</span></span>

<span data-ttu-id="15894-165">La classe **Win32 \_ PrinterController** è derivata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="15894-165">The **Win32\_PrinterController** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15894-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15894-166">Requirements</span></span>



| <span data-ttu-id="15894-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="15894-167">Requirement</span></span> | <span data-ttu-id="15894-168">Valore</span><span class="sxs-lookup"><span data-stu-id="15894-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="15894-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15894-169">Minimum supported client</span></span><br/> | <span data-ttu-id="15894-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15894-170">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="15894-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15894-171">Minimum supported server</span></span><br/> | <span data-ttu-id="15894-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15894-172">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="15894-173">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="15894-173">Namespace</span></span><br/>                | <span data-ttu-id="15894-174">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="15894-174">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="15894-175">MOF</span><span class="sxs-lookup"><span data-stu-id="15894-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15894-176"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15894-176"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="15894-177">DLL</span><span class="sxs-lookup"><span data-stu-id="15894-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15894-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15894-178"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="15894-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15894-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15894-180">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="15894-180">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="15894-181">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="15894-181">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
