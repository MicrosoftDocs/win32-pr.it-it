---
description: La \_ classe di slot CIM rappresenta i connettori in cui vengono inseriti i pacchetti.
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: Classe CIM_Slot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a63c8cd200096aa132d8205691669d765e54f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483829"
---
# <a name="cim_slot-class"></a><span data-ttu-id="3eaca-103">\_Classe slot CIM</span><span class="sxs-lookup"><span data-stu-id="3eaca-103">CIM\_Slot class</span></span>

<span data-ttu-id="3eaca-104">La classe di **\_ slot CIM** rappresenta i connettori in cui vengono inseriti i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="3eaca-104">The **CIM\_Slot** class represents connectors into which packages are inserted.</span></span> <span data-ttu-id="3eaca-105">Ad esempio, un pacchetto fisico che è un'unità disco può essere inserito in uno slot SCA oppure una scheda (una sottoclasse di [CIM \_ PhysicalPackage](cim-physicalpackage.md)) può essere inserita in uno slot di espansione a 16, 32 o 64 in una lavagna di hosting.</span><span class="sxs-lookup"><span data-stu-id="3eaca-105">For example, a physical package that is a disk drive can be inserted into an SCA slot, or a card (a subclass of [CIM\_PhysicalPackage](cim-physicalpackage.md)) can be inserted into a 16-, 32-, or 64-bit expansion slot on a hosting board.</span></span> <span data-ttu-id="3eaca-106">Gli slot PCI o PCMCIA di tipo III sono esempi del secondo.</span><span class="sxs-lookup"><span data-stu-id="3eaca-106">PCI or PCMCIA Type III Slots are examples of the latter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3eaca-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="3eaca-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3eaca-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3eaca-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3eaca-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3eaca-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3eaca-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3eaca-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eaca-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3eaca-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a><span data-ttu-id="3eaca-112">Members</span><span class="sxs-lookup"><span data-stu-id="3eaca-112">Members</span></span>

<span data-ttu-id="3eaca-113">La classe di **\_ slot CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3eaca-113">The **CIM\_Slot** class has these types of members:</span></span>

-   [<span data-ttu-id="3eaca-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3eaca-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3eaca-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3eaca-115">Properties</span></span>

<span data-ttu-id="3eaca-116">La **classe \_ slot CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3eaca-116">The **CIM\_Slot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3eaca-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="3eaca-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3eaca-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-121">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3eaca-121">Short textual description of the object.</span></span>

<span data-ttu-id="3eaca-122">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-123">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="3eaca-123">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-126">Stringa in formato libero che descrive la configurazione del PIN e l'uso del segnale di un connettore fisico.</span><span class="sxs-lookup"><span data-stu-id="3eaca-126">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

<span data-ttu-id="3eaca-127">Questa proprietà viene ereditata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-127">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-128">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="3eaca-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-129">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3eaca-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-131">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Slot di sistema DMTF \| 004,2 ")</span><span class="sxs-lookup"><span data-stu-id="3eaca-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.2")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-132">Tipo di connettore fisico.</span><span class="sxs-lookup"><span data-stu-id="3eaca-132">Type of physical connector.</span></span> <span data-ttu-id="3eaca-133">Viene specificata una matrice per consentire la descrizione delle combinazioni di informazioni del connettore.</span><span class="sxs-lookup"><span data-stu-id="3eaca-133">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="3eaca-134">Una voce della matrice, ad esempio, può specificare RS-232, un altro DB-25 e un terzo può definire il connettore come "maschio".</span><span class="sxs-lookup"><span data-stu-id="3eaca-134">For example, one array entry could specify RS-232, another DB-25, and a third could define the connector as "Male".</span></span>

<span data-ttu-id="3eaca-135">Questa proprietà viene ereditata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-135">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<dt>

