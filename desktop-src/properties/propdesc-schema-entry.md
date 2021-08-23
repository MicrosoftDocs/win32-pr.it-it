---
description: Questo argomento presenta lo schema di descrizione della proprietà usato dal sistema di proprietà shell.
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: Informazioni sullo schema di descrizione delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85dbb0f20c5c4a206069e80aa308a26908bf90ee0d00cf80712a342e834411e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554561"
---
# <a name="understanding-the-property-description-schema"></a>Informazioni sullo schema di descrizione delle proprietà

Questo argomento presenta lo schema di descrizione della proprietà usato dal sistema di proprietà shell.

L'introduzione di nuove funzionalità per Windows Vista e versioni successive richiedeva l'estensione del sistema di proprietà shell esistente a:

-   Supporto di un sistema di descrizione delle proprietà avanzate ed estendibile che fornisce informazioni sulle proprietà, inclusi nomi visualizzati, tipo, tipo di visualizzazione, comportamento di ordinamento e raggruppamento e altri attributi necessari per presentare e operare sulle proprietà.
-   Supporto di un elenco di tipi di proprietà (combinati con l'interfaccia utente che possono modificare tali tipi in visualizzazioni diverse, ad esempio la visualizzazione elenco, il riquadro di anteprima, le finestre di dialogo delle proprietà e così via) che possono essere associati a varie proprietà.
-   Fornire elenchi di descrizione delle proprietà, che definiscono il set di proprietà visualizzate in diverse visualizzazioni.
-   Fornire un'interfaccia semplificata, [**IPropertyStore,**](/windows/win32/api/propsys/nn-propsys-ipropertystore)in modo che i gestori delle proprietà possano essere scritti più facilmente e in modo che le proprietà possano essere rese persistenti nei file.
-   Supporto per i gestori di proprietà non di file per esporre le proprietà nella visualizzazione.

Queste funzionalità vengono ottenute in un'architettura che fornisce accesso astratto alle proprietà di un elemento della shell. Questa astrazione è denominata sistema di proprietà shell.

-   [Che cos'è lo schema di descrizione della proprietà?](#what-is-the-property-description-schema)
-   [Perché usare uno schema?](#why-use-a-schema)
-   [Quali sono le parti principali dello schema?](#what-are-the-major-schema-parts)
-   [Modifiche per Windows 7](#changes-for-windows-7)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-the-property-description-schema"></a>Che cos'è lo schema di descrizione della proprietà?

Il sottosistema dello schema è costituito dai seguenti elementi:

-   Uno o più file di schema propdesc che definiscono le descrizioni delle proprietà. Lo schema di descrizione della proprietà viene definito in una raccolta di file di XML Schema (con estensione propdesc) in fase di esecuzione nel sistema. Questi file vengono caricati lazy quando una parte del sistema di proprietà li richiede.
-   Cache dello schema in memoria utilizzata per archiviare i file di schema analizzati, che includono tutte le descrizioni delle proprietà introdotte nel sottosistema. Non è necessario eseguire nuovamente l'analisi dei file di configurazione propdesc che descrivono lo schema. Per altre informazioni, vedere [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)e [**PSRefreshPropertySchema.**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema)
-   Oggetto del sottosistema che implementa [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), usato per ottenere o usare le descrizioni delle proprietà.
-   Oggetto del sottosistema che implementa [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), che viene usato per informare e operare in base a una descrizione della proprietà.
-   Oggetto del sottosistema che [**implementa IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), che viene usato come raccolta di descrizioni delle proprietà.

> [!Note]  
> È necessario aggiungere `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` all'elemento radice dello schema dei file con estensione propdesc.

 

## <a name="why-use-a-schema"></a>Perché usare uno schema?

Le proprietà, di per sé, non sono indipendente dai tipi. Un componente può assegnare un valore numerico alla proprietà System.Author o un indicatore di data [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) al sistema. Musica. La proprietà AlbumTitle e, senza ulteriori imposizioni o indicazioni, gli archivi di proprietà lo consentiranno. Quindi, era necessaria una nozione per "schematizzare" le proprietà, che porta al sottosistema dello schema.

## <a name="what-are-the-major-schema-parts"></a>Quali sono le parti principali dello schema?

Lo schema di descrizione della proprietà usato dal sistema di proprietà Shell è costituito da un singolo elemento [propertyDescriptionList,](./propdesc-schema-propertydescriptionlist.md) nonché da un *attributo schemaVersion,* che indica la versione di questo formato di definizione dello schema. Nota: il valore deve essere "1.0".


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



[propertyDescriptionList è](./propdesc-schema-propertydescriptionlist.md) costituito da uno o più [elementi propertyDescription,](./propdesc-schema-propertydescription.md) nonché da *attributi publisher* *e product.*


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



PropertyDescription [è](./propdesc-schema-propertydescription.md) costituito da un [elemento searchInfo](./propdesc-schema-searchinfo.md) e da zero o da un elemento [labelInfo](./propdesc-schema-labelinfo.md), [typeInfo](./propdesc-schema-typeinfo.md)e [displayInfo,](./propdesc-schema-displayinfo.md) nonché da attributi *formatID*, *propID*, *propstr* e *name.*

Deve essere presente un [elemento propertyDescription](./propdesc-schema-propertydescription.md) per ogni nome di proprietà canonico univoco che deve essere disponibile nel sistema. Gli attributi di stringa hanno un limite di 512 caratteri. I valori di lunghezza superiore a 512 caratteri vengono troncati.


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

Lo schema di descrizione della proprietà è stato modificato per Windows 7. Si tratta di modifiche non di rilievo. Se un attributo o un elemento proprietà non è più supportato in Windows 7, il sistema operativo Windows 7 ignora l'elemento o gli attributi Windows Vista. Analogamente, Windows Vista ignora anche i Windows 7 elementi o attributi di proprietà.

È tuttavia consigliabile aggiornare le proprietà personalizzate Windows 7 per un'esperienza utente migliore e più coerente.

Di seguito sono riportati nuovi elementi e attributi:

-   [elementi relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) [e relatedProperty](./propdesc-schema-relatedproperty.md)
-   [elemento image](./propdesc-schema-image.md)
-   Attributo mnemonics [dell'elemento searchInfo](./propdesc-schema-searchinfo.md)
-   Attributo mnemonics [dell'elemento enum](./propdesc-schema-enum.md)
-   Attributo searchRawValue [dell'elemento typeInfo](./propdesc-schema-typeinfo.md)

Gli elementi e gli attributi seguenti sono stati modificati:

-   [Elementi enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md)ed [enumRange](./propdesc-schema-enumrange.md)
-   [elemento drawControl](./propdesc-schema-drawcontrol.md)
-   [editControl -](./propdesc-schema-editcontrol.md) elemento
-   Attributo propID [dell'elemento propertyDescription](./propdesc-schema-propertydescription.md)
-   Attributo columnIndexType [dell'elemento searchInfo](./propdesc-schema-searchinfo.md)

Gli elementi e gli attributi seguenti sono stati rimossi:

-   [elemento queryControl](./propdesc-schema-querycontrol.md)
-   Attributo isQueryable [dell'elemento typeInfo](./propdesc-schema-typeinfo.md)
-   Attributo includeInFullTextQuery [dell'elemento typeInfo](./propdesc-schema-typeinfo.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[proprietàDescrizione](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[Datetimeformat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[DrawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> </dl>

 

 
