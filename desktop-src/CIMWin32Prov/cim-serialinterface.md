---
description: La \_ classe CIM SerialInterface rappresenta una \_ relazione CIM ControlledBy che indica i dispositivi a cui si accede tramite il controller seriale e le caratteristiche dell'accesso.
ms.assetid: bebc304a-c2b7-41c7-b24a-8f450ee3c4bb
ms.tgt_platform: multiple
title: Classe CIM_SerialInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialInterface
- CIM_SerialInterface.NegotiatedDataWidth
- CIM_SerialInterface.NegotiatedSpeed
- CIM_SerialInterface.AccessState
- CIM_SerialInterface.NumberOfHardResets
- CIM_SerialInterface.NumberOfSoftResets
- CIM_SerialInterface.Dependent
- CIM_SerialInterface.Antecedent
- CIM_SerialInterface.FlowControlInfo
- CIM_SerialInterface.NumberOfStopBits
- CIM_SerialInterface.ParityInfo
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1df787ff64798f412035a72e6db6d7b01b4b9b0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877669"
---
# <a name="cim_serialinterface-class"></a><span data-ttu-id="5e35c-103">CIM \_ SerialInterface (classe)</span><span class="sxs-lookup"><span data-stu-id="5e35c-103">CIM\_SerialInterface class</span></span>