<span data-ttu-id="3eaca-136">0</span><span class="sxs-lookup"><span data-stu-id="3eaca-136">0</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-137">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="3eaca-137">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-138">1</span><span class="sxs-lookup"><span data-stu-id="3eaca-138">1</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-139">Altro</span><span class="sxs-lookup"><span data-stu-id="3eaca-139">Other</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-140">2</span><span class="sxs-lookup"><span data-stu-id="3eaca-140">2</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-141">Male</span><span class="sxs-lookup"><span data-stu-id="3eaca-141">Male</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-142">3</span><span class="sxs-lookup"><span data-stu-id="3eaca-142">3</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-143">Female</span><span class="sxs-lookup"><span data-stu-id="3eaca-143">Female</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-144">4</span><span class="sxs-lookup"><span data-stu-id="3eaca-144">4</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-145">Schermato</span><span class="sxs-lookup"><span data-stu-id="3eaca-145">Shielded</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-146">5</span><span class="sxs-lookup"><span data-stu-id="3eaca-146">5</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-147">Eseguendolo</span><span class="sxs-lookup"><span data-stu-id="3eaca-147">Unshielded</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-148">6</span><span class="sxs-lookup"><span data-stu-id="3eaca-148">6</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-149">SCSI (A) ad alta densità (50 pin)</span><span class="sxs-lookup"><span data-stu-id="3eaca-149">SCSI (A) High-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-150">7</span><span class="sxs-lookup"><span data-stu-id="3eaca-150">7</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-151">SCSI (A) A bassa densità (50 pin)</span><span class="sxs-lookup"><span data-stu-id="3eaca-151">SCSI (A) Low-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-152">8</span><span class="sxs-lookup"><span data-stu-id="3eaca-152">8</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-153">SCSI (P) ad alta densità (68 pin)</span><span class="sxs-lookup"><span data-stu-id="3eaca-153">SCSI (P) High-density (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-154">9</span><span class="sxs-lookup"><span data-stu-id="3eaca-154">9</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-155">SCSI SCA-I (80 pin)</span><span class="sxs-lookup"><span data-stu-id="3eaca-155">SCSI SCA-I (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-156">10</span><span class="sxs-lookup"><span data-stu-id="3eaca-156">10</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-157">SCSI SCA-II (80 pin)</span><span class="sxs-lookup"><span data-stu-id="3eaca-157">SCSI SCA-II (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-158">11</span><span class="sxs-lookup"><span data-stu-id="3eaca-158">11</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-159">Fibre Channel SCSI (DB-9, rame)</span><span class="sxs-lookup"><span data-stu-id="3eaca-159">SCSI Fibre Channel (DB-9, Copper)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-160">12</span><span class="sxs-lookup"><span data-stu-id="3eaca-160">12</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-161">Fibre Channel SCSI (fibre)</span><span class="sxs-lookup"><span data-stu-id="3eaca-161">SCSI Fibre Channel (Fibre)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-162">13</span><span class="sxs-lookup"><span data-stu-id="3eaca-162">13</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-163">SCSI Fibre Channel SCA-II (40 pin)</span><span class="sxs-lookup"><span data-stu-id="3eaca-163">SCSI Fibre Channel SCA-II (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-164">14</span><span class="sxs-lookup"><span data-stu-id="3eaca-164">14</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-165">SCSI Fibre Channel SCA-II (20 pin)</span><span class="sxs-lookup"><span data-stu-id="3eaca-165">SCSI Fibre Channel SCA-II (20 pins)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-166">15</span><span class="sxs-lookup"><span data-stu-id="3eaca-166">15</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-167">SCSI Fibre Channel BNC</span><span class="sxs-lookup"><span data-stu-id="3eaca-167">SCSI Fibre Channel BNC</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-168">16</span><span class="sxs-lookup"><span data-stu-id="3eaca-168">16</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-169">ATA 3-1/2 pollice (40 pin)</span><span class="sxs-lookup"><span data-stu-id="3eaca-169">ATA 3-1/2 Inch (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-170">17</span><span class="sxs-lookup"><span data-stu-id="3eaca-170">17</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-171">ATA 2-1/2 pollice (44 pin)</span><span class="sxs-lookup"><span data-stu-id="3eaca-171">ATA 2-1/2 Inch (44 pins)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-172">18</span><span class="sxs-lookup"><span data-stu-id="3eaca-172">18</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-173">ATA-2</span><span class="sxs-lookup"><span data-stu-id="3eaca-173">ATA-2</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-174">19</span><span class="sxs-lookup"><span data-stu-id="3eaca-174">19</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-175">ATA-3</span><span class="sxs-lookup"><span data-stu-id="3eaca-175">ATA-3</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-176">20</span><span class="sxs-lookup"><span data-stu-id="3eaca-176">20</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-177">ATA/66</span><span class="sxs-lookup"><span data-stu-id="3eaca-177">ATA/66</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-178">21</span><span class="sxs-lookup"><span data-stu-id="3eaca-178">21</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-179">DB-9</span><span class="sxs-lookup"><span data-stu-id="3eaca-179">DB-9</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-180">22</span><span class="sxs-lookup"><span data-stu-id="3eaca-180">22</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-181">DB-15</span><span class="sxs-lookup"><span data-stu-id="3eaca-181">DB-15</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-182">23</span><span class="sxs-lookup"><span data-stu-id="3eaca-182">23</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-183">DB-25</span><span class="sxs-lookup"><span data-stu-id="3eaca-183">DB-25</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-184">24</span><span class="sxs-lookup"><span data-stu-id="3eaca-184">24</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-185">DB-36</span><span class="sxs-lookup"><span data-stu-id="3eaca-185">DB-36</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-186">25</span><span class="sxs-lookup"><span data-stu-id="3eaca-186">25</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-187">RS-232C</span><span class="sxs-lookup"><span data-stu-id="3eaca-187">RS-232C</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-188">26</span><span class="sxs-lookup"><span data-stu-id="3eaca-188">26</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-189">RS-422</span><span class="sxs-lookup"><span data-stu-id="3eaca-189">RS-422</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-190">27</span><span class="sxs-lookup"><span data-stu-id="3eaca-190">27</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-191">RS-423</span><span class="sxs-lookup"><span data-stu-id="3eaca-191">RS-423</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-192">28</span><span class="sxs-lookup"><span data-stu-id="3eaca-192">28</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-193">RS-485</span><span class="sxs-lookup"><span data-stu-id="3eaca-193">RS-485</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-194">29</span><span class="sxs-lookup"><span data-stu-id="3eaca-194">29</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-195">RS-449</span><span class="sxs-lookup"><span data-stu-id="3eaca-195">RS-449</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-196">30</span><span class="sxs-lookup"><span data-stu-id="3eaca-196">30</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-197">V. 35</span><span class="sxs-lookup"><span data-stu-id="3eaca-197">V.35</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-198">31</span><span class="sxs-lookup"><span data-stu-id="3eaca-198">31</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-199">X. 21</span><span class="sxs-lookup"><span data-stu-id="3eaca-199">X.21</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-200">32</span><span class="sxs-lookup"><span data-stu-id="3eaca-200">32</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-201">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="3eaca-201">IEEE-488</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-202">33</span><span class="sxs-lookup"><span data-stu-id="3eaca-202">33</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-203">AUI</span><span class="sxs-lookup"><span data-stu-id="3eaca-203">AUI</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-204">34</span><span class="sxs-lookup"><span data-stu-id="3eaca-204">34</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-205">UTP categoria 3</span><span class="sxs-lookup"><span data-stu-id="3eaca-205">UTP Category 3</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-206">35</span><span class="sxs-lookup"><span data-stu-id="3eaca-206">35</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-207">Categoria 4 UTP</span><span class="sxs-lookup"><span data-stu-id="3eaca-207">UTP Category 4</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-208">36</span><span class="sxs-lookup"><span data-stu-id="3eaca-208">36</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-209">UTP categoria 5</span><span class="sxs-lookup"><span data-stu-id="3eaca-209">UTP Category 5</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-210">37</span><span class="sxs-lookup"><span data-stu-id="3eaca-210">37</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-211">BNC</span><span class="sxs-lookup"><span data-stu-id="3eaca-211">BNC</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-212">38</span><span class="sxs-lookup"><span data-stu-id="3eaca-212">38</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-213">RJ11</span><span class="sxs-lookup"><span data-stu-id="3eaca-213">RJ11</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-214">39</span><span class="sxs-lookup"><span data-stu-id="3eaca-214">39</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-215">RJ45</span><span class="sxs-lookup"><span data-stu-id="3eaca-215">RJ45</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-216">40</span><span class="sxs-lookup"><span data-stu-id="3eaca-216">40</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-217">Fibre MIC</span><span class="sxs-lookup"><span data-stu-id="3eaca-217">Fiber MIC</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-218">41</span><span class="sxs-lookup"><span data-stu-id="3eaca-218">41</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-219">Apple AUI</span><span class="sxs-lookup"><span data-stu-id="3eaca-219">Apple AUI</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-220">42</span><span class="sxs-lookup"><span data-stu-id="3eaca-220">42</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-221">Apple GeoPort</span><span class="sxs-lookup"><span data-stu-id="3eaca-221">Apple GeoPort</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-222">43</span><span class="sxs-lookup"><span data-stu-id="3eaca-222">43</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-223">PCI</span><span class="sxs-lookup"><span data-stu-id="3eaca-223">PCI</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-224">44</span><span class="sxs-lookup"><span data-stu-id="3eaca-224">44</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-225">ISA</span><span class="sxs-lookup"><span data-stu-id="3eaca-225">ISA</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-226">45</span><span class="sxs-lookup"><span data-stu-id="3eaca-226">45</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-227">EISA</span><span class="sxs-lookup"><span data-stu-id="3eaca-227">EISA</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-228">46</span><span class="sxs-lookup"><span data-stu-id="3eaca-228">46</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-229">VESA</span><span class="sxs-lookup"><span data-stu-id="3eaca-229">VESA</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-230">47</span><span class="sxs-lookup"><span data-stu-id="3eaca-230">47</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-231">PCMCIA</span><span class="sxs-lookup"><span data-stu-id="3eaca-231">PCMCIA</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-232">48</span><span class="sxs-lookup"><span data-stu-id="3eaca-232">48</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-233">Tipi PCMCIA I</span><span class="sxs-lookup"><span data-stu-id="3eaca-233">PCMCIA Type I</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-234">49</span><span class="sxs-lookup"><span data-stu-id="3eaca-234">49</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-235">PCMCIA tipo II</span><span class="sxs-lookup"><span data-stu-id="3eaca-235">PCMCIA Type II</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-236">50</span><span class="sxs-lookup"><span data-stu-id="3eaca-236">50</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-237">Tipo PCMCIA III</span><span class="sxs-lookup"><span data-stu-id="3eaca-237">PCMCIA Type III</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-238">51</span><span class="sxs-lookup"><span data-stu-id="3eaca-238">51</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-239">Porta ZV</span><span class="sxs-lookup"><span data-stu-id="3eaca-239">ZV Port</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-240">52</span><span class="sxs-lookup"><span data-stu-id="3eaca-240">52</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-241">CardBus</span><span class="sxs-lookup"><span data-stu-id="3eaca-241">CardBus</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-242">53</span><span class="sxs-lookup"><span data-stu-id="3eaca-242">53</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-243">USB</span><span class="sxs-lookup"><span data-stu-id="3eaca-243">USB</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-244">54</span><span class="sxs-lookup"><span data-stu-id="3eaca-244">54</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-245">IEEE 1394</span><span class="sxs-lookup"><span data-stu-id="3eaca-245">IEEE 1394</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-246">55</span><span class="sxs-lookup"><span data-stu-id="3eaca-246">55</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-247">HIPPI</span><span class="sxs-lookup"><span data-stu-id="3eaca-247">HIPPI</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-248">56</span><span class="sxs-lookup"><span data-stu-id="3eaca-248">56</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-249">HSSDC (6 pin)</span><span class="sxs-lookup"><span data-stu-id="3eaca-249">HSSDC (6 pins)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-250">57</span><span class="sxs-lookup"><span data-stu-id="3eaca-250">57</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-251">GBIC</span><span class="sxs-lookup"><span data-stu-id="3eaca-251">GBIC</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-252">58</span><span class="sxs-lookup"><span data-stu-id="3eaca-252">58</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-253">DIN</span><span class="sxs-lookup"><span data-stu-id="3eaca-253">DIN</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-254">59</span><span class="sxs-lookup"><span data-stu-id="3eaca-254">59</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-255">Mini-DIN</span><span class="sxs-lookup"><span data-stu-id="3eaca-255">Mini-DIN</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-256">60</span><span class="sxs-lookup"><span data-stu-id="3eaca-256">60</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-257">Micro-DIN</span><span class="sxs-lookup"><span data-stu-id="3eaca-257">Micro-DIN</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-258">61</span><span class="sxs-lookup"><span data-stu-id="3eaca-258">61</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-259">PS/2</span><span class="sxs-lookup"><span data-stu-id="3eaca-259">PS/2</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-260">62</span><span class="sxs-lookup"><span data-stu-id="3eaca-260">62</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-261">Infrarossi</span><span class="sxs-lookup"><span data-stu-id="3eaca-261">Infrared</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-262">63</span><span class="sxs-lookup"><span data-stu-id="3eaca-262">63</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-263">HP-</span><span class="sxs-lookup"><span data-stu-id="3eaca-263">HP-HIL</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-264">64</span><span class="sxs-lookup"><span data-stu-id="3eaca-264">64</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-265">Access. bus</span><span class="sxs-lookup"><span data-stu-id="3eaca-265">Access.bus</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-266">65</span><span class="sxs-lookup"><span data-stu-id="3eaca-266">65</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-267">NuBus</span><span class="sxs-lookup"><span data-stu-id="3eaca-267">NuBus</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-268">66</span><span class="sxs-lookup"><span data-stu-id="3eaca-268">66</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-269">Centronics</span><span class="sxs-lookup"><span data-stu-id="3eaca-269">Centronics</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-270">67</span><span class="sxs-lookup"><span data-stu-id="3eaca-270">67</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-271">Mini-Centronics</span><span class="sxs-lookup"><span data-stu-id="3eaca-271">Mini-Centronics</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-272">68</span><span class="sxs-lookup"><span data-stu-id="3eaca-272">68</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-273">Tipo Mini-Centronics-14</span><span class="sxs-lookup"><span data-stu-id="3eaca-273">Mini-Centronics Type-14</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-274">69</span><span class="sxs-lookup"><span data-stu-id="3eaca-274">69</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-275">Tipo Mini-Centronics-20</span><span class="sxs-lookup"><span data-stu-id="3eaca-275">Mini-Centronics Type-20</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-276">70</span><span class="sxs-lookup"><span data-stu-id="3eaca-276">70</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-277">Tipo Mini-Centronics-26</span><span class="sxs-lookup"><span data-stu-id="3eaca-277">Mini-Centronics Type-26</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-278">71</span><span class="sxs-lookup"><span data-stu-id="3eaca-278">71</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-279">Mouse bus</span><span class="sxs-lookup"><span data-stu-id="3eaca-279">Bus Mouse</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-280">72</span><span class="sxs-lookup"><span data-stu-id="3eaca-280">72</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-281">ADB</span><span class="sxs-lookup"><span data-stu-id="3eaca-281">ADB</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-282">73</span><span class="sxs-lookup"><span data-stu-id="3eaca-282">73</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-283">AGP</span><span class="sxs-lookup"><span data-stu-id="3eaca-283">AGP</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-284">74</span><span class="sxs-lookup"><span data-stu-id="3eaca-284">74</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-285">Bus VME</span><span class="sxs-lookup"><span data-stu-id="3eaca-285">VME Bus</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-286">75</span><span class="sxs-lookup"><span data-stu-id="3eaca-286">75</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-287">VME64</span><span class="sxs-lookup"><span data-stu-id="3eaca-287">VME64</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-288">76</span><span class="sxs-lookup"><span data-stu-id="3eaca-288">76</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-289">Proprietario</span><span class="sxs-lookup"><span data-stu-id="3eaca-289">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-290">77</span><span class="sxs-lookup"><span data-stu-id="3eaca-290">77</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-291">Slot scheda processore proprietario</span><span class="sxs-lookup"><span data-stu-id="3eaca-291">Proprietary Processor Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-292">78</span><span class="sxs-lookup"><span data-stu-id="3eaca-292">78</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-293">Slot scheda di memoria proprietaria</span><span class="sxs-lookup"><span data-stu-id="3eaca-293">Proprietary Memory Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-294">79</span><span class="sxs-lookup"><span data-stu-id="3eaca-294">79</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-295">Slot di riser I/O proprietario</span><span class="sxs-lookup"><span data-stu-id="3eaca-295">Proprietary I/O Riser Slot</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-296">80</span><span class="sxs-lookup"><span data-stu-id="3eaca-296">80</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-297">PCI-66MHZ</span><span class="sxs-lookup"><span data-stu-id="3eaca-297">PCI-66MHZ</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-298">81</span><span class="sxs-lookup"><span data-stu-id="3eaca-298">81</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-299">AGP2X</span><span class="sxs-lookup"><span data-stu-id="3eaca-299">AGP2X</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-300">82</span><span class="sxs-lookup"><span data-stu-id="3eaca-300">82</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-301">AGP4X</span><span class="sxs-lookup"><span data-stu-id="3eaca-301">AGP4X</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-302">83</span><span class="sxs-lookup"><span data-stu-id="3eaca-302">83</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-303">PC-98</span><span class="sxs-lookup"><span data-stu-id="3eaca-303">PC-98</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-304">84</span><span class="sxs-lookup"><span data-stu-id="3eaca-304">84</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-305">PC-98-Hireso</span><span class="sxs-lookup"><span data-stu-id="3eaca-305">PC-98-Hireso</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-306">85</span><span class="sxs-lookup"><span data-stu-id="3eaca-306">85</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-307">PC-H98</span><span class="sxs-lookup"><span data-stu-id="3eaca-307">PC-H98</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-308">86</span><span class="sxs-lookup"><span data-stu-id="3eaca-308">86</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-309">PC-98Note</span><span class="sxs-lookup"><span data-stu-id="3eaca-309">PC-98Note</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-310">87</span><span class="sxs-lookup"><span data-stu-id="3eaca-310">87</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-311">PC-98Full</span><span class="sxs-lookup"><span data-stu-id="3eaca-311">PC-98Full</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-312">88</span><span class="sxs-lookup"><span data-stu-id="3eaca-312">88</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-313">SCSI SSA</span><span class="sxs-lookup"><span data-stu-id="3eaca-313">SSA SCSI</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-314">89</span><span class="sxs-lookup"><span data-stu-id="3eaca-314">89</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-315">Circolare</span><span class="sxs-lookup"><span data-stu-id="3eaca-315">Circular</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-316">90</span><span class="sxs-lookup"><span data-stu-id="3eaca-316">90</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-317">Connettore IDE a bordo</span><span class="sxs-lookup"><span data-stu-id="3eaca-317">On Board IDE Connector</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-318">91</span><span class="sxs-lookup"><span data-stu-id="3eaca-318">91</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-319">Connettore floppy a bordo</span><span class="sxs-lookup"><span data-stu-id="3eaca-319">On Board Floppy Connector</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-320">92</span><span class="sxs-lookup"><span data-stu-id="3eaca-320">92</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-321">2 pin doppio inline</span><span class="sxs-lookup"><span data-stu-id="3eaca-321">9 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-322">93</span><span class="sxs-lookup"><span data-stu-id="3eaca-322">93</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-323">25 pin doppio inline</span><span class="sxs-lookup"><span data-stu-id="3eaca-323">25 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-324">94</span><span class="sxs-lookup"><span data-stu-id="3eaca-324">94</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-325">Pin 50 dual inline</span><span class="sxs-lookup"><span data-stu-id="3eaca-325">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-326">95</span><span class="sxs-lookup"><span data-stu-id="3eaca-326">95</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-327">Pin 68 dual inline</span><span class="sxs-lookup"><span data-stu-id="3eaca-327">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-328">96</span><span class="sxs-lookup"><span data-stu-id="3eaca-328">96</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-329">Connettore audio a bordo</span><span class="sxs-lookup"><span data-stu-id="3eaca-329">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-330">97</span><span class="sxs-lookup"><span data-stu-id="3eaca-330">97</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-331">Mini-Jack</span><span class="sxs-lookup"><span data-stu-id="3eaca-331">Mini-jack</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-332">98</span><span class="sxs-lookup"><span data-stu-id="3eaca-332">98</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-333">PCI-X</span><span class="sxs-lookup"><span data-stu-id="3eaca-333">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-334">99</span><span class="sxs-lookup"><span data-stu-id="3eaca-334">99</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-335">SBus IEEE 1396-1993 32 bit</span><span class="sxs-lookup"><span data-stu-id="3eaca-335">Sbus IEEE 1396-1993 32 bit</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-336">100</span><span class="sxs-lookup"><span data-stu-id="3eaca-336">100</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-337">SBus IEEE 1396-1993 64 bit</span><span class="sxs-lookup"><span data-stu-id="3eaca-337">Sbus IEEE 1396-1993 64 bit</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-338">101</span><span class="sxs-lookup"><span data-stu-id="3eaca-338">101</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-339">Contratto del cliente Microsoft</span><span class="sxs-lookup"><span data-stu-id="3eaca-339">MCA</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-340">102</span><span class="sxs-lookup"><span data-stu-id="3eaca-340">102</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-341">GIO</span><span class="sxs-lookup"><span data-stu-id="3eaca-341">GIO</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-342">103</span><span class="sxs-lookup"><span data-stu-id="3eaca-342">103</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-343">XIO</span><span class="sxs-lookup"><span data-stu-id="3eaca-343">XIO</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-344">104</span><span class="sxs-lookup"><span data-stu-id="3eaca-344">104</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-345">HIO</span><span class="sxs-lookup"><span data-stu-id="3eaca-345">HIO</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-346">105</span><span class="sxs-lookup"><span data-stu-id="3eaca-346">105</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-347">NGIO</span><span class="sxs-lookup"><span data-stu-id="3eaca-347">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-348">106</span><span class="sxs-lookup"><span data-stu-id="3eaca-348">106</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-349">PMC</span><span class="sxs-lookup"><span data-stu-id="3eaca-349">PMC</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-350">107</span><span class="sxs-lookup"><span data-stu-id="3eaca-350">107</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-351">MTRJ</span><span class="sxs-lookup"><span data-stu-id="3eaca-351">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-352">108</span><span class="sxs-lookup"><span data-stu-id="3eaca-352">108</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-353">VF-45</span><span class="sxs-lookup"><span data-stu-id="3eaca-353">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-354">109</span><span class="sxs-lookup"><span data-stu-id="3eaca-354">109</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-355">I/O futuro</span><span class="sxs-lookup"><span data-stu-id="3eaca-355">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-356">110</span><span class="sxs-lookup"><span data-stu-id="3eaca-356">110</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-357">SC</span><span class="sxs-lookup"><span data-stu-id="3eaca-357">SC</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-358">111</span><span class="sxs-lookup"><span data-stu-id="3eaca-358">111</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-359">SG</span><span class="sxs-lookup"><span data-stu-id="3eaca-359">SG</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-360">112</span><span class="sxs-lookup"><span data-stu-id="3eaca-360">112</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-361">Electrical</span><span class="sxs-lookup"><span data-stu-id="3eaca-361">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-362">113</span><span class="sxs-lookup"><span data-stu-id="3eaca-362">113</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-363">Ottico</span><span class="sxs-lookup"><span data-stu-id="3eaca-363">Optical</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-364">114</span><span class="sxs-lookup"><span data-stu-id="3eaca-364">114</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-365">Barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="3eaca-365">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-366">115</span><span class="sxs-lookup"><span data-stu-id="3eaca-366">115</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-367">GLM</span><span class="sxs-lookup"><span data-stu-id="3eaca-367">GLM</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-368">116</span><span class="sxs-lookup"><span data-stu-id="3eaca-368">116</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-369">1x9</span><span class="sxs-lookup"><span data-stu-id="3eaca-369">1x9</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-370">117</span><span class="sxs-lookup"><span data-stu-id="3eaca-370">117</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-371">Mini SG</span><span class="sxs-lookup"><span data-stu-id="3eaca-371">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-372">118</span><span class="sxs-lookup"><span data-stu-id="3eaca-372">118</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-373">LC</span><span class="sxs-lookup"><span data-stu-id="3eaca-373">LC</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-374">119</span><span class="sxs-lookup"><span data-stu-id="3eaca-374">119</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-375">HSSC</span><span class="sxs-lookup"><span data-stu-id="3eaca-375">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-376">120</span><span class="sxs-lookup"><span data-stu-id="3eaca-376">120</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-377">Schermate VHDCI (68 pin)</span><span class="sxs-lookup"><span data-stu-id="3eaca-377">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-378">121</span><span class="sxs-lookup"><span data-stu-id="3eaca-378">121</span></span>
</dt> <dd>

