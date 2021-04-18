---
description: Fornisce regole per il mapping delle classi WMI al Active Directory.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Mapping di classi Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a606cfacc2e9d56ef07973df182f5ce1a65be35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314596"
---
# <a name="mapping-active-directory-classes"></a><span data-ttu-id="fd25a-103">Mapping di classi Active Directory</span><span class="sxs-lookup"><span data-stu-id="fd25a-103">Mapping Active Directory Classes</span></span>

<span data-ttu-id="fd25a-104">Poiché Active Directory dispone di un'ampia gamma di oggetti possibili, WMI non è in grado di creare un mapping diretto uno a uno.</span><span class="sxs-lookup"><span data-stu-id="fd25a-104">Because Active Directory has a wide variety of possible objects, WMI cannot create a direct one-to-one mapping.</span></span> <span data-ttu-id="fd25a-105">Il provider di servizi directory utilizza invece regole per eseguire il mapping delle classi tra le due tecnologie.</span><span class="sxs-lookup"><span data-stu-id="fd25a-105">Instead, the Directory Services provider uses rules to map classes between the two technologies.</span></span>

<span data-ttu-id="fd25a-106">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="fd25a-106">This following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="fd25a-107">Classi di mapping</span><span class="sxs-lookup"><span data-stu-id="fd25a-107">Mapping Classes</span></span>](#mapping-classes)
-   [<span data-ttu-id="fd25a-108">Attributi di mapping</span><span class="sxs-lookup"><span data-stu-id="fd25a-108">Mapping Attributes</span></span>](#mapping-attributes)
-   [<span data-ttu-id="fd25a-109">Classi Association</span><span class="sxs-lookup"><span data-stu-id="fd25a-109">Association Classes</span></span>](#association-classes)

> [!Note]  
> <span data-ttu-id="fd25a-110">Per ulteriori informazioni sul supporto e l'installazione di questo componente in un sistema operativo specifico, vedere la pagina relativa alla [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="fd25a-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

## <a name="mapping-classes"></a><span data-ttu-id="fd25a-111">Classi di mapping</span><span class="sxs-lookup"><span data-stu-id="fd25a-111">Mapping Classes</span></span>

<span data-ttu-id="fd25a-112">Nell'elenco seguente vengono descritte le linee guida utilizzate dal provider di servizi directory per eseguire il mapping delle classi Active Directory alle classi WMI:</span><span class="sxs-lookup"><span data-stu-id="fd25a-112">The following list describes the guidelines that the Directory Services provider uses to map Active Directory classes to WMI classes:</span></span>

-   <span data-ttu-id="fd25a-113">Ogni classe astratta nello schema Active Directory viene mappata a una classe astratta nello schema WMI.</span><span class="sxs-lookup"><span data-stu-id="fd25a-113">Each abstract class in the Active Directory schema maps to one abstract class in the WMI schema.</span></span>

    <span data-ttu-id="fd25a-114">Nello schema WMI ogni classe astratta è preceduta da servizi di dominio Active Directory \_ .</span><span class="sxs-lookup"><span data-stu-id="fd25a-114">In the WMI schema, each abstract class is prefixed with DS\_.</span></span> <span data-ttu-id="fd25a-115">Ad esempio, la classe **Person** dello schema Active Directory viene mappata alla classe WMI **\_ Person DS** .</span><span class="sxs-lookup"><span data-stu-id="fd25a-115">For example, the **person** class from the Active Directory schema maps to the **DS\_person** WMI class.</span></span>

-   <span data-ttu-id="fd25a-116">Ogni classe non astratta dello schema Active Directory viene mappata alle due classi seguenti nello schema WMI:</span><span class="sxs-lookup"><span data-stu-id="fd25a-116">Each nonabstract class from the Active Directory schema maps to the following two classes in the WMI schema:</span></span>

    -   <span data-ttu-id="fd25a-117">La prima classe mappata è preceduta da ADS \_ .</span><span class="sxs-lookup"><span data-stu-id="fd25a-117">The first mapped class is prefixed with ADS\_.</span></span> <span data-ttu-id="fd25a-118">Si tratta di classi astratte, mappate in base alle regole indicate di seguito.</span><span class="sxs-lookup"><span data-stu-id="fd25a-118">These are abstract classes, mapped according to the rules below.</span></span>
    -   <span data-ttu-id="fd25a-119">La seconda classe mappata è una classe non astratta con il \_ prefisso del nome DS.</span><span class="sxs-lookup"><span data-stu-id="fd25a-119">The second mapped class is a nonabstract class with the DS\_ name prefix.</span></span> <span data-ttu-id="fd25a-120">Questa classe è derivata dalla \_ classe astratta ADS, con l'aggiunta del qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="fd25a-120">This class is derived from the ADS\_ abstract class, with the addition of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

    <span data-ttu-id="fd25a-121">Ad esempio, la classe **utente** dello schema Active Directory viene mappata a due classi.</span><span class="sxs-lookup"><span data-stu-id="fd25a-121">For example, the **user** class from the Active Directory schema maps to two classes.</span></span> <span data-ttu-id="fd25a-122">La prima classe è la classe astratta **\_ dell'utente ADS** , mappata in base alle regole indicate di seguito.</span><span class="sxs-lookup"><span data-stu-id="fd25a-122">The first class is the **ADS\_user** abstract class, mapped according to rules below.</span></span> <span data-ttu-id="fd25a-123">La seconda classe è la classe non astratta dell' **\_ utente DS** .</span><span class="sxs-lookup"><span data-stu-id="fd25a-123">The second class is the **DS\_user** nonabstract class.</span></span> <span data-ttu-id="fd25a-124">Viene derivato dall' **\_ utente ADS** ed è associato al qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) aggiunto.</span><span class="sxs-lookup"><span data-stu-id="fd25a-124">It is derived from **ADS\_user** and has the added [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

-   <span data-ttu-id="fd25a-125">Se non specificato diversamente, il nome di una classe mappata è il valore modificato della proprietà **LDAP-Display-Name** nella classe Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fd25a-125">Unless specified otherwise, the name of a mapped class is the mangled value of the **LDAP-Display-Name** property in the Active Directory class.</span></span>
-   <span data-ttu-id="fd25a-126">Se la proprietà **Sub-Class-of** è presente nella classe Active Directory, la classe mappata a WMI viene derivata dalla classe specificata.</span><span class="sxs-lookup"><span data-stu-id="fd25a-126">If the **Sub-Class-Of** property is present on the Active Directory class, the WMI-mapped class is derived from the specified class.</span></span>

    <span data-ttu-id="fd25a-127">Se la proprietà **della classe secondaria-of** non è presente, la classe mappata a WMI viene derivata dalla classe della classe **\_ \_ radice \_ LDAP DS** , come specificato nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="fd25a-127">If the **Sub-Class-Of** property is not present, the WMI-mapped class is derived from the **DS\_LDAP\_Root\_Class** class, as specified in the MOF file.</span></span>

    > [!Note]  
    > <span data-ttu-id="fd25a-128">Questa classe dispone della proprietà della chiave **ADSIPath** , con un tipo **VT \_ BSTR**.</span><span class="sxs-lookup"><span data-stu-id="fd25a-128">This class has the **ADSIPath** key property, with a type **VT\_BSTR**.</span></span> <span data-ttu-id="fd25a-129">Si tratta del percorso ADSI univoco che identifica questa istanza.</span><span class="sxs-lookup"><span data-stu-id="fd25a-129">This is the unique ADSI path that identifies this instance.</span></span> <span data-ttu-id="fd25a-130">Active Directory supporta solo l'ereditarietà singola, quindi funziona.</span><span class="sxs-lookup"><span data-stu-id="fd25a-130">Active Directory supports single-inheritance only, so this works.</span></span>

     

-   <span data-ttu-id="fd25a-131">Un qualificatore **dinamico** di tipo **VT \_ bool** e Flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` impostato su **true** viene creato per ogni classe.</span><span class="sxs-lookup"><span data-stu-id="fd25a-131">A **Dynamic** qualifier of type **VT\_BOOL**, and flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to **TRUE** is created for every class.</span></span> <span data-ttu-id="fd25a-132">Si tratta di un qualificatore WMI standard che indica che le istanze di questa classe vengono fornite dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="fd25a-132">This is a standard WMI qualifier that indicates that instances of this class are provided dynamically.</span></span>
-   <span data-ttu-id="fd25a-133">Se la classe non è astratta, il provider crea un qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) di tipo **VT \_ BSTR bool** e Qualifier Flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` impostati su "DS instance provider" per ogni classe.</span><span class="sxs-lookup"><span data-stu-id="fd25a-133">If the class is not abstract, the provider creates a [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier of type **VT\_BSTR BOOL** and qualifier flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to "DS Instance Provider" for every class.</span></span> <span data-ttu-id="fd25a-134">Qualificatore WMI standard che indica il nome del provider che fornisce dinamicamente le istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="fd25a-134">This is a standard WMI qualifier that indicates the name of the provider dynamically providing instances of this class.</span></span>

<span data-ttu-id="fd25a-135">Il resto delle proprietà ADSI viene mappato a qualificatori di classe e proprietà in base alle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="fd25a-135">The rest of the ADSI properties map to class qualifiers and properties as per the following tables.</span></span> <span data-ttu-id="fd25a-136">Tutti i qualificatori vengono mappati con un valore del flag di qualificatore `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .</span><span class="sxs-lookup"><span data-stu-id="fd25a-136">All qualifiers map with a qualifier flag value of `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS`.</span></span>

<span data-ttu-id="fd25a-137">Di seguito sono elencate le informazioni di mapping per la classe Active Directory, che mostra il qualificatore WMI e il tipo di qualificatore WMI per ogni proprietà Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fd25a-137">The following lists mapping information for the Active Directory class, showing the WMI qualifier and WMI qualifier type for each Active Directory property.</span></span>

<dl> <dt>

<span data-ttu-id="fd25a-138">**Nome comune**</span><span class="sxs-lookup"><span data-stu-id="fd25a-138">**Common-Name**</span></span>
</dt> <dd>

<span data-ttu-id="fd25a-139">**CN** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="fd25a-139">**CN** (**VT\_BSTR**)</span></span>

<span data-ttu-id="fd25a-140">Mappato direttamente dal valore stringa.</span><span class="sxs-lookup"><span data-stu-id="fd25a-140">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="fd25a-141">**Default-Object-Category**</span><span class="sxs-lookup"><span data-stu-id="fd25a-141">**Default-Object-Category**</span></span>
</dt> <dd>

<span data-ttu-id="fd25a-142">**DefaultObjectCategory** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="fd25a-142">**DefaultObjectCategory** (**VT\_BSTR**)</span></span>

<span data-ttu-id="fd25a-143">Mappato direttamente dal valore stringa.</span><span class="sxs-lookup"><span data-stu-id="fd25a-143">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="fd25a-144">**Descrittore di sicurezza predefinito**</span><span class="sxs-lookup"><span data-stu-id="fd25a-144">**Default-Security-Descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="fd25a-145">**DefaultSecurityDescriptor** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="fd25a-145">**DefaultSecurityDescriptor** (**VT\_BSTR**)</span></span>

<span data-ttu-id="fd25a-146">Mappato direttamente dal valore stringa.</span><span class="sxs-lookup"><span data-stu-id="fd25a-146">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="fd25a-147">**Governas-ID**</span><span class="sxs-lookup"><span data-stu-id="fd25a-147">**Governs-Id**</span></span>
</dt> <dd>

<span data-ttu-id="fd25a-148">**GovernsId** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="fd25a-148">**GovernsId** (**VT\_BSTR**)</span></span>

<span data-ttu-id="fd25a-149">Mappato dalla rappresentazione di stringa dell'OID; ad esempio, "{1 3 3 6}".</span><span class="sxs-lookup"><span data-stu-id="fd25a-149">Mapped from the string representation of the OID; for example, "{ 1 3 3 6 }".</span></span>

</dd> <dt>

<span data-ttu-id="fd25a-150">**Classe Object**</span><span class="sxs-lookup"><span data-stu-id="fd25a-150">**Object-Class**</span></span>
</dt> <dd>

<span data-ttu-id="fd25a-151">N/D</span><span class="sxs-lookup"><span data-stu-id="fd25a-151">N/A</span></span>

<span data-ttu-id="fd25a-152">Non mappato.</span><span class="sxs-lookup"><span data-stu-id="fd25a-152">Not mapped.</span></span>

</dd> <dt>

<span data-ttu-id="fd25a-153">**Classe Object-Category**</span><span class="sxs-lookup"><span data-stu-id="fd25a-153">**Object-Class-Category**</span></span>
</dt> <dd>

<span data-ttu-id="fd25a-154">**ObjectClassCategory** (**VT \_ I4**)</span><span class="sxs-lookup"><span data-stu-id="fd25a-154">**ObjectClassCategory** (**VT\_I4**)</span></span>

<span data-ttu-id="fd25a-155">Mappato direttamente dal valore intero.</span><span class="sxs-lookup"><span data-stu-id="fd25a-155">Mapped directly from the integer value.</span></span> <span data-ttu-id="fd25a-156">Inoltre, se il valore è abstract (2), viene creato anche il qualificatore standard di **VT \_ bool** CIM, denominato qualificatore **"abstract"** .</span><span class="sxs-lookup"><span data-stu-id="fd25a-156">In addition, if the value is Abstract(2), then the standard **VT\_BOOL** CIM qualifier, called the **"Abstract"** qualifier, is also created.</span></span>

</dd> <dt>

<span data-ttu-id="fd25a-157">**RDN-ATT-ID**</span><span class="sxs-lookup"><span data-stu-id="fd25a-157">**RDN-ATT-ID**</span></span>
</dt> <dd>

<span data-ttu-id="fd25a-158">**RDNATTID** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="fd25a-158">**RDNATTID** (**VT\_BSTR**)</span></span>

<span data-ttu-id="fd25a-159">Mappato dalla rappresentazione di stringa del valore OID; ad esempio, "{1 3 3 6}".</span><span class="sxs-lookup"><span data-stu-id="fd25a-159">Mapped from the string representation of the OID value; for example, "{ 1 3 3 6 }".</span></span> <span data-ttu-id="fd25a-160">Inoltre, la proprietà identificata qui viene annotata con il qualificatore CIM **indicizzato** standard impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="fd25a-160">In addition, the property identified here is annotated with the standard **Indexed** CIM qualifier set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="fd25a-161">**Solo sistema**</span><span class="sxs-lookup"><span data-stu-id="fd25a-161">**System-Only**</span></span>
</dt> <dd>

<span data-ttu-id="fd25a-162">**SystemOnly** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="fd25a-162">**SystemOnly** (**VT\_BOOL**)</span></span>

<span data-ttu-id="fd25a-163">Mappato direttamente dal valore booleano.</span><span class="sxs-lookup"><span data-stu-id="fd25a-163">Mapped directly from the Boolean value.</span></span>

</dd> </dl>

 

<span data-ttu-id="fd25a-164">Di seguito sono elencate le proprietà della classe Active Directory mappate alle proprietà della classe WMI.</span><span class="sxs-lookup"><span data-stu-id="fd25a-164">The following lists the Active Directory class properties mapped to WMI class properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd25a-165">**Può contenere**</span><span class="sxs-lookup"><span data-stu-id="fd25a-165">**May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="fd25a-166">Ogni proprietà in questo elenco è mappata a una proprietà WMI.</span><span class="sxs-lookup"><span data-stu-id="fd25a-166">Each property in this list is mapped to a WMI property.</span></span>

</dd> <dt>

<span data-ttu-id="fd25a-167">**Deve contenere**</span><span class="sxs-lookup"><span data-stu-id="fd25a-167">**Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="fd25a-168">Ogni proprietà in questo elenco è mappata a una proprietà WMI.</span><span class="sxs-lookup"><span data-stu-id="fd25a-168">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="fd25a-169">Per ognuno di questi, viene creato il qualificatore CIM standard **Not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="fd25a-169">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span>

</dd> <dt>

<span data-ttu-id="fd25a-170">**Sistema-può contenere**</span><span class="sxs-lookup"><span data-stu-id="fd25a-170">**System-May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="fd25a-171">Ogni proprietà in questo elenco è mappata a una proprietà WMI.</span><span class="sxs-lookup"><span data-stu-id="fd25a-171">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="fd25a-172">Inoltre, ogni proprietà viene annotata con un qualificatore di **sistema** , impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="fd25a-172">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="fd25a-173">**System-must-contain**</span><span class="sxs-lookup"><span data-stu-id="fd25a-173">**System-Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="fd25a-174">Ogni proprietà in questo elenco è mappata a una proprietà WMI.</span><span class="sxs-lookup"><span data-stu-id="fd25a-174">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="fd25a-175">Per ognuno di questi, viene creato il qualificatore CIM standard **Not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="fd25a-175">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span> <span data-ttu-id="fd25a-176">Inoltre, ogni proprietà viene annotata con un qualificatore di **sistema** , impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="fd25a-176">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> </dl>

## <a name="mapping-attributes"></a><span data-ttu-id="fd25a-177">Attributi di mapping</span><span class="sxs-lookup"><span data-stu-id="fd25a-177">Mapping Attributes</span></span>

<span data-ttu-id="fd25a-178">Il provider di servizi directory esegue il mapping di ogni attributo di una classe Active Directory esattamente a una proprietà della classe WMI corrispondente in base alle regole di questa sezione.</span><span class="sxs-lookup"><span data-stu-id="fd25a-178">The Directory Services provider maps each attribute of an Active Directory class to exactly one property of the corresponding WMI class according to the rules in this section.</span></span> <span data-ttu-id="fd25a-179">In generale, il provider di servizi directory denomina la proprietà WMI come versione alterata del valore **LDAP-Display-Name** dell'attributo Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fd25a-179">In general, the Directory Services Provider names the WMI property as the mangled version of the **LDAP-Display-Name** value of the Active Directory attribute.</span></span>

<span data-ttu-id="fd25a-180">Se la proprietà Active Directory **è a valore singolo** è **false**, questa proprietà WMI viene combinata con l'operatore OR con la **matrice di \_ flag \_ CIM**.</span><span class="sxs-lookup"><span data-stu-id="fd25a-180">If the Active Directory property **Is-Single-Valued** is **FALSE**, then this WMI property is combined with the OR operator with **CIM\_FLAG\_ARRAY**.</span></span> <span data-ttu-id="fd25a-181">Si noti che ogni proprietà è contrassegnata con il qualificatore **\_ BSTR VT** , **ADSyntax**.</span><span class="sxs-lookup"><span data-stu-id="fd25a-181">Note that each property is tagged with the **VT\_BSTR** qualifier, **ADSyntax**.</span></span> <span data-ttu-id="fd25a-182">Rappresenta la sintassi del Active Directory sottostante.</span><span class="sxs-lookup"><span data-stu-id="fd25a-182">It represents the underlying Active Directory syntax.</span></span>

<span data-ttu-id="fd25a-183">Nella tabella seguente viene elencato il mapping della sintassi Active Directory al tipo di dati della proprietà WMI.</span><span class="sxs-lookup"><span data-stu-id="fd25a-183">The following table lists the mapping of the Active Directory syntax to the WMI property data type.</span></span>



| <span data-ttu-id="fd25a-184">Elemento Active Directory</span><span class="sxs-lookup"><span data-stu-id="fd25a-184">Active Directory element</span></span>                                      | <span data-ttu-id="fd25a-185">Tipo di dati WMI</span><span class="sxs-lookup"><span data-stu-id="fd25a-185">WMI data type</span></span>                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="fd25a-186">**Punto di accesso**</span><span class="sxs-lookup"><span data-stu-id="fd25a-186">**Access-Point**</span></span>](/windows/desktop/ADSchema/s-object-access-point)            | <span data-ttu-id="fd25a-187">**\_stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-187">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="fd25a-188">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fd25a-188">**Boolean**</span></span>](/windows/desktop/ADSchema/s-boolean)                             | <span data-ttu-id="fd25a-189">**\_valore booleano CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-189">**CIM\_BOOLEAN**</span></span>                                                        |
| <span data-ttu-id="fd25a-190">**Stringa senza distinzione tra maiuscole e minuscole**</span><span class="sxs-lookup"><span data-stu-id="fd25a-190">**Case Insensitive String**</span></span>                                   | <span data-ttu-id="fd25a-191">**\_stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-191">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="fd25a-192">**Stringa distinzione tra maiuscole e minuscole**</span><span class="sxs-lookup"><span data-stu-id="fd25a-192">**Case Sensitive String**</span></span>](/windows/desktop/ADSchema/s-string-case-sensitive) | <span data-ttu-id="fd25a-193">**\_stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-193">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="fd25a-194">**Nome distinto**</span><span class="sxs-lookup"><span data-stu-id="fd25a-194">**Distinguished Name**</span></span>](/windows/desktop/ADSchema/s-object-ds-dn)             | <span data-ttu-id="fd25a-195">**\_stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-195">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="fd25a-196">**DN-binario**</span><span class="sxs-lookup"><span data-stu-id="fd25a-196">**DN-Binary**</span></span>](/windows/desktop/ADSchema/s-object-dn-binary)                  | <span data-ttu-id="fd25a-197">Oggetto incorporato della classe **DN \_ con \_ binario** definito di seguito.</span><span class="sxs-lookup"><span data-stu-id="fd25a-197">Embedded object of class **DN\_With\_Binary** defined below.</span></span><br/> |
| [<span data-ttu-id="fd25a-198">**Stringa DN**</span><span class="sxs-lookup"><span data-stu-id="fd25a-198">**DN-String**</span></span>](/windows/desktop/ADSchema/s-object-dn-string)                  | <span data-ttu-id="fd25a-199">Oggetto incorporato della classe **DN \_ con la \_ stringa** definita di seguito.</span><span class="sxs-lookup"><span data-stu-id="fd25a-199">Embedded object of class **DN\_With\_String** defined below.</span></span><br/> |
| [<span data-ttu-id="fd25a-200">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="fd25a-200">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="fd25a-201">**\_SINT32 CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-201">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="fd25a-202">**Enumerazione**</span><span class="sxs-lookup"><span data-stu-id="fd25a-202">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="fd25a-203">**\_stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-203">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="fd25a-204">**Integer**</span><span class="sxs-lookup"><span data-stu-id="fd25a-204">**Integer**</span></span>](/windows/desktop/ADSchema/s-integer)                             | <span data-ttu-id="fd25a-205">**\_SINT32 CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-205">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="fd25a-206">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="fd25a-206">**LargeInteger**</span></span>](/windows/desktop/ADSchema/s-largeinteger)                   | <span data-ttu-id="fd25a-207">**\_stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-207">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="fd25a-208">Descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="fd25a-208">Security Descriptor</span></span>                                           | <span data-ttu-id="fd25a-209">Oggetto incorporato della classe **Uint8Array** definito di seguito.</span><span class="sxs-lookup"><span data-stu-id="fd25a-209">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="fd25a-210">Stringa numerica</span><span class="sxs-lookup"><span data-stu-id="fd25a-210">Numeric String</span></span>                                                | <span data-ttu-id="fd25a-211">**\_stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-211">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="fd25a-212">ID dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fd25a-212">Object ID</span></span>                                                     | <span data-ttu-id="fd25a-213">**\_stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-213">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="fd25a-214">Stringa ottetto</span><span class="sxs-lookup"><span data-stu-id="fd25a-214">Octet String</span></span>                                                  | <span data-ttu-id="fd25a-215">Oggetto incorporato della classe **Uint8Array** definito di seguito.</span><span class="sxs-lookup"><span data-stu-id="fd25a-215">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="fd25a-216">O nome</span><span class="sxs-lookup"><span data-stu-id="fd25a-216">OR Name</span></span>                                                       | <span data-ttu-id="fd25a-217">**\_stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-217">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="fd25a-218">Presentation-Address</span><span class="sxs-lookup"><span data-stu-id="fd25a-218">Presentation-Address</span></span>                                          | <span data-ttu-id="fd25a-219">Oggetto incorporato della classe **Uint8Array** definito di seguito.</span><span class="sxs-lookup"><span data-stu-id="fd25a-219">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="fd25a-220">Stringa del case di stampa</span><span class="sxs-lookup"><span data-stu-id="fd25a-220">Print Case String</span></span>                                             | <span data-ttu-id="fd25a-221">**\_stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-221">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="fd25a-222">Collegamento replica</span><span class="sxs-lookup"><span data-stu-id="fd25a-222">Replica Link</span></span>                                                  | <span data-ttu-id="fd25a-223">Oggetto incorporato della classe **Uint8Array** definito di seguito.</span><span class="sxs-lookup"><span data-stu-id="fd25a-223">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| [<span data-ttu-id="fd25a-224">**Stringa (SID)**</span><span class="sxs-lookup"><span data-stu-id="fd25a-224">**String(Sid)**</span></span>](/windows/desktop/ADSchema/s-string-sid)                      | <span data-ttu-id="fd25a-225">Oggetto incorporato della classe **Uint8Array** definito di seguito.</span><span class="sxs-lookup"><span data-stu-id="fd25a-225">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="fd25a-226">Tempo</span><span class="sxs-lookup"><span data-stu-id="fd25a-226">Time</span></span>                                                          | <span data-ttu-id="fd25a-227">**\_DateTime CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-227">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="fd25a-228">Ora codificata UTC</span><span class="sxs-lookup"><span data-stu-id="fd25a-228">UTC Coded Time</span></span>                                                | <span data-ttu-id="fd25a-229">**\_DateTime CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-229">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="fd25a-230">Stringa Unicode</span><span class="sxs-lookup"><span data-stu-id="fd25a-230">Unicode String</span></span>                                                | <span data-ttu-id="fd25a-231">**\_stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="fd25a-231">**CIM\_STRING**</span></span>                                                         |



 

<span data-ttu-id="fd25a-232">La sintassi della stringa di ottetto, che fa riferimento a una matrice di valori **Uint8** , presenta un problema quando viene eseguito il mapping a WMI, perché WMI consente le proprietà dei tipi **Uint8** e le matrici di **Uint8**, mentre Active Directory consente le proprietà di tipo stringa ottetto, nonché matrici di stringa ottetto.</span><span class="sxs-lookup"><span data-stu-id="fd25a-232">The Octet String syntax, which refers to an array of **uint8** values, presents a problem when mapped to WMI because WMI allows properties of types **uint8** and arrays of **uint8**, whereas Active Directory allows properties of type Octet String as well as arrays of Octet String.</span></span>

<span data-ttu-id="fd25a-233">Nell'esempio seguente viene illustrata la classe del provider di servizi directory utilizzata per eseguire il mapping di una matrice di proprietà di tipo stringa ottetto.</span><span class="sxs-lookup"><span data-stu-id="fd25a-233">The following example shows the Directory Services Provider class that is used to map an array of Octet String type properties.</span></span>

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

<span data-ttu-id="fd25a-234">WMI esegue il mapping di tutte le stringhe ottetto Active Directory valori di proprietà a istanze incorporate di **Uint8Array**.</span><span class="sxs-lookup"><span data-stu-id="fd25a-234">WMI maps all Octet String Active Directory property values to embedded instances of **Uint8Array**.</span></span> <span data-ttu-id="fd25a-235">Analogamente, WMI esegue il mapping di matrici di stringa ottetto a matrici di oggetti **Uint8Array** incorporati.</span><span class="sxs-lookup"><span data-stu-id="fd25a-235">Similarly, WMI maps arrays of Octet String to arrays of embedded **Uint8Array** objects.</span></span>

<span data-ttu-id="fd25a-236">Nell'esempio seguente vengono illustrate le classi di cui è stato eseguito il mapping da WMI per DN-Binary e DN-String i valori delle proprietà DS.</span><span class="sxs-lookup"><span data-stu-id="fd25a-236">The following example shows the classes that are mapped by WMI to DN-Binary and DN-String DS property values.</span></span>

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

<span data-ttu-id="fd25a-237">Nella tabella seguente viene elencato il mapping tra il resto delle proprietà dell'interfaccia dell'attributo Active Directory e i qualificatori di proprietà WMI.</span><span class="sxs-lookup"><span data-stu-id="fd25a-237">The following table lists how WMI maps the rest of the Active Directory attribute interface properties to WMI property qualifiers.</span></span>



| <span data-ttu-id="fd25a-238">Attributo Active Directory-nome proprietà</span><span class="sxs-lookup"><span data-stu-id="fd25a-238">Active Directory attribute-property name</span></span> | <span data-ttu-id="fd25a-239">Qualificatore WMI</span><span class="sxs-lookup"><span data-stu-id="fd25a-239">WMI Qualifier</span></span>       | <span data-ttu-id="fd25a-240">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fd25a-240">Data type</span></span>    | <span data-ttu-id="fd25a-241">Informazioni sul mapping</span><span class="sxs-lookup"><span data-stu-id="fd25a-241">Mapping information</span></span>                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| <span data-ttu-id="fd25a-242">**Sintassi degli attributi**</span><span class="sxs-lookup"><span data-stu-id="fd25a-242">**Attribute-Syntax**</span></span>                     | <span data-ttu-id="fd25a-243">**AttributeSyntax**</span><span class="sxs-lookup"><span data-stu-id="fd25a-243">**AttributeSyntax**</span></span> | <span data-ttu-id="fd25a-244">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="fd25a-244">**VT\_BSTR**</span></span> | <span data-ttu-id="fd25a-245">Mappato dalla rappresentazione di stringa dell'OID.</span><span class="sxs-lookup"><span data-stu-id="fd25a-245">Mapped from the string representation of the OID.</span></span> |
| <span data-ttu-id="fd25a-246">**Nome comune**</span><span class="sxs-lookup"><span data-stu-id="fd25a-246">**Common-Name**</span></span>                          | <span data-ttu-id="fd25a-247">**CN**</span><span class="sxs-lookup"><span data-stu-id="fd25a-247">**CN**</span></span>              | <span data-ttu-id="fd25a-248">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="fd25a-248">**VT\_BSTR**</span></span> | <span data-ttu-id="fd25a-249">Mappata dal valore stringa.</span><span class="sxs-lookup"><span data-stu-id="fd25a-249">Mapped from the string value.</span></span>                     |
| <span data-ttu-id="fd25a-250">**Solo sistema**</span><span class="sxs-lookup"><span data-stu-id="fd25a-250">**System-Only**</span></span>                          | <span data-ttu-id="fd25a-251">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="fd25a-251">**System**</span></span>          | <span data-ttu-id="fd25a-252">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="fd25a-252">**VT\_BOOL**</span></span> | <span data-ttu-id="fd25a-253">Mappato da un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="fd25a-253">Mapped from the Boolean value.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="fd25a-254">WMI esegue il mapping di tutti i qualificatori di Active Directory con le `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` versioni del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="fd25a-254">WMI maps all Active Directory qualifiers with the `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` qualifier flavors.</span></span>

 

## <a name="association-classes"></a><span data-ttu-id="fd25a-255">Classi Association</span><span class="sxs-lookup"><span data-stu-id="fd25a-255">Association Classes</span></span>

<span data-ttu-id="fd25a-256">Il servizio directory è essenzialmente un archivio gerarchico di oggetti.</span><span class="sxs-lookup"><span data-stu-id="fd25a-256">The Directory Service is essentially a hierarchical store of objects.</span></span> <span data-ttu-id="fd25a-257">Gli oggetti che possono essere visualizzati a un livello non foglia nella gerarchia sono detti "contenitori".</span><span class="sxs-lookup"><span data-stu-id="fd25a-257">Those objects that can appear at a nonleaf level in the hierarchy are called "containers".</span></span> <span data-ttu-id="fd25a-258">La struttura di questa gerarchia è ulteriormente controllata dalle proprietà "poss-superiors" e "System-poss-superiors" di una classe nello schema.</span><span class="sxs-lookup"><span data-stu-id="fd25a-258">The structure of this hierarchy is further controlled by the "Poss-Superiors" and "System-Poss-Superiors" properties of a class in the schema.</span></span> <span data-ttu-id="fd25a-259">Insieme, specificano il set di classi le cui istanze possono essere contenute all'interno di un'istanza di una classe contenitore.</span><span class="sxs-lookup"><span data-stu-id="fd25a-259">These, taken together, specify the set of classes whose instances can be contained within an instance of a container class.</span></span>

<span data-ttu-id="fd25a-260">Nell'esempio seguente viene modellata un'associazione CIM come istanza della classe di associazione statica di [**dominio DS \_ \_ \_ contenuto della classe LDAP**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).</span><span class="sxs-lookup"><span data-stu-id="fd25a-260">The following example models a CIM association as instances of the static association class [**DS\_LDAP\_Class\_Containment**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).</span></span>

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

<span data-ttu-id="fd25a-261">Il provider della classe Association supporta i metodi [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) e [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) .</span><span class="sxs-lookup"><span data-stu-id="fd25a-261">The association class provider supports the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods.</span></span>

 

