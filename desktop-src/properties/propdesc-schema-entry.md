---
description: In questo argomento viene presentato lo schema di descrizione della proprietà utilizzato dal sistema di proprietà della shell.
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: Informazioni sullo schema della descrizione della proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51d9e7c2b6fb4b599f977c0c49ad1cb2514fe8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049787"
---
# <a name="understanding-the-property-description-schema"></a><span data-ttu-id="ed328-103">Informazioni sullo schema della descrizione della proprietà</span><span class="sxs-lookup"><span data-stu-id="ed328-103">Understanding the Property Description Schema</span></span>

<span data-ttu-id="ed328-104">In questo argomento viene presentato lo schema di descrizione della proprietà utilizzato dal sistema di proprietà della shell.</span><span class="sxs-lookup"><span data-stu-id="ed328-104">This topic introduces the property description schema used by the Shell property system.</span></span>

<span data-ttu-id="ed328-105">L'introduzione di nuove funzionalità per Windows Vista e versioni successive richiede che il sistema di proprietà della shell esistente venga esteso a:</span><span class="sxs-lookup"><span data-stu-id="ed328-105">The introduction of new features for Windows Vista and later required that the existing Shell property system be extended to:</span></span>

-   <span data-ttu-id="ed328-106">Supporta un sistema completo ed estendibile per la descrizione delle proprietà che fornisce informazioni sulle proprietà, inclusi i nomi visualizzati, il tipo, il tipo di visualizzazione, il comportamento di ordinamento e gruppo e altri attributi necessari per presentare e operare sulle proprietà.</span><span class="sxs-lookup"><span data-stu-id="ed328-106">Support a rich and extensible property description system that provides information about properties including display names, type, display type, sort and group behavior, and other attributes needed to present and operate over the properties.</span></span>
-   <span data-ttu-id="ed328-107">Supportare un elenco di titoli di tipi di proprietà (combinati con l'interfaccia utente che possono modificare tali tipi in visualizzazioni diverse, ad esempio ListView, riquadro di anteprima, finestre di dialogo delle proprietà e così via) che possono essere associati a varie proprietà.</span><span class="sxs-lookup"><span data-stu-id="ed328-107">Support a stock list of property types (combined with UI that can edit those types in different views like the listview, preview pane, property dialogs, and so on) that can be associated with various properties.</span></span>
-   <span data-ttu-id="ed328-108">Specificare gli elenchi di descrizioni delle proprietà, che definiscono il set di proprietà visualizzato in diverse visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="ed328-108">Supply property description lists, which define the set of properties displayed in various views.</span></span>
-   <span data-ttu-id="ed328-109">Fornire un'interfaccia semplificata, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), in modo che i gestori di proprietà possano essere scritti più facilmente, quindi le proprietà possono essere rese permanente nei file.</span><span class="sxs-lookup"><span data-stu-id="ed328-109">Provide a simplified interface, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), so property handlers can be written more easily and so properties can be persisted to files.</span></span>
-   <span data-ttu-id="ed328-110">Supporto per gestori di proprietà non file per esporre le proprietà nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ed328-110">Support for non-file property handlers to expose properties in the view.</span></span>

<span data-ttu-id="ed328-111">Queste funzionalità sono realizzate in un'architettura che fornisce l'accesso astratto alle proprietà di un elemento della shell.</span><span class="sxs-lookup"><span data-stu-id="ed328-111">These features are achieved on an architecture that provides abstract access to the properties of a Shell item.</span></span> <span data-ttu-id="ed328-112">Questa astrazione è denominata sistema di proprietà della shell.</span><span class="sxs-lookup"><span data-stu-id="ed328-112">This abstraction is called the Shell property system.</span></span>

-   [<span data-ttu-id="ed328-113">Che cos'è lo schema della descrizione della proprietà?</span><span class="sxs-lookup"><span data-stu-id="ed328-113">What Is the Property Description Schema?</span></span>](#what-is-the-property-description-schema)
-   [<span data-ttu-id="ed328-114">Perché usare uno schema?</span><span class="sxs-lookup"><span data-stu-id="ed328-114">Why Use a Schema?</span></span>](#why-use-a-schema)
-   [<span data-ttu-id="ed328-115">Quali sono le principali parti dello schema?</span><span class="sxs-lookup"><span data-stu-id="ed328-115">What Are the Major Schema Parts?</span></span>](#what-are-the-major-schema-parts)
-   [<span data-ttu-id="ed328-116">Modifiche per Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed328-116">Changes for Windows 7</span></span>](#changes-for-windows-7)
-   [<span data-ttu-id="ed328-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed328-117">Related topics</span></span>](#related-topics)

## <a name="what-is-the-property-description-schema"></a><span data-ttu-id="ed328-118">Che cos'è lo schema della descrizione della proprietà?</span><span class="sxs-lookup"><span data-stu-id="ed328-118">What Is the Property Description Schema?</span></span>

<span data-ttu-id="ed328-119">Il sottosistema dello schema è costituito dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ed328-119">The schema subsystem consists of the following:</span></span>

-   <span data-ttu-id="ed328-120">Uno o più file di schema con estensione propdesc che definiscono descrizioni di proprietà.</span><span class="sxs-lookup"><span data-stu-id="ed328-120">One or more .propdesc schema files that define property descriptions.</span></span> <span data-ttu-id="ed328-121">Lo schema della descrizione della proprietà è definito in una raccolta di file di XML Schema (usando l'estensione di file propdesc) in fase di esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ed328-121">The property description schema is defined in a collection of XML schema files (using the .propdesc file extension) at runtime on the system.</span></span> <span data-ttu-id="ed328-122">Questi file vengono caricati in modo lazy quando una parte del sistema di proprietà li richiede.</span><span class="sxs-lookup"><span data-stu-id="ed328-122">These files are lazy-loaded when a part of the property system requires them.</span></span>
-   <span data-ttu-id="ed328-123">Cache dello schema in memoria utilizzata per archiviare i file di schema analizzati, che includono tutte le descrizioni delle proprietà introdotte nel sottosistema.</span><span class="sxs-lookup"><span data-stu-id="ed328-123">An in-memory schema cache used to store the parsed schema files, which include all property descriptions introduced to the subsystem.</span></span> <span data-ttu-id="ed328-124">Non è necessario analizzare nuovamente i file di configurazione con estensione propdesc che descrivono lo schema.</span><span class="sxs-lookup"><span data-stu-id="ed328-124">There is no need to reparse the .propdesc config files that describe the schema.</span></span> <span data-ttu-id="ed328-125">Per ulteriori informazioni, vedere [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)e [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span><span class="sxs-lookup"><span data-stu-id="ed328-125">For more information, see [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema), and [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span></span>
-   <span data-ttu-id="ed328-126">Oggetto sottosistema che implementa [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), che viene utilizzato per ottenere o utilizzare descrizioni di proprietà.</span><span class="sxs-lookup"><span data-stu-id="ed328-126">A subsystem object that implements [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), which is used to obtain or work with property descriptions.</span></span>
-   <span data-ttu-id="ed328-127">Oggetto sottosistema che implementa [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), che viene usato per informare e operare in base a una descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ed328-127">A subsystem object that implements [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), which is used to inform and operate based on a property description.</span></span>
-   <span data-ttu-id="ed328-128">Oggetto sottosistema che implementa [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), che viene usato come raccolta di descrizioni di proprietà.</span><span class="sxs-lookup"><span data-stu-id="ed328-128">A subsystem object that implements [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which is used as a collection of property descriptions.</span></span>

> [!Note]  
> <span data-ttu-id="ed328-129">È necessario aggiungere `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` all'elemento dello schema radice dei file con estensione propdesc.</span><span class="sxs-lookup"><span data-stu-id="ed328-129">You must add `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` to the root schema element of your .propdesc files.</span></span>

 

## <a name="why-use-a-schema"></a><span data-ttu-id="ed328-130">Perché usare uno schema?</span><span class="sxs-lookup"><span data-stu-id="ed328-130">Why Use a Schema?</span></span>

<span data-ttu-id="ed328-131">Le proprietà, di per sé, non sono indipendenti dai tipi.</span><span class="sxs-lookup"><span data-stu-id="ed328-131">Properties, by themselves, are not type-safe.</span></span> <span data-ttu-id="ed328-132">Un componente può assegnare un valore numerico alla proprietà System. Author o a un indicatore di data e [**ora**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) della proprietà System. Music. AlbumTitle e, senza ulteriori imposizione o indicazioni, gli archivi delle proprietà lo consentiranno.</span><span class="sxs-lookup"><span data-stu-id="ed328-132">A component can assign a numerical value to the System.Author property, or a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) date-stamp to the System.Music.AlbumTitle property, and, without any further enforcement or guidance, the property stores will allow it.</span></span> <span data-ttu-id="ed328-133">Quindi, abbiamo bisogno di una nozione di "schematizzare" delle proprietà, che ci porta al sottosistema dello schema.</span><span class="sxs-lookup"><span data-stu-id="ed328-133">So, we needed a notion to "schematize" the properties, which brings us to the schema subsystem.</span></span>

## <a name="what-are-the-major-schema-parts"></a><span data-ttu-id="ed328-134">Quali sono le principali parti dello schema?</span><span class="sxs-lookup"><span data-stu-id="ed328-134">What Are the Major Schema Parts?</span></span>

<span data-ttu-id="ed328-135">Lo schema della descrizione della proprietà usato dal sistema di proprietà della shell è costituito da un singolo elemento [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) , oltre che da un attributo *SchemaVersion* , che indica la versione di questo formato di definizione dello schema.</span><span class="sxs-lookup"><span data-stu-id="ed328-135">The property description schema used by the Shell property system is composed of a single [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) element, as well as a *schemaVersion* attribute, which indicates the version of this schema definition format.</span></span> <span data-ttu-id="ed328-136">Nota: il valore deve essere "1,0".</span><span class="sxs-lookup"><span data-stu-id="ed328-136">Note: value must be "1.0".</span></span>


```
<!-- schema -->
    <xs:element name="schema">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescriptionList" minOccurs="1" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="schemaVersion"  type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



<span data-ttu-id="ed328-137">[PropertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) è costituito da uno o più elementi [PropertyDescription](./propdesc-schema-propertydescription.md) , oltre che dagli attributi del *server di pubblicazione* e del *prodotto* .</span><span class="sxs-lookup"><span data-stu-id="ed328-137">The [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) is composed of one or more [propertyDescription](./propdesc-schema-propertydescription.md) elements, as well as *publisher* and *product* attributes.</span></span>


```
<!-- propertyDescriptionList -->
    <xs:element name="propertyDescriptionList">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product"   type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



<span data-ttu-id="ed328-138">Un [PropertyDescription](./propdesc-schema-propertydescription.md) è costituito da [un searchInfo](./propdesc-schema-searchinfo.md) e da zero o da uno o più elementi [labelInfo](./propdesc-schema-labelinfo.md), [TypeInfo](./propdesc-schema-typeinfo.md)e [displayInfo](./propdesc-schema-displayinfo.md) , oltre che dagli attributi *FormatID*, *propid*, *propstr* e *Name* .</span><span class="sxs-lookup"><span data-stu-id="ed328-138">A [propertyDescription](./propdesc-schema-propertydescription.md) is composed of one [searchInfo](./propdesc-schema-searchinfo.md) and zero or one [labelInfo](./propdesc-schema-labelinfo.md), [typeInfo](./propdesc-schema-typeinfo.md), and [displayInfo](./propdesc-schema-displayinfo.md) elements, as well as *formatID*, *propID*, *propstr*, and *name* attributes.</span></span>

<span data-ttu-id="ed328-139">Deve essere presente un elemento [PropertyDescription](./propdesc-schema-propertydescription.md) per ogni nome di proprietà canonico univoco che deve essere disponibile nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ed328-139">There should be one [propertyDescription](./propdesc-schema-propertydescription.md) element for every unique canonical property name that is intended to be available in the system.</span></span> <span data-ttu-id="ed328-140">Gli attributi di stringa hanno un limite di 512 caratteri.</span><span class="sxs-lookup"><span data-stu-id="ed328-140">The string attributes have a limit of 512 characters.</span></span> <span data-ttu-id="ed328-141">I valori più lunghi di 512 caratteri vengono troncati.</span><span class="sxs-lookup"><span data-stu-id="ed328-141">Values longer than 512 characters are truncated.</span></span>


```
<!-- propertyDescription -->
    <xs:element name="propertyDescription">
      <xs:complexType>
        <xs:all>
          <xs:element name="description"    type="xs:string" minOccurs="0" maxOccurs="1"/>
          <xs:element ref="searchInfo"   minOccurs="1" maxOccurs="1"/>
          <xs:element ref="labelInfo"    minOccurs="0" maxOccurs="1"/>
          <xs:element ref="typeInfo"     minOccurs="0" maxOccurs="1"/>
          <xs:element ref="displayInfo"  minOccurs="0" maxOccurs="1"/>
        </xs:all>
        <xs:attribute name="formatID"  type="upcase-uuid" use="required""/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required""/>
        <xs:attribute name="name"      type="canonical-name" use="required"/>
      </xs:complexType>
    </xs:element>
```



## <a name="changes-for-windows-7"></a><span data-ttu-id="ed328-142">Modifiche per Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed328-142">Changes for Windows 7</span></span>

<span data-ttu-id="ed328-143">Lo schema della descrizione della proprietà è stato modificato per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ed328-143">The property description schema has been changed for Windows 7.</span></span> <span data-ttu-id="ed328-144">Si tratta di modifiche non di rilievo.</span><span class="sxs-lookup"><span data-stu-id="ed328-144">These are non-breaking changes.</span></span> <span data-ttu-id="ed328-145">Se un elemento o attributo di proprietà non è più supportato in Windows 7, il sistema operativo Windows 7 ignora gli attributi o gli elementi di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed328-145">If a property element or attribute is no longer supported in Windows 7, the Windows 7 operating system ignores the Windows Vista element or attributes.</span></span> <span data-ttu-id="ed328-146">Analogamente, Windows Vista ignora anche i nuovi elementi o attributi delle proprietà di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ed328-146">Similarly, Windows Vista ignores new Windows 7 property elements or attributes as well.</span></span>

<span data-ttu-id="ed328-147">Tuttavia, l'aggiornamento delle proprietà personalizzate per Windows 7 è consigliato per un'esperienza utente migliore e coerente.</span><span class="sxs-lookup"><span data-stu-id="ed328-147">However, updating custom properties for Windows 7 is recommended for a better and more consistent user experience.</span></span>

<span data-ttu-id="ed328-148">Di seguito sono riportati nuovi elementi e attributi:</span><span class="sxs-lookup"><span data-stu-id="ed328-148">The following are new elements and attributes:</span></span>

-   <span data-ttu-id="ed328-149">elementi [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) e [relatedProperty](./propdesc-schema-relatedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-149">[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) and [relatedProperty](./propdesc-schema-relatedproperty.md) elements</span></span>
-   <span data-ttu-id="ed328-150">elemento [Image](./propdesc-schema-image.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-150">[image](./propdesc-schema-image.md) element</span></span>
-   <span data-ttu-id="ed328-151">attributo mnemonicos dell'elemento [searchInfo](./propdesc-schema-searchinfo.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-151">mnemonics attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>
-   <span data-ttu-id="ed328-152">attributo mnemonicos dell'elemento [enum](./propdesc-schema-enum.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-152">mnemonics attribute of the [enum](./propdesc-schema-enum.md) element</span></span>
-   <span data-ttu-id="ed328-153">attributo searchRawValue dell'elemento [TypeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-153">searchRawValue attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

<span data-ttu-id="ed328-154">Gli elementi e gli attributi seguenti sono stati modificati:</span><span class="sxs-lookup"><span data-stu-id="ed328-154">The following elements and attributes have changed:</span></span>

-   <span data-ttu-id="ed328-155">elementi [enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md)e [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-155">[enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md), and [enumRange](./propdesc-schema-enumrange.md) elements</span></span>
-   <span data-ttu-id="ed328-156">elemento [drawControl](./propdesc-schema-drawcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-156">[drawControl](./propdesc-schema-drawcontrol.md) element</span></span>
-   <span data-ttu-id="ed328-157">elemento [editControl](./propdesc-schema-editcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-157">[editControl](./propdesc-schema-editcontrol.md) element</span></span>
-   <span data-ttu-id="ed328-158">attributo propID dell'elemento [PropertyDescription](./propdesc-schema-propertydescription.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-158">propID attribute of the [propertyDescription](./propdesc-schema-propertydescription.md) element</span></span>
-   <span data-ttu-id="ed328-159">attributo columnIndexType dell'elemento [searchInfo](./propdesc-schema-searchinfo.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-159">columnIndexType attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>

<span data-ttu-id="ed328-160">Sono stati rimossi gli elementi e gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ed328-160">The following elements and attributes have been removed:</span></span>

-   <span data-ttu-id="ed328-161">elemento [queryControl](./propdesc-schema-querycontrol.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-161">[queryControl](./propdesc-schema-querycontrol.md) element</span></span>
-   <span data-ttu-id="ed328-162">attributo Queryable dell'elemento [TypeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-162">isQueryable attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>
-   <span data-ttu-id="ed328-163">attributo includeInFullTextQuery dell'elemento [TypeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="ed328-163">includeInFullTextQuery attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed328-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ed328-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed328-165">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="ed328-165">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="ed328-166">searchInfo</span><span class="sxs-lookup"><span data-stu-id="ed328-166">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="ed328-167">labelInfo</span><span class="sxs-lookup"><span data-stu-id="ed328-167">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="ed328-168">typeInfo</span><span class="sxs-lookup"><span data-stu-id="ed328-168">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="ed328-169">displayInfo</span><span class="sxs-lookup"><span data-stu-id="ed328-169">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="ed328-170">stringFormat</span><span class="sxs-lookup"><span data-stu-id="ed328-170">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="ed328-171">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="ed328-171">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="ed328-172">numberFormat</span><span class="sxs-lookup"><span data-stu-id="ed328-172">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="ed328-173">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ed328-173">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="ed328-174">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="ed328-174">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="ed328-175">drawControl</span><span class="sxs-lookup"><span data-stu-id="ed328-175">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="ed328-176">editControl</span><span class="sxs-lookup"><span data-stu-id="ed328-176">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="ed328-177">filterControl</span><span class="sxs-lookup"><span data-stu-id="ed328-177">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="ed328-178">queryControl</span><span class="sxs-lookup"><span data-stu-id="ed328-178">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="ed328-179">image</span><span class="sxs-lookup"><span data-stu-id="ed328-179">image</span></span>](./propdesc-schema-image.md)
</dt> </dl>

 

 