<span data-ttu-id="3eaca-379">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="3eaca-379">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3eaca-380">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3eaca-380">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-381">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-383">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3eaca-383">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-384">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="3eaca-384">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3eaca-385">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="3eaca-385">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3eaca-386">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-386">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-387">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3eaca-387">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-388">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-389">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-390">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="3eaca-390">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-391">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3eaca-391">Textual description of the object.</span></span>

<span data-ttu-id="3eaca-392">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-393">**HeightAllowed**</span><span class="sxs-lookup"><span data-stu-id="3eaca-393">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-394">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="3eaca-394">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-395">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-396">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="3eaca-396">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-397">Altezza massima, in pollici, di una scheda adattatore che può essere inserita nello slot.</span><span class="sxs-lookup"><span data-stu-id="3eaca-397">Maximum height, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-398">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3eaca-398">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-399">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3eaca-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-401">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="3eaca-401">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-402">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3eaca-402">Date and time the object was installed.</span></span> <span data-ttu-id="3eaca-403">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="3eaca-403">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3eaca-404">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-404">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-405">**LengthAllowed**</span><span class="sxs-lookup"><span data-stu-id="3eaca-405">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-406">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="3eaca-406">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-408">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="3eaca-408">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-409">Lunghezza massima, in pollici, di una scheda adattatore che può essere inserita nello slot.</span><span class="sxs-lookup"><span data-stu-id="3eaca-409">Maximum length, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-410">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="3eaca-410">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-411">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-411">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-412">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-413">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3eaca-413">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-414">Organizzazione che ha prodotto l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="3eaca-414">Organization that produced the physical element.</span></span> <span data-ttu-id="3eaca-415">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-415">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="3eaca-416">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-416">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-417">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="3eaca-417">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-418">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3eaca-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-420">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Slot \| 004,3 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="3eaca-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-421">Larghezza massima del bus, in bit, delle schede di scheda che possono essere inserite nello slot.</span><span class="sxs-lookup"><span data-stu-id="3eaca-421">Maximum bus width, in bits, of adapter cards that can be inserted into the slot.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="3eaca-422">**8** (0)</span><span class="sxs-lookup"><span data-stu-id="3eaca-422">**8** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="3eaca-423">**16** (1)</span><span class="sxs-lookup"><span data-stu-id="3eaca-423">**16** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="3eaca-424">**32** (2)</span><span class="sxs-lookup"><span data-stu-id="3eaca-424">**32** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="64"></span>

