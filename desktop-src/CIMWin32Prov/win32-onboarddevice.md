---
description: La \_ classe WMI OnBoardDevice Win32 rappresenta i dispositivi Adapter comuni incorporati nella scheda madre (scheda di sistema).
ms.assetid: 6fac38b4-7c04-4f64-997d-40bcbf767959
ms.tgt_platform: multiple
title: Classe Win32_OnBoardDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OnBoardDevice
- Win32_OnBoardDevice.Caption
- Win32_OnBoardDevice.CreationClassName
- Win32_OnBoardDevice.Description
- Win32_OnBoardDevice.DeviceType
- Win32_OnBoardDevice.Enabled
- Win32_OnBoardDevice.HotSwappable
- Win32_OnBoardDevice.InstallDate
- Win32_OnBoardDevice.Manufacturer
- Win32_OnBoardDevice.Model
- Win32_OnBoardDevice.Name
- Win32_OnBoardDevice.OtherIdentifyingInfo
- Win32_OnBoardDevice.PartNumber
- Win32_OnBoardDevice.PoweredOn
- Win32_OnBoardDevice.Removable
- Win32_OnBoardDevice.Replaceable
- Win32_OnBoardDevice.SerialNumber
- Win32_OnBoardDevice.SKU
- Win32_OnBoardDevice.Status
- Win32_OnBoardDevice.Tag
- Win32_OnBoardDevice.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5fae5416a4b3cbeda0d8c63f6834c0406e628013
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225765"
---
# <a name="win32_onboarddevice-class"></a><span data-ttu-id="3a982-103">Win32 \_ OnBoardDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="3a982-103">Win32\_OnBoardDevice class</span></span>

<span data-ttu-id="3a982-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ OnBoardDevice Win32** rappresenta i dispositivi Adapter comuni incorporati nella scheda madre (scheda di sistema).</span><span class="sxs-lookup"><span data-stu-id="3a982-104">The **Win32\_OnBoardDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents common adapter devices built into the motherboard (system board).</span></span>

<span data-ttu-id="3a982-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3a982-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3a982-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3a982-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a982-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a982-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{AEECF151-D0EA-11d2-ABFC-00805F538618}"), AMENDMENT]
class Win32_OnBoardDevice : CIM_PhysicalComponent
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  uint16   DeviceType;
  boolean  Enabled;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="3a982-108">Members</span><span class="sxs-lookup"><span data-stu-id="3a982-108">Members</span></span>

<span data-ttu-id="3a982-109">La classe **Win32 \_ OnBoardDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3a982-109">The **Win32\_OnBoardDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="3a982-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3a982-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a982-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3a982-111">Properties</span></span>

<span data-ttu-id="3a982-112">La classe **Win32 \_ OnBoardDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3a982-112">The **Win32\_OnBoardDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a982-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="3a982-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-116">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3a982-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3a982-117">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3a982-117">Short description of the object.</span></span>

<span data-ttu-id="3a982-118">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3a982-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-122">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="3a982-122">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3a982-123">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="3a982-123">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="3a982-124">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="3a982-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3a982-125">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-125">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-126">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3a982-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-129">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 10 \| Description")</span><span class="sxs-lookup"><span data-stu-id="3a982-129">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="3a982-130">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3a982-130">Description of the object.</span></span>

<span data-ttu-id="3a982-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-132">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="3a982-132">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-133">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a982-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-135">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 10 \| dispositivo tipo n")</span><span class="sxs-lookup"><span data-stu-id="3a982-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Type n")</span></span>
</dt> </dl>

<span data-ttu-id="3a982-136">Tipo di dispositivo rappresentato.</span><span class="sxs-lookup"><span data-stu-id="3a982-136">Type of device being represented.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3a982-137">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="3a982-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a982-138">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="3a982-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="3a982-139">**Video** (3)</span><span class="sxs-lookup"><span data-stu-id="3a982-139">**Video** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Controller"></span><span id="scsi_controller"></span><span id="SCSI_CONTROLLER"></span>

