---
description: La \_ classe CIM DMA rappresenta l'accesso diretto alla memoria (DMA) dell'architettura del computer.
ms.assetid: 101fa9f3-a403-487d-8482-b1e8e9f957d6
ms.tgt_platform: multiple
title: Classe CIM_DMA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DMA
- CIM_DMA.AddressSize
- CIM_DMA.Availability
- CIM_DMA.BurstMode
- CIM_DMA.ByteMode
- CIM_DMA.Caption
- CIM_DMA.ChannelTiming
- CIM_DMA.CreationClassName
- CIM_DMA.CSCreationClassName
- CIM_DMA.CSName
- CIM_DMA.Description
- CIM_DMA.DMAChannel
- CIM_DMA.InstallDate
- CIM_DMA.MaxTransferSize
- CIM_DMA.Name
- CIM_DMA.Status
- CIM_DMA.TransferWidths
- CIM_DMA.TypeCTiming
- CIM_DMA.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71fe9c0ad29afa7be20df6fbf05c5d1183d23d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966166"
---
# <a name="cim_dma-class"></a><span data-ttu-id="2a154-103">\_Classe CIM DMA</span><span class="sxs-lookup"><span data-stu-id="2a154-103">CIM\_DMA class</span></span>

<span data-ttu-id="2a154-104">La classe **CIM \_ DMA** rappresenta l'accesso diretto alla memoria (DMA) dell'architettura del computer.</span><span class="sxs-lookup"><span data-stu-id="2a154-104">The **CIM\_DMA** class represents computer architecture direct memory access (DMA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a154-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="2a154-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2a154-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2a154-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2a154-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2a154-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2a154-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2a154-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a154-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a154-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C523-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DMA : CIM_SystemResource
{
  uint16   AddressSize;
  uint16   Availability;
  boolean  BurstMode;
  uint16   ByteMode;
  string   Caption;
  uint16   ChannelTiming;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint32   DMAChannel;
  datetime InstallDate;
  uint32   MaxTransferSize;
  string   Name;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="2a154-110">Members</span><span class="sxs-lookup"><span data-stu-id="2a154-110">Members</span></span>

<span data-ttu-id="2a154-111">La classe **CIM \_ DMA** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2a154-111">The **CIM\_DMA** class has these types of members:</span></span>

-   [<span data-ttu-id="2a154-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a154-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a154-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a154-113">Properties</span></span>

<span data-ttu-id="2a154-114">La classe **CIM \_ DMA** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2a154-114">The **CIM\_DMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a154-115">**AddressSize**</span><span class="sxs-lookup"><span data-stu-id="2a154-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a154-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-118">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul DMA della risorsa \| di sistema DMTF 001,3 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="2a154-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-119">Dimensioni dell'indirizzo del canale DMA in bit.</span><span class="sxs-lookup"><span data-stu-id="2a154-119">DMA channel address size, in bits.</span></span> <span data-ttu-id="2a154-120">I valori consentiti sono 8, 16, 32 e 64.</span><span class="sxs-lookup"><span data-stu-id="2a154-120">Permissible values are 8, 16, 32, and 64.</span></span> <span data-ttu-id="2a154-121">Se è sconosciuto, immettere 0.</span><span class="sxs-lookup"><span data-stu-id="2a154-121">If unknown, enter 0.</span></span>

<dt>



 <span data-ttu-id="2a154-122"> (0)</span><span class="sxs-lookup"><span data-stu-id="2a154-122">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a154-123">(8)</span><span class="sxs-lookup"><span data-stu-id="2a154-123">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a154-124">(16)</span><span class="sxs-lookup"><span data-stu-id="2a154-124">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a154-125">(32)</span><span class="sxs-lookup"><span data-stu-id="2a154-125">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a154-126">(64)</span><span class="sxs-lookup"><span data-stu-id="2a154-126">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a154-127">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="2a154-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-128">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a154-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-130">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="2a154-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-131">Disponibilità del DMA.</span><span class="sxs-lookup"><span data-stu-id="2a154-131">Availability of the DMA.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2a154-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2a154-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a154-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2a154-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-134">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2a154-134">Unknown.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="2a154-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponibile** (3)</span><span class="sxs-lookup"><span data-stu-id="2a154-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-136">Disponibile.</span><span class="sxs-lookup"><span data-stu-id="2a154-136">Available.</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="2a154-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In uso/non disponibile** (4)</span><span class="sxs-lookup"><span data-stu-id="2a154-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-138">In uso (non disponibile).</span><span class="sxs-lookup"><span data-stu-id="2a154-138">In use (not available).</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="2a154-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In uso e disponibile/condivisibile** (5)</span><span class="sxs-lookup"><span data-stu-id="2a154-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-140">In uso, ma disponibile (condivisibile).</span><span class="sxs-lookup"><span data-stu-id="2a154-140">In use, but available (sharable).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2a154-141">**BurstMode**</span><span class="sxs-lookup"><span data-stu-id="2a154-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-142">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2a154-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-144">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="2a154-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-145">Se **true**, il canale DMA supporta la modalità a impulsi.</span><span class="sxs-lookup"><span data-stu-id="2a154-145">If **TRUE**, the DMA channel supports burst mode.</span></span>

</dd> <dt>

<span data-ttu-id="2a154-146">**ByteMode**</span><span class="sxs-lookup"><span data-stu-id="2a154-146">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-147">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a154-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-149">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni DMA risorse di sistema \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="2a154-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-150">Indica se il DMA può essere eseguito in modalità conteggio per byte.</span><span class="sxs-lookup"><span data-stu-id="2a154-150">Indicates whether DMA can execute in count-by-byte mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2a154-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2a154-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-152">Altro.</span><span class="sxs-lookup"><span data-stu-id="2a154-152">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a154-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2a154-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-154">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2a154-154">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="2a154-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Non eseguito in modalità' conteggio per byte '** (3)</span><span class="sxs-lookup"><span data-stu-id="2a154-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-156">Non può essere eseguito in modalità conteggio per byte.</span><span class="sxs-lookup"><span data-stu-id="2a154-156">Cannot execute in count-by-byte mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="2a154-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Esegui in modalità "conteggio per byte"** (4)</span><span class="sxs-lookup"><span data-stu-id="2a154-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-158">Può essere eseguito in modalità conteggio per byte.</span><span class="sxs-lookup"><span data-stu-id="2a154-158">Able to execute in count-by-byte mode.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2a154-159">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2a154-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a154-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-162">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2a154-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-163">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a154-163">Short textual description of the object.</span></span>

<span data-ttu-id="2a154-164">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a154-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a154-165">**ChannelTiming**</span><span class="sxs-lookup"><span data-stu-id="2a154-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-166">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a154-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-168">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni DMA risorse di sistema \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="2a154-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-169">Temporizzazione canale DMA.</span><span class="sxs-lookup"><span data-stu-id="2a154-169">DMA channel timing.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2a154-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2a154-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-171">Altro.</span><span class="sxs-lookup"><span data-stu-id="2a154-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a154-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2a154-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-173">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2a154-173">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="2a154-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**Compatibile con ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="2a154-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-175">Compatibile con ISA.</span><span class="sxs-lookup"><span data-stu-id="2a154-175">ISA-compatible.</span></span>

</dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="2a154-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Digitare A** (4)</span><span class="sxs-lookup"><span data-stu-id="2a154-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Type A** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-177">Digitare A.</span><span class="sxs-lookup"><span data-stu-id="2a154-177">Type A.</span></span>

</dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="2a154-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Digitare B** (5)</span><span class="sxs-lookup"><span data-stu-id="2a154-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Type B** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-179">Digitare B.</span><span class="sxs-lookup"><span data-stu-id="2a154-179">Type B.</span></span>

</dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="2a154-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Digitare F** (6)</span><span class="sxs-lookup"><span data-stu-id="2a154-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Type F** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-181">Digitare F.</span><span class="sxs-lookup"><span data-stu-id="2a154-181">Type F.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2a154-182">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2a154-182">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a154-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-185">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2a154-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2a154-186">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="2a154-186">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2a154-187">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="2a154-187">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="2a154-188">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2a154-188">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a154-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-191">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2a154-191">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2a154-192">Nome della classe di creazione dell'ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="2a154-192">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="2a154-193">**CSName**</span><span class="sxs-lookup"><span data-stu-id="2a154-193">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a154-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-196">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2a154-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2a154-197">Nome del sistema del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="2a154-197">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="2a154-198">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2a154-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a154-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-201">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2a154-201">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-202">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a154-202">Textual description of the object.</span></span>

<span data-ttu-id="2a154-203">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a154-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a154-204">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="2a154-204">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-205">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a154-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-207">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="2a154-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-208">Numero del canale DMA.</span><span class="sxs-lookup"><span data-stu-id="2a154-208">DMA channel number.</span></span> <span data-ttu-id="2a154-209">Questo numero fa parte del valore della chiave dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a154-209">This number is part of the object's key value.</span></span>

</dd> <dt>

<span data-ttu-id="2a154-210">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2a154-210">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-211">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2a154-211">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-213">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="2a154-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-214">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a154-214">Date and time the object was installed.</span></span> <span data-ttu-id="2a154-215">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="2a154-215">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2a154-216">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a154-216">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a154-217">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="2a154-217">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-218">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a154-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-220">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul DMA della risorsa \| di sistema DMTF 001,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="2a154-220">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-221">Numero massimo di byte che possono essere trasferiti da questo canale DMA.</span><span class="sxs-lookup"><span data-stu-id="2a154-221">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="2a154-222">Se è sconosciuto, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="2a154-222">If unknown, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="2a154-223">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2a154-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-224">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a154-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-226">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2a154-226">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-227">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="2a154-227">Label by which the object is known.</span></span> <span data-ttu-id="2a154-228">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="2a154-228">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2a154-229">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a154-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a154-230">**Status**</span><span class="sxs-lookup"><span data-stu-id="2a154-230">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-231">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a154-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-233">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2a154-233">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-234">Indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a154-234">Indicates the current status of the object.</span></span>

<span data-ttu-id="2a154-235">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2a154-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2a154-236">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a154-236">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2a154-237">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2a154-237">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2a154-238">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="2a154-238">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2a154-239">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="2a154-239">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a154-240">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="2a154-240">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2a154-241">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="2a154-241">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2a154-242">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="2a154-242">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2a154-243">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="2a154-243">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2a154-244">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="2a154-244">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2a154-245">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="2a154-245">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2a154-246">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="2a154-246">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2a154-247">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="2a154-247">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2a154-248">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="2a154-248">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a154-249">**TransferWidths**</span><span class="sxs-lookup"><span data-stu-id="2a154-249">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-250">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a154-250">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2a154-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-252">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul DMA della risorsa \| di sistema DMTF 001,2 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="2a154-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-253">Matrice che indica tutte le larghezze di trasferimento, in bit, supportate da questo canale DMA.</span><span class="sxs-lookup"><span data-stu-id="2a154-253">Array that indicates all of the transfer widths, in bits, supported by this DMA channel.</span></span> <span data-ttu-id="2a154-254">I valori consentiti sono 8, 16, 32, 64 e 128 bit.</span><span class="sxs-lookup"><span data-stu-id="2a154-254">Permissible values are 8, 16, 32, 64, and 128 bits.</span></span> <span data-ttu-id="2a154-255">Se è sconosciuto, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="2a154-255">If unknown, enter 0 (zero).</span></span>

<dt>



 <span data-ttu-id="2a154-256"> (0)</span><span class="sxs-lookup"><span data-stu-id="2a154-256">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a154-257">(8)</span><span class="sxs-lookup"><span data-stu-id="2a154-257">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a154-258">(16)</span><span class="sxs-lookup"><span data-stu-id="2a154-258">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a154-259">(32)</span><span class="sxs-lookup"><span data-stu-id="2a154-259">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a154-260">(64)</span><span class="sxs-lookup"><span data-stu-id="2a154-260">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2a154-261">(128)</span><span class="sxs-lookup"><span data-stu-id="2a154-261">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2a154-262">**TypeCTiming**</span><span class="sxs-lookup"><span data-stu-id="2a154-262">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-263">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a154-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-265">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni DMA risorse di sistema \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="2a154-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-266">Indica se è supportato l'intervallo di tipo C (impulso).</span><span class="sxs-lookup"><span data-stu-id="2a154-266">Indicates whether Type C (burst) timing is supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2a154-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2a154-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-268">Altro.</span><span class="sxs-lookup"><span data-stu-id="2a154-268">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a154-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2a154-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-270">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2a154-270">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="2a154-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**Compatibile con ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="2a154-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-272">Compatibile con ISA.</span><span class="sxs-lookup"><span data-stu-id="2a154-272">ISA-compatible.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2a154-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (4)</span><span class="sxs-lookup"><span data-stu-id="2a154-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-274">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="2a154-274">Not supported.</span></span>

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="2a154-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Supportato** (5)</span><span class="sxs-lookup"><span data-stu-id="2a154-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Supported** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-276">Supportata.</span><span class="sxs-lookup"><span data-stu-id="2a154-276">Supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2a154-277">**WordMode**</span><span class="sxs-lookup"><span data-stu-id="2a154-277">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a154-278">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a154-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a154-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a154-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a154-280">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni DMA risorse di sistema \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="2a154-280">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="2a154-281">Indica se il DMA può essere eseguito in modalità conteggio per parola.</span><span class="sxs-lookup"><span data-stu-id="2a154-281">Indicates whether DMA can execute in count-by-word mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2a154-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2a154-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-283">Altro.</span><span class="sxs-lookup"><span data-stu-id="2a154-283">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2a154-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="2a154-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-285">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2a154-285">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="2a154-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Non eseguito in modalità' conteggio per parola '** (3)</span><span class="sxs-lookup"><span data-stu-id="2a154-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-287">Non può essere eseguito in modalità conteggio per parola.</span><span class="sxs-lookup"><span data-stu-id="2a154-287">Cannot execute in count-by-word mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="2a154-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Esegui in modalità "conteggio per parola"** (4)</span><span class="sxs-lookup"><span data-stu-id="2a154-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2a154-289">Può essere eseguito in modalità conteggio per parola.</span><span class="sxs-lookup"><span data-stu-id="2a154-289">Able to execute in count-by-word mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a154-290">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a154-290">Remarks</span></span>

<span data-ttu-id="2a154-291">La classe **CIM \_ DMA** è derivata da [**CIM \_ SystemResource**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="2a154-291">The **CIM\_DMA** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="2a154-292">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="2a154-292">WMI does not implement this class.</span></span> <span data-ttu-id="2a154-293">Per le classi derivate da **CIM \_ DMA**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2a154-293">For classes derived from **CIM\_DMA**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2a154-294">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="2a154-294">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2a154-295">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="2a154-295">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a154-296">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a154-296">Requirements</span></span>



| <span data-ttu-id="2a154-297">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a154-297">Requirement</span></span> | <span data-ttu-id="2a154-298">Valore</span><span class="sxs-lookup"><span data-stu-id="2a154-298">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a154-299">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a154-299">Minimum supported client</span></span><br/> | <span data-ttu-id="2a154-300">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a154-300">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2a154-301">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a154-301">Minimum supported server</span></span><br/> | <span data-ttu-id="2a154-302">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a154-302">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2a154-303">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2a154-303">Namespace</span></span><br/>                | <span data-ttu-id="2a154-304">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2a154-304">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2a154-305">MOF</span><span class="sxs-lookup"><span data-stu-id="2a154-305">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a154-306"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a154-306"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a154-307">DLL</span><span class="sxs-lookup"><span data-stu-id="2a154-307">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a154-308"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a154-308"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a154-309">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a154-309">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a154-310">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="2a154-310">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

