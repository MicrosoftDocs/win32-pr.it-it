---
description: La \_ classe WMI DMAChannel Win32 rappresenta un canale di accesso diretto alla memoria (DMA) in un sistema di computer che esegue Windows.
ms.assetid: cc517aac-7bd4-4937-8b07-2597076fca2c
ms.tgt_platform: multiple
title: Classe Win32_DMAChannel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DMAChannel
- Win32_DMAChannel.AddressSize
- Win32_DMAChannel.Availability
- Win32_DMAChannel.BurstMode
- Win32_DMAChannel.ByteMode
- Win32_DMAChannel.Caption
- Win32_DMAChannel.ChannelTiming
- Win32_DMAChannel.CreationClassName
- Win32_DMAChannel.CSCreationClassName
- Win32_DMAChannel.CSName
- Win32_DMAChannel.Description
- Win32_DMAChannel.DMAChannel
- Win32_DMAChannel.InstallDate
- Win32_DMAChannel.MaxTransferSize
- Win32_DMAChannel.Name
- Win32_DMAChannel.Port
- Win32_DMAChannel.Status
- Win32_DMAChannel.TransferWidths
- Win32_DMAChannel.TypeCTiming
- Win32_DMAChannel.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c2b36ff17931133d0dc4529e34f31ac24e00653
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878150"
---
# <a name="win32_dmachannel-class"></a><span data-ttu-id="c85f3-103">Win32 \_ DMAChannel (classe)</span><span class="sxs-lookup"><span data-stu-id="c85f3-103">Win32\_DMAChannel class</span></span>

<span data-ttu-id="c85f3-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DMAChannel Win32** rappresenta un canale di accesso diretto alla memoria (DMA) in un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="c85f3-104">The **Win32\_DMAChannel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a direct memory access (DMA) channel on a computer system running Windows.</span></span> <span data-ttu-id="c85f3-105">DMA è un metodo di trasferimento dei dati da un dispositivo a memoria (o viceversa) senza l'aiuto del microprocessore.</span><span class="sxs-lookup"><span data-stu-id="c85f3-105">DMA is a method of moving data from a device to memory (or vice versa) without the help of the microprocessor.</span></span> <span data-ttu-id="c85f3-106">La lavagna di sistema usa un controller DMA per gestire un numero fisso di canali, ciascuno dei quali può essere usato da uno (e un solo) dispositivo alla volta.</span><span class="sxs-lookup"><span data-stu-id="c85f3-106">The system board uses a DMA controller to handle a fixed number of channels, each of which can be used by one (and only one) device at a time.</span></span>

<span data-ttu-id="c85f3-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c85f3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c85f3-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c85f3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c85f3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c85f3-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DMAChannel : CIM_DMA
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
  uint32   Port;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="c85f3-110">Members</span><span class="sxs-lookup"><span data-stu-id="c85f3-110">Members</span></span>

<span data-ttu-id="c85f3-111">La classe **Win32 \_ DMAChannel** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c85f3-111">The **Win32\_DMAChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="c85f3-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c85f3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c85f3-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c85f3-113">Properties</span></span>