<span data-ttu-id="3eaca-425">**64** (3)</span><span class="sxs-lookup"><span data-stu-id="3eaca-425">**64** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="128"></span>

<span data-ttu-id="3eaca-426">**128** (4)</span><span class="sxs-lookup"><span data-stu-id="3eaca-426">**128** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3eaca-427">**Modello**</span><span class="sxs-lookup"><span data-stu-id="3eaca-427">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-428">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-430">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3eaca-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-431">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="3eaca-431">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="3eaca-432">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-432">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-433">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3eaca-433">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-434">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-435">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-436">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="3eaca-436">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-437">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="3eaca-437">Label by which the object is known.</span></span> <span data-ttu-id="3eaca-438">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="3eaca-438">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="3eaca-439">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-440">**Number**</span><span class="sxs-lookup"><span data-stu-id="3eaca-440">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-441">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3eaca-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-442">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-443">Numero di slot fisico, che può essere usato come indice in una tabella degli slot di sistema, per determinare se lo slot è fisicamente occupato.</span><span class="sxs-lookup"><span data-stu-id="3eaca-443">Physical slot number, which can be used as an index into a system slot table, to determine whether the slot is physically occupied.</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-444">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="3eaca-444">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-445">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-447">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="3eaca-447">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="3eaca-448">Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset.</span><span class="sxs-lookup"><span data-stu-id="3eaca-448">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="3eaca-449">Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="3eaca-449">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="3eaca-450">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-450">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-451">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="3eaca-451">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-452">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-454">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3eaca-454">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-455">Numero di parte assegnato dall'organizzazione che ha prodotto o prodotto l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="3eaca-455">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="3eaca-456">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-456">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-457">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="3eaca-457">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-458">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3eaca-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-459">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-460">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="3eaca-460">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="3eaca-461">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-461">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-462">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="3eaca-462">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-463">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-464">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-465">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ slot**.**SpecialPurpose**")</span><span class="sxs-lookup"><span data-stu-id="3eaca-465">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-466">Stringa in formato libero che descrive il modo in cui questo slot è fisicamente univoco e può mantenere tipi speciali di hardware.</span><span class="sxs-lookup"><span data-stu-id="3eaca-466">Free-form string that describes how this slot is physically unique and that it may hold special types of hardware.</span></span> <span data-ttu-id="3eaca-467">Questa proprietà ha un significato solo quando la proprietà booleana **SpecialPurpose** corrispondente è impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="3eaca-467">This property only has meaning when the corresponding Boolean **SpecialPurpose** property is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-468">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="3eaca-468">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-469">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-470">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-471">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3eaca-471">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-472">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="3eaca-472">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="3eaca-473">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-473">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-474">**SKU**</span><span class="sxs-lookup"><span data-stu-id="3eaca-474">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-475">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-476">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-477">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3eaca-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-478">Numero di unità per l'elemento fisico che mantiene le scorte.</span><span class="sxs-lookup"><span data-stu-id="3eaca-478">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="3eaca-479">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-479">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-480">**SpecialPurpose**</span><span class="sxs-lookup"><span data-stu-id="3eaca-480">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-481">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3eaca-481">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-482">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-483">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ slot**.**PurposeDescription**")</span><span class="sxs-lookup"><span data-stu-id="3eaca-483">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-484">Se **true**, lo slot è fisicamente univoco e può ospitare tipi speciali di hardware, ad esempio uno slot del processore di grafica.</span><span class="sxs-lookup"><span data-stu-id="3eaca-484">If **TRUE**, the slot is physically unique and may hold special types of hardware, (for example, a graphics processor slot).</span></span> <span data-ttu-id="3eaca-485">Se **true**, la proprietà **PurposeDescription** deve specificare il modo in cui lo slot è univoco o lo scopo dello slot.</span><span class="sxs-lookup"><span data-stu-id="3eaca-485">If **TRUE**, the **PurposeDescription** property should specify how the slot is unique or the slot's purpose.</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-486">**Status**</span><span class="sxs-lookup"><span data-stu-id="3eaca-486">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-487">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-488">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-489">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="3eaca-489">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-490">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3eaca-490">Current status of the object.</span></span> <span data-ttu-id="3eaca-491">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-491">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3eaca-492">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3eaca-492">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3eaca-493">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3eaca-493">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3eaca-494">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="3eaca-494">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3eaca-495">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="3eaca-495">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3eaca-496">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="3eaca-496">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3eaca-497">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="3eaca-497">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3eaca-498">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="3eaca-498">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3eaca-499">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="3eaca-499">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3eaca-500">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="3eaca-500">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3eaca-501">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="3eaca-501">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3eaca-502">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="3eaca-502">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3eaca-503">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="3eaca-503">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3eaca-504">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="3eaca-504">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3eaca-505">**SupportsHotPlug**</span><span class="sxs-lookup"><span data-stu-id="3eaca-505">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-506">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3eaca-506">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-507">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-508">Se **true**, lo slot supporta il collegamento a caldo delle schede degli adapter.</span><span class="sxs-lookup"><span data-stu-id="3eaca-508">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-509">**Tag**</span><span class="sxs-lookup"><span data-stu-id="3eaca-509">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-510">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-511">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-512">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3eaca-512">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-513">Stringa arbitraria che identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3eaca-513">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="3eaca-514">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="3eaca-514">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="3eaca-515">La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="3eaca-515">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="3eaca-516">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="3eaca-516">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="3eaca-517">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="3eaca-517">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="3eaca-518">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="3eaca-518">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="3eaca-519">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-519">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-520">**ThermalRating**</span><span class="sxs-lookup"><span data-stu-id="3eaca-520">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-521">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3eaca-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-522">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-523">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Slot di sistema DMTF \| 004,11 "), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatt ")</span><span class="sxs-lookup"><span data-stu-id="3eaca-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-524">Dissipazione termica massima dello slot, in milliwatt.</span><span class="sxs-lookup"><span data-stu-id="3eaca-524">Maximum thermal dissipation of the slot, in milliwatts.</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-525">**VccMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="3eaca-525">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-526">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3eaca-526">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-527">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-528">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Slot di sistema DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="3eaca-528">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-529">Tensione Vcc supportata dallo slot.</span><span class="sxs-lookup"><span data-stu-id="3eaca-529">Vcc voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3eaca-530">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3eaca-530">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3eaca-531">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="3eaca-531">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="3eaca-532">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="3eaca-532">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="3eaca-533">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="3eaca-533">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3eaca-534">**Versione**</span><span class="sxs-lookup"><span data-stu-id="3eaca-534">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-535">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3eaca-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-536">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-537">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3eaca-537">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-538">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="3eaca-538">Version of the physical element.</span></span>

