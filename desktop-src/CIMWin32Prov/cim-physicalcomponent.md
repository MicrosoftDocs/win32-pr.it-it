---
description: La \_ classe CIM PhysicalComponent rappresenta un componente di base o di basso livello all'interno di un pacchetto. Un elemento fisico che non è un collegamento, un connettore o un pacchetto è un discendente (o membro) di questa classe.
ms.assetid: 079874cd-5717-4662-a192-0ced16270bbd
ms.tgt_platform: multiple
title: Classe CIM_PhysicalComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalComponent
- CIM_PhysicalComponent.Caption
- CIM_PhysicalComponent.Description
- CIM_PhysicalComponent.InstallDate
- CIM_PhysicalComponent.Name
- CIM_PhysicalComponent.Status
- CIM_PhysicalComponent.CreationClassName
- CIM_PhysicalComponent.Manufacturer
- CIM_PhysicalComponent.Model
- CIM_PhysicalComponent.OtherIdentifyingInfo
- CIM_PhysicalComponent.PartNumber
- CIM_PhysicalComponent.PoweredOn
- CIM_PhysicalComponent.SerialNumber
- CIM_PhysicalComponent.SKU
- CIM_PhysicalComponent.Tag
- CIM_PhysicalComponent.Version
- CIM_PhysicalComponent.HotSwappable
- CIM_PhysicalComponent.Removable
- CIM_PhysicalComponent.Replaceable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e7e1db2c1d314b2d45816801643912dcf3b31bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483524"
---
# <a name="cim_physicalcomponent-class"></a><span data-ttu-id="a8b35-104">CIM \_ PhysicalComponent (classe)</span><span class="sxs-lookup"><span data-stu-id="a8b35-104">CIM\_PhysicalComponent class</span></span>