<span data-ttu-id="c85f3-114">La classe **Win32 \_ DMAChannel** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c85f3-114">The **Win32\_DMAChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c85f3-115">**AddressSize**</span><span class="sxs-lookup"><span data-stu-id="c85f3-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c85f3-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-118">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul DMA della risorsa \| di sistema DMTF 001,3 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="c85f3-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-119">Dimensioni dell'indirizzo del canale DMA in bit.</span><span class="sxs-lookup"><span data-stu-id="c85f3-119">DMA channel address size in bits.</span></span> <span data-ttu-id="c85f3-120">I valori consentiti sono 8, 16, 32 o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="c85f3-120">Permissible values are 8, 16, 32, or 64 bits.</span></span> <span data-ttu-id="c85f3-121">Se è sconosciuto, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="c85f3-121">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="c85f3-122">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-122">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="c85f3-123"> (0)</span><span class="sxs-lookup"><span data-stu-id="c85f3-123">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c85f3-124">(8)</span><span class="sxs-lookup"><span data-stu-id="c85f3-124">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c85f3-125">(16)</span><span class="sxs-lookup"><span data-stu-id="c85f3-125">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c85f3-126">(32)</span><span class="sxs-lookup"><span data-stu-id="c85f3-126">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c85f3-127">(64)</span><span class="sxs-lookup"><span data-stu-id="c85f3-127">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c85f3-128">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="c85f3-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c85f3-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-131">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="c85f3-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-132">Disponibilità del DMA.</span><span class="sxs-lookup"><span data-stu-id="c85f3-132">Availability of the DMA.</span></span> <span data-ttu-id="c85f3-133">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-133">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c85f3-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="c85f3-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c85f3-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="c85f3-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="c85f3-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponibile** (3)</span><span class="sxs-lookup"><span data-stu-id="c85f3-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="c85f3-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In uso/non disponibile** (4)</span><span class="sxs-lookup"><span data-stu-id="c85f3-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c85f3-138">In uso o non disponibile</span><span class="sxs-lookup"><span data-stu-id="c85f3-138">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="c85f3-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In uso e disponibile/condivisibile** (5)</span><span class="sxs-lookup"><span data-stu-id="c85f3-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c85f3-140">In uso e disponibile o condivisibile</span><span class="sxs-lookup"><span data-stu-id="c85f3-140">In Use and Available or Sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c85f3-141">**BurstMode**</span><span class="sxs-lookup"><span data-stu-id="c85f3-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-142">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c85f3-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-144">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="c85f3-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-145">Indica se il canale DMA supporta la modalità a impulsi.</span><span class="sxs-lookup"><span data-stu-id="c85f3-145">Indicates whether or not the DMA channel supports burst mode.</span></span>

<span data-ttu-id="c85f3-146">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-146">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="c85f3-147">**ByteMode**</span><span class="sxs-lookup"><span data-stu-id="c85f3-147">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-148">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c85f3-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-150">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni DMA risorse di sistema \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="c85f3-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-151">Modalità di esecuzione DMA.</span><span class="sxs-lookup"><span data-stu-id="c85f3-151">DMA execution mode.</span></span>

<span data-ttu-id="c85f3-152">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-152">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c85f3-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="c85f3-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c85f3-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="c85f3-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="c85f3-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Non eseguito in modalità' conteggio per byte '** (3)</span><span class="sxs-lookup"><span data-stu-id="c85f3-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c85f3-156">Non viene eseguito in modalità "conteggio per byte"</span><span class="sxs-lookup"><span data-stu-id="c85f3-156">Does not execute in "count by byte" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="c85f3-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Esegui in modalità "conteggio per byte"** (4)</span><span class="sxs-lookup"><span data-stu-id="c85f3-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c85f3-158">Esegui in modalità "conteggio per byte"</span><span class="sxs-lookup"><span data-stu-id="c85f3-158">Execute in "count by byte" mode</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c85f3-159">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="c85f3-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c85f3-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-162">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c85f3-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-163">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="c85f3-163">Short description of the object a one-line string.</span></span>

<span data-ttu-id="c85f3-164">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c85f3-165">**ChannelTiming**</span><span class="sxs-lookup"><span data-stu-id="c85f3-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-166">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c85f3-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-168">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni DMA risorse di sistema \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="c85f3-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-169">Temporizzazione canale DMA.</span><span class="sxs-lookup"><span data-stu-id="c85f3-169">DMA channel timing.</span></span>

<span data-ttu-id="c85f3-170">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-170">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c85f3-171">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="c85f3-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c85f3-172">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="c85f3-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="c85f3-173">**Compatibile con ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="c85f3-173">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="c85f3-174">**Digitare A** (4)</span><span class="sxs-lookup"><span data-stu-id="c85f3-174">**Type A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="c85f3-175">**Digitare B** (5)</span><span class="sxs-lookup"><span data-stu-id="c85f3-175">**Type B** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="c85f3-176">**Digitare F** (6)</span><span class="sxs-lookup"><span data-stu-id="c85f3-176">**Type F** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c85f3-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c85f3-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c85f3-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-180">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c85f3-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-181">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="c85f3-181">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c85f3-182">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="c85f3-182">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c85f3-183">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-183">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="c85f3-184">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c85f3-184">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c85f3-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-187">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c85f3-187">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-188">Nome della classe di creazione dell'ambito del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="c85f3-188">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="c85f3-189">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-189">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="c85f3-190">**CSName**</span><span class="sxs-lookup"><span data-stu-id="c85f3-190">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c85f3-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-193">Qualificatori: [**propagati**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c85f3-193">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-194">Nome del sistema di ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="c85f3-194">Name of the scoping computer system.</span></span>

