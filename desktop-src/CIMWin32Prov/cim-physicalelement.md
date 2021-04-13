---
description: Le \_ sottoclassi CIM PhysicalElement definiscono qualsiasi componente di un sistema con un'identità fisica distinta. Le istanze di questa classe possono essere definite in termini di etichette che possono essere fisicamente collegate all'oggetto.
ms.assetid: 7ba6d1a9-f449-4ae2-a37c-517245bea39e
ms.tgt_platform: multiple
title: Classe CIM_PhysicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElement
- CIM_PhysicalElement.Caption
- CIM_PhysicalElement.Description
- CIM_PhysicalElement.InstallDate
- CIM_PhysicalElement.Name
- CIM_PhysicalElement.Status
- CIM_PhysicalElement.CreationClassName
- CIM_PhysicalElement.Manufacturer
- CIM_PhysicalElement.Model
- CIM_PhysicalElement.OtherIdentifyingInfo
- CIM_PhysicalElement.PartNumber
- CIM_PhysicalElement.PoweredOn
- CIM_PhysicalElement.SerialNumber
- CIM_PhysicalElement.SKU
- CIM_PhysicalElement.Tag
- CIM_PhysicalElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5afeda74789bc492aac3d37629b64385b8734f60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523121"
---
# <a name="cim_physicalelement-class"></a><span data-ttu-id="a38b4-104">CIM \_ PhysicalElement (classe)</span><span class="sxs-lookup"><span data-stu-id="a38b4-104">CIM\_PhysicalElement class</span></span>

<span data-ttu-id="a38b4-105">Le sottoclassi **CIM \_ PhysicalElement** definiscono qualsiasi componente di un sistema con un'identità fisica distinta.</span><span class="sxs-lookup"><span data-stu-id="a38b4-105">The **CIM\_PhysicalElement** subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="a38b4-106">Le istanze di questa classe possono essere definite in termini di etichette che possono essere fisicamente collegate all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a38b4-106">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span> <span data-ttu-id="a38b4-107">Tutti i processi, i file e i dispositivi logici non sono considerati elementi fisici.</span><span class="sxs-lookup"><span data-stu-id="a38b4-107">All processes, files, and logical devices are not considered to be physical elements.</span></span> <span data-ttu-id="a38b4-108">Ad esempio, non è possibile alleghi un'etichetta a un modem; è possibile solo alleghi un'etichetta alla scheda che implementa il modem.</span><span class="sxs-lookup"><span data-stu-id="a38b4-108">For example, it is not possible to attach a label to a modem; it is only possible to attach a label to the card that implements the modem.</span></span> <span data-ttu-id="a38b4-109">La stessa scheda può inoltre implementare una scheda LAN.</span><span class="sxs-lookup"><span data-stu-id="a38b4-109">The same card could also implement a LAN adapter.</span></span>

<span data-ttu-id="a38b4-110">Gli elementi di sistema gestiti tangibili, in genere elementi hardware, hanno una manifestazione fisica.</span><span class="sxs-lookup"><span data-stu-id="a38b4-110">Tangible managed system elements (usually hardware items) have a physical manifestation.</span></span> <span data-ttu-id="a38b4-111">Un elemento del sistema gestito non è necessariamente un componente discreto.</span><span class="sxs-lookup"><span data-stu-id="a38b4-111">A managed system element is not necessarily a discrete component.</span></span> <span data-ttu-id="a38b4-112">Ad esempio, è possibile che una singola scheda (un tipo di elemento fisico) ospiti più di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="a38b4-112">For example, it is possible for a single card (a type of physical element) to host more than one logical device.</span></span> <span data-ttu-id="a38b4-113">La scheda verrebbe rappresentata da un singolo elemento fisico associato a più dispositivi logici.</span><span class="sxs-lookup"><span data-stu-id="a38b4-113">The card would be represented by a single physical element associated with multiple logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a38b4-114">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a38b4-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a38b4-115">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a38b4-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a38b4-116">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a38b4-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a38b4-117">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a38b4-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a38b4-118">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a38b4-118">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B61-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="a38b4-119">Members</span><span class="sxs-lookup"><span data-stu-id="a38b4-119">Members</span></span>

<span data-ttu-id="a38b4-120">La classe **CIM \_ PhysicalElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a38b4-120">The **CIM\_PhysicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="a38b4-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a38b4-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a38b4-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a38b4-122">Properties</span></span>

<span data-ttu-id="a38b4-123">La classe **CIM \_ PhysicalElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a38b4-123">The **CIM\_PhysicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a38b4-124">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a38b4-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-127">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a38b4-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-128">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a38b4-128">A short textual description of the object.</span></span>

<span data-ttu-id="a38b4-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a38b4-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a38b4-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-133">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a38b4-133">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-134">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="a38b4-134">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a38b4-135">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a38b4-135">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-136">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a38b4-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-139">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a38b4-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-140">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a38b4-140">A textual description of the object.</span></span>