<span data-ttu-id="a8b35-105">La classe **CIM \_ PhysicalComponent** rappresenta un componente di base o di basso livello all'interno di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a8b35-105">The **CIM\_PhysicalComponent** class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="a8b35-106">Un elemento fisico che non è un collegamento, un connettore o un pacchetto è un discendente (o membro) di questa classe.</span><span class="sxs-lookup"><span data-stu-id="a8b35-106">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span> <span data-ttu-id="a8b35-107">Ad esempio, il chipset UART in una scheda modem interna è una sottoclasse (se sono definite proprietà o associazioni aggiuntive) o un'istanza di **CIM \_ PhysicalComponent**.</span><span class="sxs-lookup"><span data-stu-id="a8b35-107">For example, the UART chipset on an internal modem card would be a subclass (if additional properties or associations are defined) or an instance of **CIM\_PhysicalComponent**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8b35-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a8b35-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a8b35-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a8b35-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a8b35-110">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a8b35-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a8b35-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a8b35-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b35-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8b35-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B78-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalComponent : CIM_PhysicalElement
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
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
};
```

## <a name="members"></a><span data-ttu-id="a8b35-113">Members</span><span class="sxs-lookup"><span data-stu-id="a8b35-113">Members</span></span>

<span data-ttu-id="a8b35-114">La classe **CIM \_ PhysicalComponent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a8b35-114">The **CIM\_PhysicalComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="a8b35-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a8b35-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8b35-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a8b35-116">Properties</span></span>

<span data-ttu-id="a8b35-117">La classe **CIM \_ PhysicalComponent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a8b35-117">The **CIM\_PhysicalComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8b35-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a8b35-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-121">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a8b35-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-122">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a8b35-122">A short textual description of the object.</span></span>

<span data-ttu-id="a8b35-123">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a8b35-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-127">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a8b35-127">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-128">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="a8b35-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a8b35-129">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a8b35-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a8b35-130">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-130">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a8b35-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-134">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a8b35-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-135">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a8b35-135">A textual description of the object.</span></span>

<span data-ttu-id="a8b35-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-137">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="a8b35-137">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-138">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a8b35-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-140">Se **true**, il pacchetto può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="a8b35-140">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="a8b35-141">Un pacchetto fisico può essere scambiato a caldo se l'elemento può essere sostituito da un oggetto fisicamente diverso (ma equivalente) uno mentre il pacchetto contenitore è attivato.</span><span class="sxs-lookup"><span data-stu-id="a8b35-141">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="a8b35-142">Un componente della ventola, ad esempio, può essere progettato per essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="a8b35-142">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="a8b35-143">Tutti i componenti che possono essere scambiati a caldo sono intrinsecamente rimovibili e sostituibili.</span><span class="sxs-lookup"><span data-stu-id="a8b35-143">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-144">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a8b35-144">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-145">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a8b35-145">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-147">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a8b35-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-148">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="a8b35-148">Indicates when the object was installed.</span></span> <span data-ttu-id="a8b35-149">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="a8b35-149">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a8b35-150">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-151">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="a8b35-151">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-154">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a8b35-154">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-155">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a8b35-155">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="a8b35-156">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-156">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="a8b35-157">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-157">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-158">**Modello**</span><span class="sxs-lookup"><span data-stu-id="a8b35-158">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-161">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a8b35-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-162">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="a8b35-162">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="a8b35-163">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-163">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-164">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a8b35-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-167">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a8b35-167">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-168">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="a8b35-168">Label by which the object is known.</span></span> <span data-ttu-id="a8b35-169">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="a8b35-169">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a8b35-170">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-171">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a8b35-171">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-174">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a8b35-174">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="a8b35-175">Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset.</span><span class="sxs-lookup"><span data-stu-id="a8b35-175">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="a8b35-176">Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="a8b35-176">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="a8b35-177">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-177">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-178">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="a8b35-178">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-181">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a8b35-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-182">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a8b35-182">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="a8b35-183">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-183">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-184">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="a8b35-184">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-185">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a8b35-185">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-187">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="a8b35-187">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="a8b35-188">In caso contrario, è attualmente disattivato.</span><span class="sxs-lookup"><span data-stu-id="a8b35-188">Otherwise, it is currently off.</span></span>

<span data-ttu-id="a8b35-189">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-189">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-190">**Rimovibile**</span><span class="sxs-lookup"><span data-stu-id="a8b35-190">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-191">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a8b35-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-193">Se **true**, questo elemento è progettato per essere utilizzato e esterno al contenitore fisico in cui viene normalmente individuato, senza compromettere la funzione della creazione complessiva dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a8b35-193">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="a8b35-194">Un pacchetto viene considerato rimovibile anche se è necessario spegnere l'alimentazione per eseguire la rimozione.</span><span class="sxs-lookup"><span data-stu-id="a8b35-194">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="a8b35-195">Se la potenza può essere accesa e il pacchetto viene rimosso, l'elemento è rimovibile e può essere scambiato a caldo.</span><span class="sxs-lookup"><span data-stu-id="a8b35-195">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="a8b35-196">Ad esempio, un chip del processore aggiornabile è rimovibile.</span><span class="sxs-lookup"><span data-stu-id="a8b35-196">For example, an upgradeable processor chip is removable.</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-197">**Sostituibili**</span><span class="sxs-lookup"><span data-stu-id="a8b35-197">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-198">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a8b35-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-200">Se **true**, è possibile sostituire l'elemento con uno fisicamente diverso.</span><span class="sxs-lookup"><span data-stu-id="a8b35-200">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="a8b35-201">Alcuni sistemi di computer, ad esempio, consentono di aggiornare il chip del processore principale a una delle valutazioni di clock più elevate.</span><span class="sxs-lookup"><span data-stu-id="a8b35-201">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="a8b35-202">In questo caso, il processore viene definito sostituibile.</span><span class="sxs-lookup"><span data-stu-id="a8b35-202">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="a8b35-203">Tutti i componenti rimovibili sono intrinsecamente sostituibili.</span><span class="sxs-lookup"><span data-stu-id="a8b35-203">All removable components are inherently replaceable.</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-204">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="a8b35-204">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-205">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-207">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a8b35-207">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-208">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a8b35-208">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="a8b35-209">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-209">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-210">**SKU**</span><span class="sxs-lookup"><span data-stu-id="a8b35-210">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-211">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-213">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a8b35-213">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-214">Numero di unità di conservazione per questo elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a8b35-214">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="a8b35-215">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-215">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-216">**Status**</span><span class="sxs-lookup"><span data-stu-id="a8b35-216">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-219">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a8b35-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-220">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a8b35-220">String that indicates the current status of the object.</span></span> <span data-ttu-id="a8b35-221">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="a8b35-221">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a8b35-222">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="a8b35-222">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a8b35-223">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="a8b35-223">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a8b35-224">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="a8b35-224">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a8b35-225">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="a8b35-225">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a8b35-226">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="a8b35-226">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a8b35-227">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-227">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a8b35-228">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8b35-228">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a8b35-229">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a8b35-229">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a8b35-230">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a8b35-230">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a8b35-231">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a8b35-231">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a8b35-232">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a8b35-232">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a8b35-233">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a8b35-233">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a8b35-234">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a8b35-234">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a8b35-235">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a8b35-235">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a8b35-236">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a8b35-236">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a8b35-237">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a8b35-237">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a8b35-238">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a8b35-238">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a8b35-239">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a8b35-239">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a8b35-240">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a8b35-240">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a8b35-241">**Tag**</span><span class="sxs-lookup"><span data-stu-id="a8b35-241">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-244">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a8b35-244">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-245">Identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a8b35-245">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="a8b35-246">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="a8b35-246">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="a8b35-247">La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="a8b35-247">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="a8b35-248">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="a8b35-248">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="a8b35-249">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="a8b35-249">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="a8b35-250">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="a8b35-250">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="a8b35-251">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-251">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8b35-252">**Versione**</span><span class="sxs-lookup"><span data-stu-id="a8b35-252">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b35-253">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a8b35-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a8b35-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b35-255">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a8b35-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a8b35-256">Indica la versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a8b35-256">Indicates the version of the physical element.</span></span>

<span data-ttu-id="a8b35-257">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8b35-258">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8b35-258">Remarks</span></span>

<span data-ttu-id="a8b35-259">La classe **CIM \_ PhysicalComponent** è derivata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-259">The **CIM\_PhysicalComponent** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="a8b35-260">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a8b35-260">WMI does not implement this class.</span></span> <span data-ttu-id="a8b35-261">Per le classi WMI derivate da **CIM \_ PhysicalComponent**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a8b35-261">For WMI classes derived from **CIM\_PhysicalComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a8b35-262">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a8b35-262">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a8b35-263">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a8b35-263">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b35-264">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8b35-264">Requirements</span></span>



| <span data-ttu-id="a8b35-265">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b35-265">Requirement</span></span> | <span data-ttu-id="a8b35-266">Valore</span><span class="sxs-lookup"><span data-stu-id="a8b35-266">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b35-267">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8b35-267">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b35-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8b35-268">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8b35-269">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8b35-269">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b35-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8b35-270">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8b35-271">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a8b35-271">Namespace</span></span><br/>                | <span data-ttu-id="a8b35-272">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a8b35-272">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a8b35-273">MOF</span><span class="sxs-lookup"><span data-stu-id="a8b35-273">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8b35-274"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8b35-274"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8b35-275">DLL</span><span class="sxs-lookup"><span data-stu-id="a8b35-275">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8b35-276"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8b35-276"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b35-277">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8b35-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b35-278">**\_PhysicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="a8b35-278">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

