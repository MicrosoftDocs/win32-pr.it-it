---
description: Descrive le funzionalità e la gestione di un controller seriale.
ms.assetid: ce3e0424-4ab8-435d-a155-1164535b3b0d
title: Classe CIM_SerialController (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a2e69bab38bb8b68c15ed93b2bee721c35a7600
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307768"
---
# <a name="cim_serialcontroller-class-hyper-v-management"></a><span data-ttu-id="84c8a-103">Classe CIM_SerialController (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="84c8a-103">CIM_SerialController class (Hyper-V management)</span></span>

<span data-ttu-id="84c8a-104">Descrive le funzionalità e la gestione di un controller seriale.</span><span class="sxs-lookup"><span data-stu-id="84c8a-104">Describes the capabilities and management of a serial controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c8a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84c8a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_SerialController : CIM_Controller
{
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint32 MaxBaudRate;
  uint16 Security;
};
```

## <a name="members"></a><span data-ttu-id="84c8a-106">Members</span><span class="sxs-lookup"><span data-stu-id="84c8a-106">Members</span></span>

<span data-ttu-id="84c8a-107">La classe **CIM \_ controller seriale** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="84c8a-107">The **CIM\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="84c8a-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84c8a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84c8a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84c8a-109">Properties</span></span>

<span data-ttu-id="84c8a-110">La classe **CIM \_ controller seriale** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="84c8a-110">The **CIM\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84c8a-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="84c8a-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c8a-112">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84c8a-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="84c8a-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84c8a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c8a-114">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porte seriali DMTF \| 004,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ controller seriale**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="84c8a-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="84c8a-115">Compatibilità a livello di chip per il controller seriale.</span><span class="sxs-lookup"><span data-stu-id="84c8a-115">The chip level compatibility for the serial controller.</span></span> <span data-ttu-id="84c8a-116">Questa proprietà descrive il buffering e altre funzionalità del controller seriale che potrebbero essere inerenti all'hardware del chip.</span><span class="sxs-lookup"><span data-stu-id="84c8a-116">This property describes the buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="84c8a-117">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="84c8a-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84c8a-118">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="84c8a-118">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="84c8a-119">**XT/AT Compatible** (3)</span><span class="sxs-lookup"><span data-stu-id="84c8a-119">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="84c8a-120">**16450 compatibile** (4)</span><span class="sxs-lookup"><span data-stu-id="84c8a-120">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="84c8a-121">**16550 compatibile** (5)</span><span class="sxs-lookup"><span data-stu-id="84c8a-121">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="84c8a-122">**compatibile con 16550A** (6)</span><span class="sxs-lookup"><span data-stu-id="84c8a-122">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="84c8a-123">**8251 compatibile** (160)</span><span class="sxs-lookup"><span data-stu-id="84c8a-123">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="84c8a-124">**compatibile con 8251FIFO** (161)</span><span class="sxs-lookup"><span data-stu-id="84c8a-124">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84c8a-125">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="84c8a-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c8a-126">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="84c8a-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="84c8a-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84c8a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c8a-128">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ controller seriale**.**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="84c8a-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="84c8a-129">Matrice che contiene spiegazioni più dettagliate per le funzionalità del controller seriale nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="84c8a-129">An array that contains more detailed explanations for serial controller features in the **Capabilities** array.</span></span> <span data-ttu-id="84c8a-130">Gli elementi nella matrice **CapabilityDescriptions** sono correlati a quelli nella matrice delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="84c8a-130">The items in the **CapabilityDescriptions** array correlate to those in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="84c8a-131">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="84c8a-131">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c8a-132">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84c8a-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84c8a-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84c8a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c8a-134">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| porte seriali \| 004,6 "), **punito** (" bit/secondo ")</span><span class="sxs-lookup"><span data-stu-id="84c8a-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.6"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="84c8a-135">Velocità massima in baud, in bit al secondo, supportata dal controller seriale.</span><span class="sxs-lookup"><span data-stu-id="84c8a-135">The maximum baud rate in, bits per second, that is supported by the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="84c8a-136">**Sicurezza**</span><span class="sxs-lookup"><span data-stu-id="84c8a-136">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84c8a-137">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84c8a-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84c8a-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84c8a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84c8a-139">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porte seriali DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="84c8a-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="84c8a-140">Sicurezza operativa per il controller.</span><span class="sxs-lookup"><span data-stu-id="84c8a-140">The operational security for the controller.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="84c8a-141">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="84c8a-141">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84c8a-142">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="84c8a-142">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="84c8a-143">**Nessuno** (3)</span><span class="sxs-lookup"><span data-stu-id="84c8a-143">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Locked_Out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="84c8a-144">**Interfaccia esterna bloccata** (4)</span><span class="sxs-lookup"><span data-stu-id="84c8a-144">**External Interface Locked Out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="84c8a-145">**Interfaccia esterna abilitata** (5)</span><span class="sxs-lookup"><span data-stu-id="84c8a-145">**External Interface Enabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="84c8a-146">**Bypass di avvio** (6)</span><span class="sxs-lookup"><span data-stu-id="84c8a-146">**Boot Bypass** (6)</span></span>


<span data-ttu-id="84c8a-147"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="84c8a-147"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="84c8a-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84c8a-148">Requirements</span></span>



| <span data-ttu-id="84c8a-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="84c8a-149">Requirement</span></span> | <span data-ttu-id="84c8a-150">Valore</span><span class="sxs-lookup"><span data-stu-id="84c8a-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c8a-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84c8a-151">Minimum supported client</span></span><br/> | <span data-ttu-id="84c8a-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="84c8a-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="84c8a-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84c8a-153">Minimum supported server</span></span><br/> | <span data-ttu-id="84c8a-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84c8a-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="84c8a-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="84c8a-155">Namespace</span></span><br/>                | <span data-ttu-id="84c8a-156">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="84c8a-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="84c8a-157">MOF</span><span class="sxs-lookup"><span data-stu-id="84c8a-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84c8a-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84c8a-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84c8a-159">DLL</span><span class="sxs-lookup"><span data-stu-id="84c8a-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84c8a-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84c8a-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84c8a-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84c8a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c8a-162">**\_Controller CIM**</span><span class="sxs-lookup"><span data-stu-id="84c8a-162">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

