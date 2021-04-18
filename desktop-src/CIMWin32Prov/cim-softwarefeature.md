---
description: La \_ classe CIM SoftwareFeature rappresenta una funzione o una funzionalità specifica di un prodotto o di un sistema applicativo.
ms.assetid: 7beeb32c-d285-44f7-adeb-3b661d8ab037
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeature
- CIM_SoftwareFeature.Caption
- CIM_SoftwareFeature.Description
- CIM_SoftwareFeature.IdentifyingNumber
- CIM_SoftwareFeature.InstallDate
- CIM_SoftwareFeature.Name
- CIM_SoftwareFeature.ProductName
- CIM_SoftwareFeature.Status
- CIM_SoftwareFeature.Vendor
- CIM_SoftwareFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3959f7b99170cf1470d3688a101e4858f70e9a99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304489"
---
# <a name="cim_softwarefeature-class"></a><span data-ttu-id="a7867-103">CIM \_ SoftwareFeature (classe)</span><span class="sxs-lookup"><span data-stu-id="a7867-103">CIM\_SoftwareFeature class</span></span>

<span data-ttu-id="a7867-104">La classe **CIM \_ SoftwareFeature** rappresenta una funzione o una funzionalità specifica di un prodotto o di un sistema applicativo.</span><span class="sxs-lookup"><span data-stu-id="a7867-104">The **CIM\_SoftwareFeature** class represents a particular function or capability of a product or application system.</span></span> <span data-ttu-id="a7867-105">Questa classe riflette un livello di granularità significativo per un utente di un prodotto anziché per le unità che riflettono il modo in cui il prodotto viene compilato o incluso nel pacchetto (acquisito tramite una classe [**CIM \_ SoftwareElement**](cim-softwareelement.md) ).</span><span class="sxs-lookup"><span data-stu-id="a7867-105">This class reflects a level of granularity that is meaningful to a user of a product rather than the units that reflect how the product is built or packaged (captured using a [**CIM\_SoftwareElement**](cim-softwareelement.md) class).</span></span> <span data-ttu-id="a7867-106">Quando una funzionalità software può esistere in più piattaforme o sistemi operativi, la funzionalità software è una raccolta di elementi software per le diverse piattaforme.</span><span class="sxs-lookup"><span data-stu-id="a7867-106">When a software feature can exist on multiple platforms or operating systems, the software feature is a collection of the software elements for the different platforms.</span></span> <span data-ttu-id="a7867-107">In tal caso, gli utenti del modello saranno in genere interessati a una raccolta secondaria degli elementi software necessari per una determinata piattaforma.</span><span class="sxs-lookup"><span data-stu-id="a7867-107">In which case, the users of the model will be typically interested in a sub-collection of the software elements required for a particular platform.</span></span> <span data-ttu-id="a7867-108">Poiché le funzionalità vengono recapitate tramite prodotti, le funzionalità software sono sempre definite nel contesto di una classe di [**\_ prodotto CIM**](cim-product.md) mediante l'associazione [**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) .</span><span class="sxs-lookup"><span data-stu-id="a7867-108">Because features are delivered through products, software features are always defined in the context of a [**CIM\_Product**](cim-product.md) class using the [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association.</span></span> <span data-ttu-id="a7867-109">Facoltativamente, le funzionalità software di uno o più prodotti possono essere organizzate in sistemi applicativi mediante l'associazione [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="a7867-109">Optionally, software features from one or more products can be organized into application systems using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7867-110">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a7867-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a7867-111">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a7867-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a7867-112">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a7867-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a7867-113">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a7867-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7867-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7867-114">Syntax</span></span>

``` syntax
[UUID("{E527D7F2-E3D4-11d2-8601-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_SoftwareFeature : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="a7867-115">Members</span><span class="sxs-lookup"><span data-stu-id="a7867-115">Members</span></span>

<span data-ttu-id="a7867-116">La classe **CIM \_ SoftwareFeature** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a7867-116">The **CIM\_SoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="a7867-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a7867-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7867-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a7867-118">Properties</span></span>

<span data-ttu-id="a7867-119">La classe **CIM \_ SoftwareFeature** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a7867-119">The **CIM\_SoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7867-120">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a7867-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7867-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7867-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7867-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7867-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7867-123">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a7867-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a7867-124">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7867-124">Short textual description of the object.</span></span>

<span data-ttu-id="a7867-125">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7867-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7867-126">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a7867-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7867-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7867-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7867-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7867-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7867-129">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a7867-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a7867-130">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7867-130">Textual description of the object.</span></span>

<span data-ttu-id="a7867-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7867-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7867-132">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="a7867-132">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7867-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7867-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7867-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7867-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7867-135">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ prodotto CIM**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="a7867-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="a7867-136">Identificazione del prodotto, ad esempio un numero di serie del software o un numero di dado su un chip hardware.</span><span class="sxs-lookup"><span data-stu-id="a7867-136">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="a7867-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a7867-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7867-138">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a7867-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7867-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7867-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7867-140">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a7867-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a7867-141">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7867-141">Date and time the object was installed.</span></span> <span data-ttu-id="a7867-142">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="a7867-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a7867-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7867-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7867-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a7867-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7867-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7867-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7867-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7867-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7867-147">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a7867-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a7867-148">Etichetta con cui l'oggetto è noto all'esterno del sistema di elaborazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="a7867-148">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="a7867-149">L'etichetta è un nome leggibile che identifica in modo univoco l'elemento nel contesto dello spazio dei nomi dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a7867-149">The label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="a7867-150">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7867-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7867-151">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="a7867-151">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7867-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7867-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7867-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7867-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7867-154">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ prodotto CIM**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="a7867-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="a7867-155">Nome del prodotto comunemente usato.</span><span class="sxs-lookup"><span data-stu-id="a7867-155">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="a7867-156">**Status**</span><span class="sxs-lookup"><span data-stu-id="a7867-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7867-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7867-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7867-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7867-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7867-159">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a7867-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a7867-160">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7867-160">Current status of the object.</span></span>

<span data-ttu-id="a7867-161">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7867-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a7867-162">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7867-162">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a7867-163">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a7867-163">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a7867-164">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a7867-164">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a7867-165">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a7867-165">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a7867-166">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a7867-166">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a7867-167">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a7867-167">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a7867-168">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a7867-168">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a7867-169">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a7867-169">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a7867-170">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a7867-170">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a7867-171">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a7867-171">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a7867-172">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a7867-172">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a7867-173">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a7867-173">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a7867-174">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a7867-174">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a7867-175">**Fornitore**</span><span class="sxs-lookup"><span data-stu-id="a7867-175">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7867-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7867-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7867-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7867-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7867-178">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ prodotto CIM**](cim-product.md).**Vendor**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="a7867-178">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="a7867-179">Nome del fornitore del prodotto, che corrisponde alla proprietà del **Fornitore** nell'oggetto prodotto dello standard di scambio della soluzione DMTF.</span><span class="sxs-lookup"><span data-stu-id="a7867-179">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> <dt>

<span data-ttu-id="a7867-180">**Versione**</span><span class="sxs-lookup"><span data-stu-id="a7867-180">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7867-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7867-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7867-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7867-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7867-183">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ prodotto CIM**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="a7867-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a7867-184">Informazioni sulla versione del prodotto, che corrisponde alla proprietà **Version** nell'oggetto Product dello standard di scambio della soluzione DMTF.</span><span class="sxs-lookup"><span data-stu-id="a7867-184">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7867-185">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7867-185">Remarks</span></span>

<span data-ttu-id="a7867-186">La classe **CIM \_ SoftwareFeature** è derivata da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7867-186">The **CIM\_SoftwareFeature** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="a7867-187">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a7867-187">WMI does not implement this class.</span></span> <span data-ttu-id="a7867-188">Per le classi WMI derivate da **CIM \_ SoftwareFeature**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a7867-188">For WMI classes derived from **CIM\_SoftwareFeature**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a7867-189">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a7867-189">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a7867-190">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a7867-190">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7867-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7867-191">Requirements</span></span>



| <span data-ttu-id="a7867-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7867-192">Requirement</span></span> | <span data-ttu-id="a7867-193">Valore</span><span class="sxs-lookup"><span data-stu-id="a7867-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7867-194">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7867-194">Minimum supported client</span></span><br/> | <span data-ttu-id="a7867-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7867-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7867-196">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7867-196">Minimum supported server</span></span><br/> | <span data-ttu-id="a7867-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7867-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7867-198">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a7867-198">Namespace</span></span><br/>                | <span data-ttu-id="a7867-199">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a7867-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a7867-200">MOF</span><span class="sxs-lookup"><span data-stu-id="a7867-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7867-201"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7867-201"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7867-202">DLL</span><span class="sxs-lookup"><span data-stu-id="a7867-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7867-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7867-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7867-204">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7867-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7867-205">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="a7867-205">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

