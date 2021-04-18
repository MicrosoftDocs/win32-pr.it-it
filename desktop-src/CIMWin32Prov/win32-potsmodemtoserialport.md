---
description: La \_ classe WMI dell'associazione POTSModemToSerialPort Win32 mette in relazione un modem con la porta seriale utilizzata dal modem.
ms.assetid: 4dbde5ae-f785-4d2d-80d9-508effd72cf2
ms.tgt_platform: multiple
title: Classe Win32_POTSModemToSerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModemToSerialPort
- Win32_POTSModemToSerialPort.NegotiatedDataWidth
- Win32_POTSModemToSerialPort.NegotiatedSpeed
- Win32_POTSModemToSerialPort.AccessState
- Win32_POTSModemToSerialPort.NumberOfHardResets
- Win32_POTSModemToSerialPort.NumberOfSoftResets
- Win32_POTSModemToSerialPort.Dependent
- Win32_POTSModemToSerialPort.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a1e6128ffde7afce0132dd4415e4eca1f06b5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304871"
---
# <a name="win32_potsmodemtoserialport-class"></a><span data-ttu-id="a22d9-103">Win32 \_ POTSModemToSerialPort (classe)</span><span class="sxs-lookup"><span data-stu-id="a22d9-103">Win32\_POTSModemToSerialPort class</span></span>

<span data-ttu-id="a22d9-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ POTSModemToSerialPort Win32** mette in relazione un modem con la porta seriale utilizzata dal modem.</span><span class="sxs-lookup"><span data-stu-id="a22d9-104">The **Win32\_POTSModemToSerialPort** association [WMI class](../wmisdk/retrieving-a-class.md) relates a modem to the serial port the modem uses.</span></span>