<span data-ttu-id="a38b4-141">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a38b4-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a38b4-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-143">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a38b4-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-145">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a38b4-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-146">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="a38b4-146">Indicates when the object was installed.</span></span> <span data-ttu-id="a38b4-147">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="a38b4-147">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a38b4-148">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a38b4-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-149">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="a38b4-149">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-152">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a38b4-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-153">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a38b4-153">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="a38b4-154">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="a38b4-154">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-155">**Modello**</span><span class="sxs-lookup"><span data-stu-id="a38b4-155">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-158">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a38b4-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-159">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="a38b4-159">Name by which the physical element is generally known.</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-160">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a38b4-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-163">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a38b4-163">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-164">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="a38b4-164">Label by which the object is known.</span></span> <span data-ttu-id="a38b4-165">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="a38b4-165">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a38b4-166">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a38b4-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-167">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a38b4-167">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-170">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a38b4-170">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="a38b4-171">Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset.</span><span class="sxs-lookup"><span data-stu-id="a38b4-171">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="a38b4-172">Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="a38b4-172">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-173">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="a38b4-173">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-176">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a38b4-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-177">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a38b4-177">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-178">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="a38b4-178">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-179">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a38b4-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-181">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="a38b4-181">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="a38b4-182">In caso contrario, è attualmente disattivato.</span><span class="sxs-lookup"><span data-stu-id="a38b4-182">Otherwise, it is currently off.</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-183">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="a38b4-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-186">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a38b4-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-187">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a38b4-187">Manufacturer-allocated number used to identify the physical element.</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-188">**SKU**</span><span class="sxs-lookup"><span data-stu-id="a38b4-188">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-191">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a38b4-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-192">Numero di unità di conservazione per questo elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a38b4-192">Stock-keeping unit number for this physical element.</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-193">**Status**</span><span class="sxs-lookup"><span data-stu-id="a38b4-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-196">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a38b4-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-197">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a38b4-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="a38b4-198">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="a38b4-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a38b4-199">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="a38b4-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a38b4-200">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="a38b4-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a38b4-201">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="a38b4-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a38b4-202">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="a38b4-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a38b4-203">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="a38b4-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a38b4-204">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a38b4-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a38b4-205">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a38b4-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a38b4-206">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a38b4-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a38b4-207">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a38b4-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a38b4-208">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a38b4-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a38b4-209">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a38b4-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a38b4-210">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a38b4-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a38b4-211">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a38b4-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a38b4-212">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a38b4-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a38b4-213">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a38b4-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a38b4-214">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a38b4-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a38b4-215">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a38b4-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a38b4-216">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a38b4-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a38b4-217">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a38b4-217">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a38b4-218">**Tag**</span><span class="sxs-lookup"><span data-stu-id="a38b4-218">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-221">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a38b4-221">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-222">Identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a38b4-222">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="a38b4-223">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="a38b4-223">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="a38b4-224">La chiave per **CIM \_ PhysicalElement** è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="a38b4-224">The key for **CIM\_PhysicalElement** is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="a38b4-225">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="a38b4-225">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="a38b4-226">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="a38b4-226">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="a38b4-227">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="a38b4-227">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="a38b4-228">**Versione**</span><span class="sxs-lookup"><span data-stu-id="a38b4-228">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a38b4-229">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a38b4-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a38b4-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a38b4-231">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a38b4-231">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a38b4-232">Indica la versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a38b4-232">Indicates the version of the physical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a38b4-233">Commenti</span><span class="sxs-lookup"><span data-stu-id="a38b4-233">Remarks</span></span>

<span data-ttu-id="a38b4-234">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a38b4-234">WMI does not implement this class.</span></span> <span data-ttu-id="a38b4-235">Per le classi WMI derivate da **CIM \_ PhysicalElement**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a38b4-235">For WMI classes derived from **CIM\_PhysicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a38b4-236">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a38b4-236">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a38b4-237">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a38b4-237">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a38b4-238">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a38b4-238">Requirements</span></span>



| <span data-ttu-id="a38b4-239">Requisito</span><span class="sxs-lookup"><span data-stu-id="a38b4-239">Requirement</span></span> | <span data-ttu-id="a38b4-240">Valore</span><span class="sxs-lookup"><span data-stu-id="a38b4-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a38b4-241">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a38b4-241">Minimum supported client</span></span><br/> | <span data-ttu-id="a38b4-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a38b4-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a38b4-243">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a38b4-243">Minimum supported server</span></span><br/> | <span data-ttu-id="a38b4-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a38b4-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a38b4-245">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a38b4-245">Namespace</span></span><br/>                | <span data-ttu-id="a38b4-246">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a38b4-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a38b4-247">MOF</span><span class="sxs-lookup"><span data-stu-id="a38b4-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a38b4-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a38b4-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a38b4-249">DLL</span><span class="sxs-lookup"><span data-stu-id="a38b4-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a38b4-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a38b4-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a38b4-251">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a38b4-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a38b4-252">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="a38b4-252">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

