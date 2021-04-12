---
description: Una \_ classe CIM ComputerSystem rappresenta una raccolta speciale di istanze CIM di \_ ManagedSystemElement.
ms.assetid: c4fd0598-3cb3-428f-ad39-a14232ef7c17
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystem (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.Caption
- CIM_ComputerSystem.Description
- CIM_ComputerSystem.InstallDate
- CIM_ComputerSystem.Status
- CIM_ComputerSystem.CreationClassName
- CIM_ComputerSystem.Name
- CIM_ComputerSystem.PrimaryOwnerContact
- CIM_ComputerSystem.PrimaryOwnerName
- CIM_ComputerSystem.Roles
- CIM_ComputerSystem.NameFormat
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4645a8d4b2440b0b102658d3eca74d825d774dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483533"
---
# <a name="cim_computersystem-class-cimwin32-wmi-providers"></a><span data-ttu-id="4a064-103">Classe CIM_ComputerSystem (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="4a064-103">CIM_ComputerSystem class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="4a064-104">Una classe **CIM \_ ComputerSystem** rappresenta una raccolta speciale di istanze [**CIM di \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="4a064-104">A **CIM\_ComputerSystem** class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="4a064-105">Questa raccolta fornisce funzionalità del computer e funge da punto di aggregazione per associare uno o più degli elementi seguenti: file system, sistema operativo, processore e memoria (archiviazione volatile e non volatile).</span><span class="sxs-lookup"><span data-stu-id="4a064-105">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="4a064-106">Questa classe è derivata dal [**\_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4a064-106">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a064-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4a064-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4a064-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4a064-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4a064-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4a064-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4a064-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="4a064-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a064-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a064-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C525-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
  string   NameFormat;
};
```

## <a name="members"></a><span data-ttu-id="4a064-112">Members</span><span class="sxs-lookup"><span data-stu-id="4a064-112">Members</span></span>

<span data-ttu-id="4a064-113">La classe **CIM \_ ComputerSystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4a064-113">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="4a064-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4a064-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4a064-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4a064-115">Properties</span></span>

<span data-ttu-id="4a064-116">La classe **CIM \_ ComputerSystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4a064-116">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4a064-117">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="4a064-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a064-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a064-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a064-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a064-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a064-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4a064-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4a064-121">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4a064-121">A short textual description of the object.</span></span>

<span data-ttu-id="4a064-122">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4a064-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a064-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4a064-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a064-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a064-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a064-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a064-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a064-126">Qualificatori: [ **\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4a064-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4a064-127">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="4a064-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4a064-128">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="4a064-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4a064-129">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4a064-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a064-130">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="4a064-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a064-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a064-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a064-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a064-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a064-133">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4a064-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4a064-134">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4a064-134">A textual description of the object.</span></span>

<span data-ttu-id="4a064-135">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4a064-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a064-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4a064-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a064-137">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4a064-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4a064-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a064-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a064-139">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="4a064-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4a064-140">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="4a064-140">Indicates when the object was installed.</span></span> <span data-ttu-id="4a064-141">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="4a064-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4a064-142">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4a064-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a064-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4a064-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a064-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a064-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a064-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a064-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a064-146">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4a064-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4a064-147">Definisce l'etichetta in base alla quale l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="4a064-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="4a064-148">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4a064-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a064-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="4a064-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a064-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a064-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a064-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a064-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a064-152">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="4a064-152">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="4a064-153">Identifica il modo in cui viene generato il nome del sistema del computer, utilizzando un approccio euristico.</span><span class="sxs-lookup"><span data-stu-id="4a064-153">Identifies how the computer system name is generated, using a heuristic.</span></span> <span data-ttu-id="4a064-154">L'euristica è descritta in dettaglio nella specifica del modello comune CIM V2.</span><span class="sxs-lookup"><span data-stu-id="4a064-154">The heuristic is outlined, in detail, in the CIM V2 Common Model specification.</span></span> <span data-ttu-id="4a064-155">Si presuppone che le regole documentate vengano attraversate nell'ordine, per determinare e assegnare un nome.</span><span class="sxs-lookup"><span data-stu-id="4a064-155">It assumes that the documented rules are traversed in order, to determine and assign a name.</span></span> <span data-ttu-id="4a064-156">L'elenco di valori **NameFormat** definisce l'ordine di precedenza per l'assegnazione del nome del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="4a064-156">The **NameFormat** values list defines the precedence order for assigning the computer system name.</span></span> <span data-ttu-id="4a064-157">Diverse regole eseguono il mapping allo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="4a064-157">Several rules do map to the same Value.</span></span>

<span data-ttu-id="4a064-158">Si noti che il **nome** dell'oggetto viene calcolato utilizzando l'euristica è il valore della chiave del sistema.</span><span class="sxs-lookup"><span data-stu-id="4a064-158">Note that the object's **Name** is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="4a064-159">Gli altri nomi possono essere assegnati e usati per l'oggetto più adatto all'azienda, usando gli alias.</span><span class="sxs-lookup"><span data-stu-id="4a064-159">Other names can be assigned and used for the object that better suit the business, using Aliases.</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="4a064-160">**IP** ("IP")</span><span class="sxs-lookup"><span data-stu-id="4a064-160">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="4a064-161">**Dial** ("dial")</span><span class="sxs-lookup"><span data-stu-id="4a064-161">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="4a064-162">**HID** ("HID")</span><span class="sxs-lookup"><span data-stu-id="4a064-162">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="4a064-163">**NWA** ("NWA")</span><span class="sxs-lookup"><span data-stu-id="4a064-163">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="4a064-164">**Hwa** ("Hwa")</span><span class="sxs-lookup"><span data-stu-id="4a064-164">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="4a064-165">**X25** ("x25")</span><span class="sxs-lookup"><span data-stu-id="4a064-165">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="4a064-166">**ISDN** ("ISDN")</span><span class="sxs-lookup"><span data-stu-id="4a064-166">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="4a064-167">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="4a064-167">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="4a064-168">**DCC** ("DCC")</span><span class="sxs-lookup"><span data-stu-id="4a064-168">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="4a064-169">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="4a064-169">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="4a064-170">**E. 164** ("e. 164")</span><span class="sxs-lookup"><span data-stu-id="4a064-170">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="4a064-171">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="4a064-171">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="4a064-172">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="4a064-172">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4a064-173">**Altro** ("altro")</span><span class="sxs-lookup"><span data-stu-id="4a064-173">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4a064-174">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="4a064-174">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a064-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a064-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a064-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a064-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a064-177">Come è possibile raggiungere il proprietario del sistema primario (ad esempio, il numero di telefono o l'indirizzo di posta elettronica).</span><span class="sxs-lookup"><span data-stu-id="4a064-177">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="4a064-178">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4a064-178">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a064-179">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="4a064-179">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a064-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a064-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a064-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a064-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a064-182">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4a064-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4a064-183">Nome del proprietario del sistema primario.</span><span class="sxs-lookup"><span data-stu-id="4a064-183">Name of the primary system owner.</span></span>

<span data-ttu-id="4a064-184">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4a064-184">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a064-185">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="4a064-185">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a064-186">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4a064-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4a064-187">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4a064-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4a064-188">Ruoli riprodotti dal sistema nell'ambiente Information Technology.</span><span class="sxs-lookup"><span data-stu-id="4a064-188">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="4a064-189">Le sottoclassi del sistema possono eseguire l'override di questa proprietà per definire valori di ruolo espliciti.</span><span class="sxs-lookup"><span data-stu-id="4a064-189">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="4a064-190">In alternativa, un gruppo di lavoro può descrivere l'euristica, le convenzioni e le linee guida per specificare i ruoli.</span><span class="sxs-lookup"><span data-stu-id="4a064-190">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="4a064-191">Per un'istanza di un sistema di rete, ad esempio, questa proprietà potrebbe contenere la stringa "switch" o "Bridge".</span><span class="sxs-lookup"><span data-stu-id="4a064-191">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="4a064-192">Questa proprietà viene ereditata [**dal \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4a064-192">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a064-193">**Status**</span><span class="sxs-lookup"><span data-stu-id="4a064-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a064-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4a064-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a064-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4a064-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a064-196">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="4a064-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4a064-197">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4a064-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="4a064-198">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="4a064-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4a064-199">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="4a064-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4a064-200">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="4a064-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4a064-201">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="4a064-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4a064-202">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="4a064-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4a064-203">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="4a064-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4a064-204">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4a064-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4a064-205">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="4a064-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4a064-206">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="4a064-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4a064-207">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="4a064-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4a064-208">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="4a064-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4a064-209">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="4a064-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4a064-210">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="4a064-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4a064-211">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="4a064-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4a064-212">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="4a064-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4a064-213">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="4a064-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4a064-214">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="4a064-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4a064-215">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="4a064-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4a064-216">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="4a064-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4a064-217">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="4a064-217">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="4a064-218"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4a064-218"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="4a064-219">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a064-219">Remarks</span></span>

<span data-ttu-id="4a064-220">La classe **CIM \_ ComputerSystem** è derivata dal [**\_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="4a064-220">The **CIM\_ComputerSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="4a064-221">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="4a064-221">WMI does not implement this class.</span></span> <span data-ttu-id="4a064-222">Per ulteriori informazioni sulle classi derivate da **CIM \_ ComputerSystem**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4a064-222">For more information about classes derived from **CIM\_ComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4a064-223">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4a064-223">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4a064-224">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4a064-224">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a064-225">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a064-225">Requirements</span></span>



| <span data-ttu-id="4a064-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a064-226">Requirement</span></span> | <span data-ttu-id="4a064-227">Valore</span><span class="sxs-lookup"><span data-stu-id="4a064-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a064-228">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a064-228">Minimum supported client</span></span><br/> | <span data-ttu-id="4a064-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a064-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a064-230">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a064-230">Minimum supported server</span></span><br/> | <span data-ttu-id="4a064-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a064-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a064-232">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4a064-232">Namespace</span></span><br/>                | <span data-ttu-id="4a064-233">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4a064-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4a064-234">MOF</span><span class="sxs-lookup"><span data-stu-id="4a064-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a064-235"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a064-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a064-236">DLL</span><span class="sxs-lookup"><span data-stu-id="4a064-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a064-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a064-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a064-238">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a064-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a064-239">**\_Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="4a064-239">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