<span data-ttu-id="5e35c-104">La classe **CIM \_ SerialInterface** rappresenta una relazione [**CIM \_ ControlledBy**](cim-controlledby.md) che indica i dispositivi a cui si accede tramite il controller seriale e le caratteristiche dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="5e35c-104">The **CIM\_SerialInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e35c-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="5e35c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5e35c-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5e35c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5e35c-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5e35c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5e35c-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5e35c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e35c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e35c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8B309BDA-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SerialInterface : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  CIM_LogicalDevice    REF Dependent;
  CIM_SerialController REF Antecedent;
  uint16                   FlowControlInfo;
  uint16                   NumberOfStopBits;
  uint16                   ParityInfo;
};
```

## <a name="members"></a><span data-ttu-id="5e35c-110">Members</span><span class="sxs-lookup"><span data-stu-id="5e35c-110">Members</span></span>

<span data-ttu-id="5e35c-111">La classe **CIM \_ SerialInterface** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5e35c-111">The **CIM\_SerialInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="5e35c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5e35c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e35c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5e35c-113">Properties</span></span>

<span data-ttu-id="5e35c-114">La classe **CIM \_ SerialInterface** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5e35c-114">The **CIM\_SerialInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e35c-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="5e35c-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e35c-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e35c-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e35c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e35c-118">Indica se il controller sta attivando o accedendo attivamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e35c-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="5e35c-119">Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller.</span><span class="sxs-lookup"><span data-stu-id="5e35c-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="5e35c-120">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="5e35c-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e35c-121">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5e35c-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="5e35c-122">**Attivo** (1)</span><span class="sxs-lookup"><span data-stu-id="5e35c-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="5e35c-123">**Inattivo** (2)</span><span class="sxs-lookup"><span data-stu-id="5e35c-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5e35c-124">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5e35c-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e35c-125">Tipo di dati: **CIM \_ controller seriale**</span><span class="sxs-lookup"><span data-stu-id="5e35c-125">Data type: **CIM\_SerialController**</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e35c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-127">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="5e35c-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5e35c-128">Un [**\_ controller seriale CIM**](cim-serialcontroller.md) che descrive il controller seriale.</span><span class="sxs-lookup"><span data-stu-id="5e35c-128">A [**CIM\_SerialController**](cim-serialcontroller.md) that describes the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="5e35c-129">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="5e35c-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e35c-130">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="5e35c-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e35c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-132">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="5e35c-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5e35c-133">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5e35c-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="5e35c-134">**FlowControlInfo**</span><span class="sxs-lookup"><span data-stu-id="5e35c-134">**FlowControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e35c-135">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e35c-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e35c-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e35c-137">Indica il controllo di flusso per i dati trasmessi.</span><span class="sxs-lookup"><span data-stu-id="5e35c-137">Indicates the flow control for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e35c-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5e35c-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5e35c-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="5e35c-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="5e35c-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (2)</span><span class="sxs-lookup"><span data-stu-id="5e35c-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>

<span data-ttu-id="5e35c-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XOnXOff** (3)</span><span class="sxs-lookup"><span data-stu-id="5e35c-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XonXoff** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="RTS_CTS"></span><span id="rts_cts"></span>

<span data-ttu-id="5e35c-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span><span class="sxs-lookup"><span data-stu-id="5e35c-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>

<span data-ttu-id="5e35c-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**XOnXOff e RTS/CTS** (5)</span><span class="sxs-lookup"><span data-stu-id="5e35c-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**Both XonXoff and RTS/CTS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5e35c-144">XonXoff e RTS/CTS</span><span class="sxs-lookup"><span data-stu-id="5e35c-144">XonXoff and RTS/CTS</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5e35c-145">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="5e35c-145">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e35c-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e35c-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e35c-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-148">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="5e35c-148">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="5e35c-149">Quando sono possibili più larghezze di dati del bus o della connessione, questa proprietà definisce quella in uso tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="5e35c-149">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="5e35c-150">La larghezza dei dati è specificata in bit.</span><span class="sxs-lookup"><span data-stu-id="5e35c-150">Data width is specified in bits.</span></span> <span data-ttu-id="5e35c-151">Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="5e35c-151">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="5e35c-152">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="5e35c-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e35c-153">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="5e35c-153">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e35c-154">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5e35c-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e35c-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-156">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="5e35c-156">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="5e35c-157">Quando sono possibili più velocità di connessione o bus, questa proprietà definisce quella usata tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="5e35c-157">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="5e35c-158">La velocità è specificata in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="5e35c-158">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="5e35c-159">Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="5e35c-159">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="5e35c-160">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5e35c-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="5e35c-161">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="5e35c-161">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e35c-162">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="5e35c-162">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e35c-163">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e35c-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e35c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e35c-165">Numero di reimpostazioni rigide rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="5e35c-165">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="5e35c-166">Una reimpostazione hardware restituisce il dispositivo alla relativa inizializzazione o allo stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="5e35c-166">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="5e35c-167">Tutte le informazioni sullo stato del dispositivo interno e i dati vengono persi.</span><span class="sxs-lookup"><span data-stu-id="5e35c-167">All internal device state information and data are lost.</span></span>

<span data-ttu-id="5e35c-168">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="5e35c-168">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e35c-169">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="5e35c-169">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e35c-170">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e35c-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e35c-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e35c-172">Numero di reimpostazioni software rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="5e35c-172">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="5e35c-173">Un ripristino soft non cancella completamente i dati e lo stato corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e35c-173">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="5e35c-174">La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.</span><span class="sxs-lookup"><span data-stu-id="5e35c-174">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="5e35c-175">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="5e35c-175">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e35c-176">**NumberOfStopBits**</span><span class="sxs-lookup"><span data-stu-id="5e35c-176">**NumberOfStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e35c-177">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e35c-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e35c-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-179">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="5e35c-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="5e35c-180">Numero di bit di interruzione da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="5e35c-180">Number of stop bits to transmit.</span></span>

</dd> <dt>

<span data-ttu-id="5e35c-181">**ParityInfo**</span><span class="sxs-lookup"><span data-stu-id="5e35c-181">**ParityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e35c-182">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e35c-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e35c-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e35c-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e35c-184">Informazioni sull'impostazione di parità per i dati trasmessi.</span><span class="sxs-lookup"><span data-stu-id="5e35c-184">Information about the parity setting for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e35c-185">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5e35c-185">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="5e35c-186">**Nessuno** (1)</span><span class="sxs-lookup"><span data-stu-id="5e35c-186">**None** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="5e35c-187">**Even** (2)</span><span class="sxs-lookup"><span data-stu-id="5e35c-187">**Even** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="5e35c-188">**Dispari** (3)</span><span class="sxs-lookup"><span data-stu-id="5e35c-188">**Odd** (3)</span></span>


<span data-ttu-id="5e35c-189"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5e35c-189"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5e35c-190">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e35c-190">Remarks</span></span>

<span data-ttu-id="5e35c-191">La classe **CIM \_ SerialInterface** è derivata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="5e35c-191">The **CIM\_SerialInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="5e35c-192">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="5e35c-192">WMI does not implement this class.</span></span>

<span data-ttu-id="5e35c-193">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="5e35c-193">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5e35c-194">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="5e35c-194">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e35c-195">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e35c-195">Requirements</span></span>



| <span data-ttu-id="5e35c-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e35c-196">Requirement</span></span> | <span data-ttu-id="5e35c-197">Valore</span><span class="sxs-lookup"><span data-stu-id="5e35c-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e35c-198">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e35c-198">Minimum supported client</span></span><br/> | <span data-ttu-id="5e35c-199">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e35c-199">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e35c-200">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e35c-200">Minimum supported server</span></span><br/> | <span data-ttu-id="5e35c-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e35c-201">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e35c-202">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5e35c-202">Namespace</span></span><br/>                | <span data-ttu-id="5e35c-203">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5e35c-203">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5e35c-204">MOF</span><span class="sxs-lookup"><span data-stu-id="5e35c-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e35c-205"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e35c-205"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e35c-206">DLL</span><span class="sxs-lookup"><span data-stu-id="5e35c-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e35c-207"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e35c-207"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e35c-208">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e35c-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e35c-209">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="5e35c-209">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