<span data-ttu-id="c85f3-195">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-195">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="c85f3-196">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c85f3-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c85f3-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-199">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c85f3-199">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-200">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c85f3-200">Description of the object.</span></span>

<span data-ttu-id="c85f3-201">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c85f3-202">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="c85f3-202">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-203">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c85f3-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-205">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="c85f3-205">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-206">Numero del canale DMA, parte del valore della chiave dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c85f3-206">DMA channel number, part of the object's key value.</span></span>

<span data-ttu-id="c85f3-207">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-207">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="c85f3-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c85f3-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-209">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c85f3-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-211">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="c85f3-211">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-212">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c85f3-212">Date and time the object was installed.</span></span> <span data-ttu-id="c85f3-213">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="c85f3-213">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c85f3-214">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c85f3-215">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="c85f3-215">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-216">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c85f3-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-218">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul DMA della risorsa \| di sistema DMTF 001,4 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="c85f3-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-219">Numero massimo di byte che possono essere trasferiti da questo canale DMA.</span><span class="sxs-lookup"><span data-stu-id="c85f3-219">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="c85f3-220">Se è sconosciuto, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="c85f3-220">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="c85f3-221">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-221">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="c85f3-222">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c85f3-222">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c85f3-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-225">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c85f3-225">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-226">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="c85f3-226">Label by which the object is known.</span></span> <span data-ttu-id="c85f3-227">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="c85f3-227">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="c85f3-228">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c85f3-229">**Porta**</span><span class="sxs-lookup"><span data-stu-id="c85f3-229">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-230">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c85f3-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-232">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| strutture di sistema Win32API \| [**cm porta DMA \_ \_ \_ descrittore risorse parziali**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor) \| \| ")</span><span class="sxs-lookup"><span data-stu-id="c85f3-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Dma\|Port")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-233">Porta DMA utilizzata dalla scheda bus host.</span><span class="sxs-lookup"><span data-stu-id="c85f3-233">DMA port used by the host bus adapter.</span></span> <span data-ttu-id="c85f3-234">Questa operazione è significativa per i bus di tipo MCA.</span><span class="sxs-lookup"><span data-stu-id="c85f3-234">This is meaningful for MCA-type buses.</span></span>

<span data-ttu-id="c85f3-235">Example: 12</span><span class="sxs-lookup"><span data-stu-id="c85f3-235">Example: 12</span></span>

</dd> <dt>

<span data-ttu-id="c85f3-236">**Status**</span><span class="sxs-lookup"><span data-stu-id="c85f3-236">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c85f3-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-239">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c85f3-239">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-240">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c85f3-240">Current status of the object.</span></span> <span data-ttu-id="c85f3-241">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="c85f3-241">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c85f3-242">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="c85f3-242">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c85f3-243">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="c85f3-243">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c85f3-244">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="c85f3-244">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c85f3-245">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="c85f3-245">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c85f3-246">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-246">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c85f3-247">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c85f3-247">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c85f3-248">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c85f3-248">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c85f3-249">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="c85f3-249">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c85f3-250">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="c85f3-250">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c85f3-251">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="c85f3-251">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c85f3-252">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="c85f3-252">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c85f3-253">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="c85f3-253">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c85f3-254">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="c85f3-254">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c85f3-255">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="c85f3-255">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c85f3-256">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="c85f3-256">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c85f3-257">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="c85f3-257">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c85f3-258">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="c85f3-258">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c85f3-259">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="c85f3-259">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c85f3-260">**TransferWidths**</span><span class="sxs-lookup"><span data-stu-id="c85f3-260">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-261">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c85f3-261">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-263">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul DMA della risorsa \| di sistema DMTF 001,2 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="c85f3-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-264">Matrice di tutte le larghezze di trasferimento (in bit) supportate da questo canale DMA.</span><span class="sxs-lookup"><span data-stu-id="c85f3-264">Array of all the transfer widths (in bits) supported by this DMA channel.</span></span> <span data-ttu-id="c85f3-265">Se è sconosciuto, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="c85f3-265">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="c85f3-266">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-266">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="c85f3-267"> (0)</span><span class="sxs-lookup"><span data-stu-id="c85f3-267">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c85f3-268">(8)</span><span class="sxs-lookup"><span data-stu-id="c85f3-268">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c85f3-269">(16)</span><span class="sxs-lookup"><span data-stu-id="c85f3-269">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c85f3-270">(32)</span><span class="sxs-lookup"><span data-stu-id="c85f3-270">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c85f3-271">(64)</span><span class="sxs-lookup"><span data-stu-id="c85f3-271">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c85f3-272">(128)</span><span class="sxs-lookup"><span data-stu-id="c85f3-272">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c85f3-273">**TypeCTiming**</span><span class="sxs-lookup"><span data-stu-id="c85f3-273">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-274">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c85f3-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-276">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni DMA risorse di sistema \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="c85f3-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-277">Supporto per l'intervallo di tipo C (picchi).</span><span class="sxs-lookup"><span data-stu-id="c85f3-277">Support for C type (burst) timing.</span></span>

