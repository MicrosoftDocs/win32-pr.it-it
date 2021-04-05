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
# <a name="understanding-the-property-description-schema"></a>Informazioni sullo schema della descrizione della proprietà

In questo argomento viene presentato lo schema di descrizione della proprietà utilizzato dal sistema di proprietà della shell.

L'introduzione di nuove funzionalità per Windows Vista e versioni successive richiede che il sistema di proprietà della shell esistente venga esteso a:

-   Supporta un sistema completo ed estendibile per la descrizione delle proprietà che fornisce informazioni sulle proprietà, inclusi i nomi visualizzati, il tipo, il tipo di visualizzazione, il comportamento di ordinamento e gruppo e altri attributi necessari per presentare e operare sulle proprietà.
-   Supportare un elenco di titoli di tipi di proprietà (combinati con l'interfaccia utente che possono modificare tali tipi in visualizzazioni diverse, ad esempio ListView, riquadro di anteprima, finestre di dialogo delle proprietà e così via) che possono essere associati a varie proprietà.
-   Specificare gli elenchi di descrizioni delle proprietà, che definiscono il set di proprietà visualizzato in diverse visualizzazioni.
-   Fornire un'interfaccia semplificata, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), in modo che i gestori di proprietà possano essere scritti più facilmente, quindi le proprietà possono essere rese permanente nei file.
-   Supporto per gestori di proprietà non file per esporre le proprietà nella visualizzazione.

Queste funzionalità sono realizzate in un'architettura che fornisce l'accesso astratto alle proprietà di un elemento della shell. Questa astrazione è denominata sistema di proprietà della shell.

-   [Che cos'è lo schema della descrizione della proprietà?](#what-is-the-property-description-schema)
-   [Perché usare uno schema?](#why-use-a-schema)
-   [Quali sono le principali parti dello schema?](#what-are-the-major-schema-parts)
-   [Modifiche per Windows 7](#changes-for-windows-7)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-the-property-description-schema"></a>Che cos'è lo schema della descrizione della proprietà?

Il sottosistema dello schema è costituito dagli elementi seguenti:

-   Uno o più file di schema con estensione propdesc che definiscono descrizioni di proprietà. Lo schema della descrizione della proprietà è definito in una raccolta di file di XML Schema (usando l'estensione di file propdesc) in fase di esecuzione nel sistema. Questi file vengono caricati in modo lazy quando una parte del sistema di proprietà li richiede.
-   Cache dello schema in memoria utilizzata per archiviare i file di schema analizzati, che includono tutte le descrizioni delle proprietà introdotte nel sottosistema. Non è necessario analizzare nuovamente i file di configurazione con estensione propdesc che descrivono lo schema. Per ulteriori informazioni, vedere [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)e [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).
-   Oggetto sottosistema che implementa [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), che viene utilizzato per ottenere o utilizzare descrizioni di proprietà.
-   Oggetto sottosistema che implementa [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), che viene usato per informare e operare in base a una descrizione della proprietà.
-   Oggetto sottosistema che implementa [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), che viene usato come raccolta di descrizioni di proprietà.

> [!Note]  
> È necessario aggiungere `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` all'elemento dello schema radice dei file con estensione propdesc.

 

## <a name="why-use-a-schema"></a>Perché usare uno schema?

Le proprietà, di per sé, non sono indipendenti dai tipi. Un componente può assegnare un valore numerico alla proprietà System. Author o a un indicatore di data e [**ora**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) della proprietà System. Music. AlbumTitle e, senza ulteriori imposizione o indicazioni, gli archivi delle proprietà lo consentiranno. Quindi, abbiamo bisogno di una nozione di "schematizzare" delle proprietà, che ci porta al sottosistema dello schema.

## <a name="what-are-the-major-schema-parts"></a>Quali sono le principali parti dello schema?

Lo schema della descrizione della proprietà usato dal sistema di proprietà della shell è costituito da un singolo elemento [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) , oltre che da un attributo *SchemaVersion* , che indica la versione di questo formato di definizione dello schema. Nota: il valore deve essere "1,0".


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



[PropertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) è costituito da uno o più elementi [PropertyDescription](./propdesc-schema-propertydescription.md) , oltre che dagli attributi del *server di pubblicazione* e del *prodotto* .


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



Un [PropertyDescription](./propdesc-schema-propertydescription.md) è costituito da [un searchInfo](./propdesc-schema-searchinfo.md) e da zero o da uno o più elementi [labelInfo](./propdesc-schema-labelinfo.md), [TypeInfo](./propdesc-schema-typeinfo.md)e [displayInfo](./propdesc-schema-displayinfo.md) , oltre che dagli attributi *FormatID*, *propid*, *propstr* e *Name* .

Deve essere presente un elemento [PropertyDescription](./propdesc-schema-propertydescription.md) per ogni nome di proprietà canonico univoco che deve essere disponibile nel sistema. Gli attributi di stringa hanno un limite di 512 caratteri. I valori più lunghi di 512 caratteri vengono troncati.


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



## <a name="changes-for-windows-7"></a>Modifiche per Windows 7

Lo schema della descrizione della proprietà è stato modificato per Windows 7. Si tratta di modifiche non di rilievo. Se un elemento o attributo di proprietà non è più supportato in Windows 7, il sistema operativo Windows 7 ignora gli attributi o gli elementi di Windows Vista. Analogamente, Windows Vista ignora anche i nuovi elementi o attributi delle proprietà di Windows 7.

Tuttavia, l'aggiornamento delle proprietà personalizzate per Windows 7 è consigliato per un'esperienza utente migliore e coerente.

Di seguito sono riportati nuovi elementi e attributi:

-   elementi [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) e [relatedProperty](./propdesc-schema-relatedproperty.md)
-   elemento [Image](./propdesc-schema-image.md)
-   attributo mnemonicos dell'elemento [searchInfo](./propdesc-schema-searchinfo.md)
-   attributo mnemonicos dell'elemento [enum](./propdesc-schema-enum.md)
-   attributo searchRawValue dell'elemento [TypeInfo](./propdesc-schema-typeinfo.md)

Gli elementi e gli attributi seguenti sono stati modificati:

-   elementi [enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md)e [enumRange](./propdesc-schema-enumrange.md)
-   elemento [drawControl](./propdesc-schema-drawcontrol.md)
-   elemento [editControl](./propdesc-schema-editcontrol.md)
-   attributo propID dell'elemento [PropertyDescription](./propdesc-schema-propertydescription.md)
-   attributo columnIndexType dell'elemento [searchInfo](./propdesc-schema-searchinfo.md)

Sono stati rimossi gli elementi e gli attributi seguenti:

-   elemento [queryControl](./propdesc-schema-querycontrol.md)
-   attributo Queryable dell'elemento [TypeInfo](./propdesc-schema-typeinfo.md)
-   attributo includeInFullTextQuery dell'elemento [TypeInfo](./propdesc-schema-typeinfo.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> </dl>

 

 