<span data-ttu-id="3eaca-539">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-539">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3eaca-540">**VppMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="3eaca-540">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3eaca-541">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3eaca-541">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-542">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3eaca-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3eaca-543">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Slot di sistema DMTF \| 004,10 ")</span><span class="sxs-lookup"><span data-stu-id="3eaca-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="3eaca-544">Tensione VPP supportata dallo slot.</span><span class="sxs-lookup"><span data-stu-id="3eaca-544">Vpp voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3eaca-545">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="3eaca-545">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3eaca-546">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="3eaca-546">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="3eaca-547">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="3eaca-547">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="3eaca-548">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="3eaca-548">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="3eaca-549">**12V** (4)</span><span class="sxs-lookup"><span data-stu-id="3eaca-549">**12V** (4)</span></span>


<span data-ttu-id="3eaca-550"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3eaca-550"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="3eaca-551">Commenti</span><span class="sxs-lookup"><span data-stu-id="3eaca-551">Remarks</span></span>

<span data-ttu-id="3eaca-552">La classe di **\_ slot CIM** è derivata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-552">The **CIM\_Slot** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="3eaca-553">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="3eaca-553">WMI does not implement this class.</span></span> <span data-ttu-id="3eaca-554">Per le classi WMI derivate dallo **\_ slot CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3eaca-554">For WMI classes derived from **CIM\_Slot**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3eaca-555">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="3eaca-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3eaca-556">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="3eaca-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eaca-557">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3eaca-557">Requirements</span></span>



| <span data-ttu-id="3eaca-558">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eaca-558">Requirement</span></span> | <span data-ttu-id="3eaca-559">Valore</span><span class="sxs-lookup"><span data-stu-id="3eaca-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3eaca-560">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3eaca-560">Minimum supported client</span></span><br/> | <span data-ttu-id="3eaca-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eaca-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3eaca-562">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3eaca-562">Minimum supported server</span></span><br/> | <span data-ttu-id="3eaca-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3eaca-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3eaca-564">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3eaca-564">Namespace</span></span><br/>                | <span data-ttu-id="3eaca-565">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3eaca-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3eaca-566">MOF</span><span class="sxs-lookup"><span data-stu-id="3eaca-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3eaca-567"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3eaca-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3eaca-568">DLL</span><span class="sxs-lookup"><span data-stu-id="3eaca-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3eaca-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3eaca-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eaca-570">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3eaca-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eaca-571">**\_PHYSICALCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3eaca-571">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> </dl>

 