<span data-ttu-id="c85f3-278">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-278">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c85f3-279">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="c85f3-279">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c85f3-280">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="c85f3-280">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="c85f3-281">**Compatibile con ISA** (3)</span><span class="sxs-lookup"><span data-stu-id="c85f3-281">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c85f3-282">**Non supportato** (4)</span><span class="sxs-lookup"><span data-stu-id="c85f3-282">**Not Supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="c85f3-283">**Supportato** (5)</span><span class="sxs-lookup"><span data-stu-id="c85f3-283">**Supported** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c85f3-284">**WordMode**</span><span class="sxs-lookup"><span data-stu-id="c85f3-284">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85f3-285">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c85f3-285">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c85f3-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85f3-287">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni DMA risorse di sistema \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="c85f3-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="c85f3-288">Modalità di esecuzione DMA.</span><span class="sxs-lookup"><span data-stu-id="c85f3-288">DMA execution mode.</span></span>

<span data-ttu-id="c85f3-289">Questa proprietà viene ereditata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-289">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c85f3-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="c85f3-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c85f3-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="c85f3-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="c85f3-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Non eseguito in modalità' conteggio per parola '** (3)</span><span class="sxs-lookup"><span data-stu-id="c85f3-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c85f3-293">Non viene eseguito in modalità "conteggio per parola"</span><span class="sxs-lookup"><span data-stu-id="c85f3-293">Does not execute in "count by word" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="c85f3-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Esegui in modalità "conteggio per parola"** (4)</span><span class="sxs-lookup"><span data-stu-id="c85f3-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c85f3-295">Esegui in modalità "conteggio per parola"</span><span class="sxs-lookup"><span data-stu-id="c85f3-295">Execute in "count by word" mode</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c85f3-296">Commenti</span><span class="sxs-lookup"><span data-stu-id="c85f3-296">Remarks</span></span>

<span data-ttu-id="c85f3-297">La classe **Win32 \_ DMAChannel** è derivata da [**CIM \_ DMA**](cim-dma.md).</span><span class="sxs-lookup"><span data-stu-id="c85f3-297">The **Win32\_DMAChannel** class is derived from [**CIM\_DMA**](cim-dma.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c85f3-298">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c85f3-298">Requirements</span></span>



| <span data-ttu-id="c85f3-299">Requisito</span><span class="sxs-lookup"><span data-stu-id="c85f3-299">Requirement</span></span> | <span data-ttu-id="c85f3-300">Valore</span><span class="sxs-lookup"><span data-stu-id="c85f3-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c85f3-301">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c85f3-301">Minimum supported client</span></span><br/> | <span data-ttu-id="c85f3-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c85f3-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c85f3-303">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c85f3-303">Minimum supported server</span></span><br/> | <span data-ttu-id="c85f3-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c85f3-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c85f3-305">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c85f3-305">Namespace</span></span><br/>                | <span data-ttu-id="c85f3-306">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c85f3-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c85f3-307">MOF</span><span class="sxs-lookup"><span data-stu-id="c85f3-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c85f3-308"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c85f3-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c85f3-309">DLL</span><span class="sxs-lookup"><span data-stu-id="c85f3-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c85f3-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c85f3-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c85f3-311">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c85f3-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c85f3-312">**\_DMA CIM**</span><span class="sxs-lookup"><span data-stu-id="c85f3-312">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dt>

[<span data-ttu-id="c85f3-313">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="c85f3-313">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