<span data-ttu-id="a22d9-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a22d9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a22d9-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a22d9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22d9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a22d9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModemToSerialPort : CIM_ControlledBy
{
  uint32               NegotiatedDataWidth;
  uint64               NegotiatedSpeed;
  uint16               AccessState;
  uint32               NumberOfHardResets;
  uint32               NumberOfSoftResets;
  Win32_POTSModem  REF Dependent;
  Win32_SerialPort REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="a22d9-108">Members</span><span class="sxs-lookup"><span data-stu-id="a22d9-108">Members</span></span>

<span data-ttu-id="a22d9-109">La classe **Win32 \_ POTSModemToSerialPort** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a22d9-109">The **Win32\_POTSModemToSerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="a22d9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a22d9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a22d9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a22d9-111">Properties</span></span>

<span data-ttu-id="a22d9-112">La classe **Win32 \_ POTSModemToSerialPort** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a22d9-112">The **Win32\_POTSModemToSerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a22d9-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="a22d9-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d9-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a22d9-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a22d9-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a22d9-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22d9-116">Indica se il controller sta attivando o accedendo attivamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a22d9-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="a22d9-117">Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller.</span><span class="sxs-lookup"><span data-stu-id="a22d9-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="a22d9-118">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="a22d9-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a22d9-119">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a22d9-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="a22d9-120">**Attivo** (1)</span><span class="sxs-lookup"><span data-stu-id="a22d9-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="a22d9-121">**Inattivo** (2)</span><span class="sxs-lookup"><span data-stu-id="a22d9-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a22d9-122">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="a22d9-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d9-123">Tipo di dati **: \_ SerialPort Win32**</span><span class="sxs-lookup"><span data-stu-id="a22d9-123">Data type: **Win32\_SerialPort**</span></span>
</dt> <dt>

<span data-ttu-id="a22d9-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a22d9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a22d9-125">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| SerialPort Win32 di WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="a22d9-125">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPort")</span></span>
</dt> </dl>

<span data-ttu-id="a22d9-126">[**\_ SerialPort Win32**](win32-serialport.md) che rappresenta la porta seriale utilizzata dal modem.</span><span class="sxs-lookup"><span data-stu-id="a22d9-126">A [**Win32\_SerialPort**](win32-serialport.md) that represents the serial port used by the modem.</span></span>

</dd> <dt>

<span data-ttu-id="a22d9-127">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="a22d9-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d9-128">Tipo di dati: **Win32 \_ POTSModem**</span><span class="sxs-lookup"><span data-stu-id="a22d9-128">Data type: **Win32\_POTSModem**</span></span>
</dt> <dt>

<span data-ttu-id="a22d9-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a22d9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a22d9-130">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("dipendente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ POTSModem")</span><span class="sxs-lookup"><span data-stu-id="a22d9-130">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_POTSModem")</span></span>
</dt> </dl>

<span data-ttu-id="a22d9-131">Un [**\_ POTSModem Win32**](win32-potsmodem.md) che rappresenta il modem POTS utilizzando la porta seriale.</span><span class="sxs-lookup"><span data-stu-id="a22d9-131">A [**Win32\_POTSModem**](win32-potsmodem.md) that represents the POTS modem using the serial port.</span></span>

</dd> <dt>

<span data-ttu-id="a22d9-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="a22d9-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d9-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a22d9-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a22d9-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a22d9-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a22d9-135">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="a22d9-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="a22d9-136">Quando sono possibili più larghezze di dati del bus o della connessione, questa proprietà definisce quella in uso tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="a22d9-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="a22d9-137">La larghezza dei dati è specificata in bit.</span><span class="sxs-lookup"><span data-stu-id="a22d9-137">Data width is specified in bits.</span></span> <span data-ttu-id="a22d9-138">Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="a22d9-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="a22d9-139">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="a22d9-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="a22d9-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="a22d9-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d9-141">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a22d9-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a22d9-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a22d9-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a22d9-143">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="a22d9-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="a22d9-144">Quando sono possibili più velocità di connessione o bus, questa proprietà definisce quella usata tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="a22d9-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="a22d9-145">La velocità è specificata in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="a22d9-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="a22d9-146">Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="a22d9-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="a22d9-147">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="a22d9-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="a22d9-148">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="a22d9-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="a22d9-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="a22d9-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d9-150">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a22d9-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a22d9-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a22d9-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22d9-152">Numero di reimpostazioni rigide rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="a22d9-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="a22d9-153">Una reimpostazione hardware restituisce il dispositivo alla relativa inizializzazione o allo stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="a22d9-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="a22d9-154">Tutte le informazioni sullo stato del dispositivo interno e i dati vengono persi.</span><span class="sxs-lookup"><span data-stu-id="a22d9-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="a22d9-155">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="a22d9-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="a22d9-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="a22d9-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22d9-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a22d9-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a22d9-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a22d9-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22d9-159">Numero di reimpostazioni software rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="a22d9-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="a22d9-160">Un ripristino soft non cancella completamente i dati e lo stato corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a22d9-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="a22d9-161">La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.</span><span class="sxs-lookup"><span data-stu-id="a22d9-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="a22d9-162">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="a22d9-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a22d9-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="a22d9-163">Remarks</span></span>

<span data-ttu-id="a22d9-164">La classe **Win32 \_ POTSModemToSerialPort** è derivata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="a22d9-164">The **Win32\_POTSModemToSerialPort** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a22d9-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a22d9-165">Requirements</span></span>



| <span data-ttu-id="a22d9-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="a22d9-166">Requirement</span></span> | <span data-ttu-id="a22d9-167">Valore</span><span class="sxs-lookup"><span data-stu-id="a22d9-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a22d9-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a22d9-168">Minimum supported client</span></span><br/> | <span data-ttu-id="a22d9-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a22d9-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a22d9-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a22d9-170">Minimum supported server</span></span><br/> | <span data-ttu-id="a22d9-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a22d9-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a22d9-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a22d9-172">Namespace</span></span><br/>                | <span data-ttu-id="a22d9-173">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a22d9-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a22d9-174">MOF</span><span class="sxs-lookup"><span data-stu-id="a22d9-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a22d9-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a22d9-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a22d9-176">DLL</span><span class="sxs-lookup"><span data-stu-id="a22d9-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a22d9-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a22d9-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a22d9-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a22d9-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a22d9-179">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="a22d9-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="a22d9-180">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="a22d9-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