<span data-ttu-id="3a982-140">**Controller SCSI** (4)</span><span class="sxs-lookup"><span data-stu-id="3a982-140">**SCSI Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="3a982-141">**Ethernet** (5)</span><span class="sxs-lookup"><span data-stu-id="3a982-141">**Ethernet** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="3a982-142">**Token ring** (6)</span><span class="sxs-lookup"><span data-stu-id="3a982-142">**Token Ring** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Sound"></span><span id="sound"></span><span id="SOUND"></span>

<span data-ttu-id="3a982-143">**Audio** (7)</span><span class="sxs-lookup"><span data-stu-id="3a982-143">**Sound** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a982-144">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="3a982-144">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-145">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3a982-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-147">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 10 \| dispositivo stato n")</span><span class="sxs-lookup"><span data-stu-id="3a982-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Status n")</span></span>
</dt> </dl>

<span data-ttu-id="3a982-148">Se **true**, il dispositivo di bordo è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="3a982-148">If **TRUE**, the on-board device is available for use.</span></span>

</dd> <dt>

<span data-ttu-id="3a982-149">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="3a982-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-150">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3a982-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a982-152">Se **true**, un pacchetto fisico può essere scambiato a caldo (se è possibile sostituire l'elemento con un oggetto fisicamente diverso ma equivalente mentre al pacchetto che lo contiene è stata applicata una potenza).</span><span class="sxs-lookup"><span data-stu-id="3a982-152">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="3a982-153">Ad esempio, un pacchetto di unità disco inserito usando i connettori SCA è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="3a982-153">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="3a982-154">Tutti i pacchetti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="3a982-154">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="3a982-155">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-155">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3a982-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-157">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a982-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-159">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="3a982-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3a982-160">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3a982-160">Date and time the object was installed.</span></span> <span data-ttu-id="3a982-161">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="3a982-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3a982-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-163">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="3a982-163">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-166">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="3a982-166">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3a982-167">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="3a982-167">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="3a982-168">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-168">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-169">**Modello**</span><span class="sxs-lookup"><span data-stu-id="3a982-169">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-172">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="3a982-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3a982-173">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="3a982-173">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="3a982-174">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-175">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3a982-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-178">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="3a982-178">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3a982-179">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="3a982-179">Label by which the object is known.</span></span> <span data-ttu-id="3a982-180">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="3a982-180">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="3a982-181">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-182">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="3a982-182">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a982-185">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="3a982-185">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="3a982-186">Un esempio è costituito dai dati del codice a barre associati a un elemento che dispone anche di un tag asset.</span><span class="sxs-lookup"><span data-stu-id="3a982-186">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="3a982-187">Si noti che se sono disponibili solo i dati del codice a barre ed è univoco o in grado di essere utilizzati come chiave dell'elemento, questa proprietà sarà **null** e i dati del codice a barre verranno utilizzati come chiave della classe nella proprietà Tag.</span><span class="sxs-lookup"><span data-stu-id="3a982-187">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="3a982-188">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-188">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-189">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="3a982-189">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-192">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="3a982-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3a982-193">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="3a982-193">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="3a982-194">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-195">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="3a982-195">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-196">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3a982-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a982-198">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="3a982-198">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="3a982-199">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-199">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-200">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="3a982-200">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-201">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3a982-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a982-203">Se il valore è **true**, un pacchetto fisico è rimovibile (se è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti).</span><span class="sxs-lookup"><span data-stu-id="3a982-203">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="3a982-204">Un pacchetto può ancora essere rimovibile se l'alimentazione deve essere "off" per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="3a982-204">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="3a982-205">Se Power può essere "on" e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="3a982-205">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="3a982-206">Ad esempio, una batteria aggiuntiva in un portatile è rimovibile, così come un pacchetto di unità disco inserito usando i connettori SCA.</span><span class="sxs-lookup"><span data-stu-id="3a982-206">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="3a982-207">Tuttavia, quest'ultimo può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="3a982-207">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="3a982-208">La visualizzazione di un computer portatile non è rimovibile, né è un alimentatore non ridondante.</span><span class="sxs-lookup"><span data-stu-id="3a982-208">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="3a982-209">La rimozione di questi componenti influirà sulla funzione della creazione complessiva dei pacchetti o non è possibile grazie alla stretta integrazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3a982-209">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="3a982-210">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-210">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-211">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="3a982-211">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-212">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3a982-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a982-214">Se **true**, un pacchetto fisico è sostituibile (se è possibile sostituire, FRU o upgrade, l'elemento con un fisico diverso).</span><span class="sxs-lookup"><span data-stu-id="3a982-214">If **TRUE**, a physical package is replaceable (if it is possible to replace, FRU or upgrade, the element with a physically different one).</span></span> <span data-ttu-id="3a982-215">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="3a982-215">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="3a982-216">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="3a982-216">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="3a982-217">Un altro esempio è un pacchetto di alimentazione montato sulle guide scorrevoli.</span><span class="sxs-lookup"><span data-stu-id="3a982-217">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="3a982-218">Tutti i pacchetti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="3a982-218">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="3a982-219">Questa proprietà viene ereditata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-219">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-220">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="3a982-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-223">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="3a982-223">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3a982-224">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="3a982-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="3a982-225">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-226">**SKU**</span><span class="sxs-lookup"><span data-stu-id="3a982-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-229">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="3a982-229">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3a982-230">Numero di unità per l'elemento fisico che mantiene le scorte.</span><span class="sxs-lookup"><span data-stu-id="3a982-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="3a982-231">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a982-232">**Status**</span><span class="sxs-lookup"><span data-stu-id="3a982-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-233">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-235">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="3a982-235">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3a982-236">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3a982-236">Current status of the object.</span></span> <span data-ttu-id="3a982-237">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="3a982-237">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3a982-238">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="3a982-238">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3a982-239">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="3a982-239">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3a982-240">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="3a982-240">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3a982-241">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="3a982-241">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3a982-242">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3a982-243">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a982-243">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3a982-244">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3a982-244">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3a982-245">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="3a982-245">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3a982-246">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="3a982-246">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a982-247">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="3a982-247">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3a982-248">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="3a982-248">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3a982-249">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="3a982-249">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3a982-250">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="3a982-250">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3a982-251">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="3a982-251">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3a982-252">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="3a982-252">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3a982-253">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="3a982-253">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3a982-254">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="3a982-254">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3a982-255">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="3a982-255">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a982-256">**Tag**</span><span class="sxs-lookup"><span data-stu-id="3a982-256">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-259">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="3a982-259">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="3a982-260">Identificatore univoco del dispositivo a bordo connesso al sistema.</span><span class="sxs-lookup"><span data-stu-id="3a982-260">Unique identifier of the on-board device connected to the system.</span></span>

<span data-ttu-id="3a982-261">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="3a982-262">Esempio: "on board Device 1"</span><span class="sxs-lookup"><span data-stu-id="3a982-262">Example: "On Board Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="3a982-263">**Versione**</span><span class="sxs-lookup"><span data-stu-id="3a982-263">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a982-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3a982-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a982-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3a982-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a982-266">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="3a982-266">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3a982-267">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="3a982-267">Version of the physical element.</span></span>

<span data-ttu-id="3a982-268">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a982-269">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a982-269">Remarks</span></span>

<span data-ttu-id="3a982-270">La classe **Win32 \_ OnBoardDevice** è derivata da [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3a982-270">The **Win32\_OnBoardDevice** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a982-271">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a982-271">Requirements</span></span>



| <span data-ttu-id="3a982-272">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a982-272">Requirement</span></span> | <span data-ttu-id="3a982-273">Valore</span><span class="sxs-lookup"><span data-stu-id="3a982-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a982-274">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a982-274">Minimum supported client</span></span><br/> | <span data-ttu-id="3a982-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a982-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a982-276">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a982-276">Minimum supported server</span></span><br/> | <span data-ttu-id="3a982-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a982-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a982-278">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3a982-278">Namespace</span></span><br/>                | <span data-ttu-id="3a982-279">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3a982-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3a982-280">MOF</span><span class="sxs-lookup"><span data-stu-id="3a982-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a982-281"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a982-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a982-282">DLL</span><span class="sxs-lookup"><span data-stu-id="3a982-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a982-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a982-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a982-284">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a982-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a982-285">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3a982-285">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dt>

[<span data-ttu-id="3a982-286">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="3a982-286">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
