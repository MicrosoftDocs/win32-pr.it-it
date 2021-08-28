---
description: Specifica le informazioni sul tipo di una proprietà.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: Typeinfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a70c6eeaee63bcb99ee19217ccff5d3ff7086a2
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632169"
---
# <a name="typeinfo"></a>Typeinfo

Specifica le informazioni sul tipo di una proprietà. Deve essere presente un solo [elemento typeInfo]() per [ogni propertyDescription.](./propdesc-schema-propertydescription.md) Questo elemento è stato modificato per Windows 7.

Se sono presenti più elementi, viene usato l'ultimo. Se non [viene specificato alcun elemento typeInfo,]() le impostazioni dell'attributo predefinite vengono applicate alla descrizione della proprietà.

## <a name="syntax-for-windows-7"></a>Sintassi per Windows 7


```
<!-- typeInfo for Windows 7-->
<xs:element name="typeInfo">
    <xs:complexType>
        <xs:attribute name="type" default="Any">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Any"/>
                    <xs:enumeration value="Null"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Byte"/>
                    <xs:enumeration value="Buffer"/>
                    <xs:enumeration value="Int16"/>
                    <xs:enumeration value="UInt16"/>
                    <xs:enumeration value="Int32"/>
                    <xs:enumeration value="UInt32"/>
                    <xs:enumeration value="Int64"/>
                    <xs:enumeration value="UInt64"/>
                    <xs:enumeration value="Double"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Guid"/>
                    <xs:enumeration value="Blob"/>
                    <xs:enumeration value="Stream"/>
                    <xs:enumeration value="Clipboard"/>
                    <xs:enumeration value="Object"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="groupingRange">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Discrete"/>
                    <xs:enumeration value="Alphanumeric"/>
                    <xs:enumeration value="Size"/>
                    <xs:enumeration value="Date"/>
                    <xs:enumeration value="Dynamic"/>
                    <xs:enumeration value="Percent"/>
                    <xs:enumeration value="Enumerated"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isInnate" type="xs:boolean" default="false"/>
        <xs:attribute name="canBePurged" type="xs:boolean"/>
        <xs:attribute name="multipleValues" type="xs:boolean" default="false"/>
        <xs:attribute name="isGroup" type="xs:boolean" default="false"/>
        <xs:attribute name="aggregationType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="First"/>
                    <xs:enumeration value="Sum"/>
                    <xs:enumeration value="Average"/>
                    <xs:enumeration value="DateRange"/>
                    <xs:enumeration value="Union"/>
                    <xs:enumeration value="Maximum"/>
                    <xs:enumeration value="Minimum"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="isTreeProperty" type="xs:boolean" default="false"/>
        <xs:attribute name="isViewable" type="xs:boolean" default="false"/>
        <xs:attribute name="isQueryable" type="xs:boolean" default="false"/>
        <xs:attribute name="includeInFullTextQuery" type="xs:boolean" default="false"/>
        <xs:attribute name="searchRawValue" type="xs:boolean" default="false"/>
        <xs:attribute name="conditionType">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="None"/>
                    <xs:enumeration value="String"/>
                    <xs:enumeration value="Number"/>
                    <xs:enumeration value="DateTime"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Size"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="defaultOperation">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Equal"/>
                    <xs:enumeration value="NotEqual"/>
                    <xs:enumeration value="LessThan"/>
                    <xs:enumeration value="GreaterThan"/>
                    <xs:enumeration value="Contains"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                   | Elementi figlio |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | Nessuno           |



 

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>type</td>
<td>Pubblica. facoltativo. Il valore predefinito &quot; è Any &quot; . Indica il tipo della proprietà. Di seguito sono riportati i tipi validi e i relativi tipi variant associati vengono recuperati da <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a>. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Qualsiasi</td>
<td>Valore predefinito. Il sottosistema della proprietà non imponi né forza il valore della proprietà. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> restituisce VT_NULL. I fornitori di software indipendenti (ISV) sono fortemente invitati a fornire un tipo anziché eseguire il fall back su questa impostazione predefinita.</td>
</tr>
<tr class="even">
<td>Null</td>
<td>Non esiste alcun valore per questa proprietà. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription::GetPropertyType</strong></a> restituisce VT_NULL.</td>
</tr>
<tr class="odd">
<td>Stringa</td>
<td>Il valore deve essere un VT_LPWSTR, ovvero una stringa Unicode terminata da un riferimento Null.</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Il valore deve essere un VT_BOOL, ovvero un valore booleano.</td>
</tr>
<tr class="odd">
<td>Byte</td>
<td>Il valore deve essere un VT_UI1, ovvero un byte.</td>
</tr>
<tr class="even">
<td>Buffer</td>
<td>Il valore deve essere un VT_UI1 | VT_VECTOR buffer di byte.</td>
</tr>
<tr class="odd">
<td>Int16</td>
<td>Il valore deve essere un VT_I2, ovvero un intero a 16 bit.</td>
</tr>
<tr class="even">
<td>UInt16</td>
<td>Il valore deve essere un VT_UI2, ovvero un intero senza segno a 16 bit.</td>
</tr>
<tr class="odd">
<td>Int32</td>
<td>Il valore deve essere un VT_I4, ovvero un intero a 32 bit.</td>
</tr>
<tr class="even">
<td>UInt32</td>
<td>Il valore deve essere un VT_UI4, ovvero un intero senza segno a 32 bit.</td>
</tr>
<tr class="odd">
<td>Int64</td>
<td>Il valore deve essere un VT_I8, ovvero un numero intero a 64 bit.</td>
</tr>
<tr class="even">
<td>UInt64</td>
<td>Il valore deve essere un VT_UI8, ovvero un intero senza segno a 64 bit.</td>
</tr>
<tr class="odd">
<td>Double</td>
<td>Il valore deve essere un VT_R8, ovvero un valore double.</td>
</tr>
<tr class="even">
<td>Datetime</td>
<td>Il valore deve essere un VT_FILETIME, ovvero <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>fileTIME</strong></a>.</td>
</tr>
<tr class="odd">
<td>Guid</td>
<td>Il valore deve essere un VT_CLSID, ovvero un identificatore di classe (CLSID).</td>
</tr>
<tr class="even">
<td>BLOB</td>
<td>Il valore deve essere un VT_BLOB, ovvero byte con prefisso di lunghezza.</td>
</tr>
<tr class="odd">
<td>Stream</td>
<td>Il valore deve essere un VT_STREAM, ovvero un oggetto che implementa <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream.</strong></a></td>
</tr>
<tr class="even">
<td>Appunti</td>
<td>Il valore deve essere un VT_CF, ovvero un formato degli Appunti.</td>
</tr>
<tr class="odd">
<td>Oggetto</td>
<td>Il valore deve essere un VT_UNKNOWN, ovvero un oggetto che implementa <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown.</strong></a></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>groupingRange</td>
<td>facoltativo. Il valore predefinito &quot; è Discrete &quot; . Specifica la modalità di visualizzazione della proprietà quando una visualizzazione viene raggruppata in base a questa proprietà. Una volta impostati qui, questi valori vengono recuperati <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>da IPropertyDescription::GetGroupingRange</strong></a>. Di seguito sono riportati i tipi validi.

<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Discrete</td>
<td>Valore predefinito. Visualizza i singoli valori.</td>
</tr>
<tr class="even">
<td>Alfanumerico</td>
<td>Visualizza intervalli alfanumerici statici per i valori.</td>
</tr>
<tr class="odd">
<td>Dimensione</td>
<td>Visualizza gli intervalli di dimensioni statiche per i valori.</td>
</tr>
<tr class="even">
<td>Data</td>
<td>Visualizza i gruppi mese/anno. Impostazione predefinita per le proprietà di tipo = &quot; DateTime &quot; .</td>
</tr>
<tr class="odd">
<td>TimeRelative</td>
<td>Viene visualizzato in gruppi relativi all'ora.</td>
</tr>
<tr class="even">
<td>Dynamic</td>
<td>Visualizza gli intervalli creati dinamicamente per i valori.</td>
</tr>
<tr class="odd">
<td>Percentuale</td>
<td>Visualizza i bucket di percentuale.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>isInnate</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;. Specifica se la proprietà è considerata innata. Una proprietà innata è una proprietà calcolata dal contenuto di un file o da altre risorse o sistemi. Ad esempio, System.Size è una proprietà innata fornita dal file system; La modifica del valore della proprietà in e di per sé non esegue alcuna operazione. Altri esempi sono System.Image.Dimensions e System.Document. PageCount, calcolato dai programmi in base al contenuto del file, non in base a un'impostazione modificabile dall'utente. L'impostazione di isInnate= &quot; true indica che l'utente non può modificare questa proprietà direttamente tramite un controllo &quot; proprietà. Questo valore esegue il mapping al flag PDTF_ISINNATE definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</td>
</tr>
<tr class="even">
<td>canBePurged</td>
<td><strong>Windows Vista solo con Service Pack 1 (SP1) e versioni successive.</strong> Pubblica. facoltativo. Se impostato su &quot; &quot; true, consente l'eliminazione di una proprietà innata. Le proprietà innate, calcolate da altre proprietà, sono di sola lettura per definizione. Il valore predefinito per questo attributo dipende dal <em>valore isInnate.</em>

<table>
<thead>
<tr class="header">
<th>isInnate</th>
<th>Valore predefinito canBePurged</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>true</td>
<td>false</td>
</tr>
<tr class="even">
<td>false</td>
<td>true</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Una proprietà il cui <em>valore isInnate</em> è false (vale a dire che la proprietà è di lettura/scrittura) non può anche impostare il &quot; valore &quot; <em>canBePurged</em> su &quot; &quot; false. Questa restrizione viene applicata dal sistema operativo.
</blockquote>
</div>
<div>
 
</div>
<p>Sebbene questo attributo sia stato introdotto in Windows Vista con Service Pack 1 (SP1), un file con estensione propdesc che include questo attributo è compatibile con Windows Vista prima di Windows Vista con SP1. <em>L'attributo canBePurged</em> viene semplicemente ignorato in tale situazione.</p></td>
</tr>
<tr class="odd">
<td>multipleValues</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;. Specifica se questa proprietà può avere più valori. Questo valore esegue il mapping al flag PDTF_MULTIPLEVALUES definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>. Ciò influisce anche sulla VT_VECTOR è OR sul VALORE VARTYPE del valore della proprietà.</td>
</tr>
<tr class="even">
<td>isGroup</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;. Specifica se la proprietà è un'intestazione di gruppo. Un'intestazione di gruppo viene usata esclusivamente negli elenchi proplist, non ha alcun valore, non viene mai archiviata in un file e deve avere anche <typeInfo type=&quot;Null&quot;> . Alcune ui nel sistema usano proplist per indicare la sequenza delle proprietà da visualizzare. Questi proplist possono includere riferimenti alle intestazioni di gruppo (ad esempio, System.PropGroup.Camera), che indica all'interfaccia utente di avviare una nuova sezione di gruppo (ad esempio, &quot; Camera Impostazioni &quot; ). Una descrizione della proprietà con isGroup= true deve specificare , in caso contrario &quot; non è una proprietà &quot; <labelInfo label=&quot;Some localized label&quot;> utile. Questo valore esegue il mapping al flag PDTF_ISGROUP definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</td>
</tr>
<tr class="odd">
<td>aggregationType</td>
<td>Pubblica. facoltativo. Il valore predefinito &quot; è &quot; Default. Specifica la modalità di visualizzazione delle proprietà di aggregazione quando vengono selezionati più elementi. Una volta impostati qui, questi valori vengono recuperati da <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription::GetAggregationType</strong></a> <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>come</strong></a>PROPDESC_AGGREGATION_TYPE . Di seguito sono riportati i tipi validi.

<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Predefinito</td>
<td>Valore predefinito. Visualizza un <strong>segnaposto Con più valori</strong> nell'interfaccia utente. Si tratta dell'impostazione predefinita se <em>il tipo è</em> incompatibile con l'elemento <em>aggregationType specificato.</em></td>
</tr>
<tr class="even">
<td>Primo</td>
<td>Visualizza il valore della proprietà del primo elemento nella selezione o nell'insieme.</td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>Visualizza la somma dei valori numerici. Utile per proprietà quali System.Media.Duration o System.Size. Questo valore non è compatibile con i tipi non numerici.</td>
</tr>
<tr class="even">
<td>Media</td>
<td>Visualizza la media dei valori numerici. Utile per proprietà come System.Rating. Questo valore non è compatibile con i tipi non numerici.</td>
</tr>
<tr class="odd">
<td>DateRange</td>
<td>Visualizza un intervallo di date. Utile per proprietà come System.Photo.DateTaken. Questo valore non è compatibile con nessun elemento eccetto type= &quot; DateTime &quot; ed è l'impostazione predefinita per le proprietà di quel tipo.</td>
</tr>
<tr class="even">
<td>Union</td>
<td>Visualizza un'unione di tutti i valori nella selezione o nell'insieme. L'ordine in cui vengono visualizzati i valori non è definito. Questo valore è il valore predefinito per le proprietà di tipo &quot; = String &quot; e multipleValues= &quot; &quot; true.</td>
</tr>
<tr class="odd">
<td>Massimo</td>
<td>Visualizza il valore massimo nella raccolta. Utile per proprietà come System.DateModified. Non compatibile con tipi non numerici o non di data.</td>
</tr>
<tr class="even">
<td>Minimo</td>
<td>Visualizza il valore minimo nella raccolta. Non compatibile con tipi non numerici o non di data.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>isTreeProperty</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>isViewable</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;. Specifica se questa proprietà deve essere visualizzabile per l'utente. Ad esempio, l'interfaccia utente di Selezione colonne mostra solo le proprietà con isViewable= &quot; &quot; true. L'eccezione è l'interfaccia utente basata su un proplist, che mostrerà sempre la proprietà . Se si dispone di una proprietà destinata solo a distinguere i dati tra due oggetti e che non deve mai essere visualizzata dall'utente, questo attributo deve essere false. Questo valore esegue il mapping al flag PDTF_ISVIEWABLE definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</td>
</tr>
<tr class="even">
<td>isQueryable</td>
<td>Windows Solo Vista. Non supportato in Windows 7 e versioni successive. Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;. Specifica se questa proprietà deve essere disponibile nell'interfaccia utente Generatore di query ricerca. Una proprietà deve avere isViewable= &quot; true &quot; prima che isQueryable= &quot; true venga &quot; rispettato. Questo valore esegue il mapping al flag PDTF_ISQUERYABLE definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription::GetTypeFlags</strong></a>.</td>
</tr>
<tr class="odd">
<td>searchRawValue</td>
<td><strong>Windows 7 e versioni successive.</strong> Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>includeInFullTextQuery</td>
<td>Windows Solo Vista. Non supportato in Windows 7 e versioni successive. Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>conditionType</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot; String &quot; . Specifica un hint per l'interfaccia utente Generatore di query ricerca in modo che possa determinare l'elenco di possibili operatori di condizione all'interno di un predicato. Di seguito sono riportati i valori riconosciuti. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Stringa</td>
<td>Valore predefinito. Verranno usati gli operatori seguenti: è , non è , , , , , inizia con , termina con &quot; &quot; &quot; &quot; &quot; &lt; &quot; &quot; &gt; &quot; &quot; <= &quot; &quot; >= &quot; &quot; , contiene , non contiene , è simile &quot; a &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Numero</td>
<td>Impostazione predefinita per le proprietà numeriche. Verranno usati gli operatori seguenti: uguale a , diverso da , è minore di , è maggiore di , è minore o uguale a , è maggiore o &quot; &quot; uguale a &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; .</td>
</tr>
<tr class="odd">
<td>Datetime</td>
<td>Impostazione predefinita per le proprietà di tipo = &quot; DateTime &quot; . Verranno usati gli operatori seguenti: è , non è , è prima di , è dopo , è prima di , ma include , è &quot; &quot; dopo ma &quot; include &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; .</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Impostazione predefinita per le proprietà di tipo = &quot; Boolean &quot; . Uguale a Number.</td>
</tr>
<tr class="odd">
<td>Dimensione</td>
<td>Uguale a Number.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>defaultOperation</td>
<td>Pubblica. facoltativo. Il valore predefinito &quot; è Uguale &quot; a . Specifica un hint per lo strumento Generatore di query ricerca in modo che possa determinare l'operatore predefinito. I valori possibili sono i seguenti:

<table>
<thead>
<tr class="header">
<th>valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Uguale a</td>
<td>Valore predefinito. Indica un valore equivalente.</td>
</tr>
<tr class="even">
<td>NotEqual</td>
<td>Indica che non è equivalente.</td>
</tr>
<tr class="odd">
<td>LessThan</td>
<td>Indica un valore minore di.</td>
</tr>
<tr class="even">
<td>GreaterThan</td>
<td>Impostazione predefinita per le proprietà di conditionType= &quot; &quot; Size. Indica un valore maggiore di.</td>
</tr>
<tr class="odd">
<td>Contiene</td>
<td>Impostazione predefinita per le proprietà di conditionType= &quot; String &quot; . Indica l'inclusione.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
