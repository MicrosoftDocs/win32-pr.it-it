---
description: Specifica le informazioni sul tipo di una proprietà.
ms.assetid: ae1f8835-ef6c-42bb-b44f-ad374337a012
title: typeInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa783a606066163fd8b17f53ef8a0fe2da44e539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310108"
---
# <a name="typeinfo"></a>typeInfo

Specifica le informazioni sul tipo di una proprietà. Deve essere presente un solo elemento [TypeInfo]() per ogni [PropertyDescription](./propdesc-schema-propertydescription.md). Questo elemento è stato modificato per Windows 7.

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [TypeInfo]() , le impostazioni predefinite degli attributi vengono applicate alla descrizione della proprietà.

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
| [propertyDescription](./propdesc-schema-propertydescription.md) | nessuno           |



 

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>Pubblica. facoltativo. Il valore predefinito è &quot; Any &quot; . Indica il tipo della proprietà. Di seguito sono riportati i tipi validi e i tipi Variant associati vengono recuperati da <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: GetPropertyType</strong></a>. 
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
<td>Valore predefinito. Il sottosistema di proprietà non impone né forza il valore della proprietà. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: GetPropertyType</strong></a> Restituisce VT_NULL. I fornitori di software indipendenti (ISV) sono vivamente invitati a fornire un tipo anziché eseguire il fallback su questa impostazione predefinita.</td>
</tr>
<tr class="even">
<td>Null</td>
<td>Non esiste alcun valore per questa proprietà. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertytype"><strong>IPropertyDescription:: GetPropertyType</strong></a> Restituisce VT_NULL.</td>
</tr>
<tr class="odd">
<td>string</td>
<td>Il valore deve essere un VT_LPWSTR, ovvero una stringa Unicode terminata da un riferimento null.</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Il valore deve essere un VT_BOOL, ovvero un valore booleano.</td>
</tr>
<tr class="odd">
<td>Byte</td>
<td>Il valore deve essere un VT_UI1, che è un byte.</td>
</tr>
<tr class="even">
<td>Buffer</td>
<td>Il valore deve essere un VT_UI1 | VT_VECTOR buffer di byte.</td>
</tr>
<tr class="odd">
<td>Int16</td>
<td>Il valore deve essere un VT_I2, ovvero un Integer a 16 bit.</td>
</tr>
<tr class="even">
<td>UInt16</td>
<td>Il valore deve essere un VT_UI2, ovvero una Unsigned Integer a 16 bit.</td>
</tr>
<tr class="odd">
<td>Int32</td>
<td>Il valore deve essere un VT_I4, ovvero un intero a 32 bit.</td>
</tr>
<tr class="even">
<td>UInt32</td>
<td>Il valore deve essere un VT_UI4, ovvero una Unsigned Integer a 32 bit.</td>
</tr>
<tr class="odd">
<td>Int64</td>
<td>Il valore deve essere un VT_I8, ovvero un intero a 64 bit.</td>
</tr>
<tr class="even">
<td>UInt64</td>
<td>Il valore deve essere un VT_UI8, ovvero una Unsigned Integer a 64 bit.</td>
</tr>
<tr class="odd">
<td>Double</td>
<td>Il valore deve essere un VT_R8, che è un valore Double.</td>
</tr>
<tr class="even">
<td>Datetime</td>
<td>Il valore deve essere un VT_FILETIME, che è un <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a>.</td>
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
<td>Il valore deve essere un VT_STREAM, ovvero un oggetto che implementa <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a>.</td>
</tr>
<tr class="even">
<td>Appunti</td>
<td>Il valore deve essere un VT_CF, che è un formato degli Appunti.</td>
</tr>
<tr class="odd">
<td>Oggetto</td>
<td>Il valore deve essere un VT_UNKNOWN, ovvero un oggetto che implementa <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>groupingRange</td>
<td>facoltativo. Il valore predefinito è &quot; discreto &quot; . Specifica la modalità di visualizzazione della proprietà quando una visualizzazione viene raggruppata in base a questa proprietà. Una volta impostati qui, questi valori vengono recuperati da <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getgroupingrange"><strong>IPropertyDescription:: GetGroupingRange</strong></a>. Di seguito sono riportati i tipi validi.

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
<td>Visualizza gli intervalli alfanumerici statici per i valori.</td>
</tr>
<tr class="odd">
<td>Dimensione</td>
<td>Visualizza gli intervalli di dimensioni statiche per i valori.</td>
</tr>
<tr class="even">
<td>Data</td>
<td>Visualizza i gruppi mese/anno. Valore predefinito per le proprietà di tipo = &quot; DateTime &quot; .</td>
</tr>
<tr class="odd">
<td>TimeRelative</td>
<td>Viene visualizzato nei gruppi relativi al tempo.</td>
</tr>
<tr class="even">
<td>Dynamic</td>
<td>Visualizza gli intervalli creati dinamicamente per i valori.</td>
</tr>
<tr class="odd">
<td>Percentuale</td>
<td>Visualizza i bucket percentuali.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>innata</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;. Specifica se la proprietà è considerata innata. Una proprietà innata è una proprietà calcolata dal contenuto di un file o da altri sistemi o risorse. System. size, ad esempio, è una proprietà innata fornita dal file system; la modifica del valore della proprietà in e di per sé non esegue alcuna operazione. Altri esempi sono System. image. Dimensions e System.Document. PageCount, che vengono calcolate da programmi basati sul contenuto del file, non in base a un'impostazione modificabile dall'utente. L'impostazione di innate = &quot; true &quot; indica che l'utente non può modificare direttamente questa proprietà tramite un controllo proprietà. Questo valore esegue il mapping al flag di PDTF_ISINNATE definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="even">
<td>canBePurged</td>
<td><strong>Windows Vista con Service Pack 1 (SP1) e versioni successive</strong>. Pubblica. facoltativo. Se impostato su &quot; true &quot; , consente di eliminare una proprietà innata. Le proprietà innate, che vengono calcolate da altre proprietà, sono di sola lettura per definizione. Il valore predefinito di questo attributo dipende dal valore di <em>innate</em> .

<table>
<thead>
<tr class="header">
<th>innata</th>
<th>Valore predefinito di canBePurged</th>
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
Una proprietà il cui valore <em>innate</em> è &quot; false &quot; (ovvero la proprietà è di lettura/scrittura) non può inoltre impostare il valore <em>canBePurged</em> su &quot; false &quot; . Questa restrizione viene applicata dal sistema operativo.
</blockquote>
</div>
<div>
 
</div>
<p>Anche se questo attributo è stato introdotto in Windows Vista con Service Pack 1 (SP1), un file con estensione propdesc che include questo attributo è compatibile con Windows Vista prima di Windows Vista con SP1. In questa situazione, l'attributo <em>canBePurged</em> viene semplicemente ignorato.</p></td>
</tr>
<tr class="odd">
<td>multipleValues</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;. Specifica se la proprietà può avere più valori. Questo valore esegue il mapping al flag di PDTF_MULTIPLEVALUES definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>. Ciò influisce anche sul fatto che VT_VECTOR sia o a un VARTYPE del valore della proprietà.</td>
</tr>
<tr class="even">
<td>isGroup</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;. Specifica se la proprietà è un'intestazione di gruppo. Un'intestazione di gruppo viene utilizzata rigorosamente in proplists, non ha alcun valore, non viene mai archiviata in un file e deve avere anche <typeInfo type=&quot;Null&quot;> . Alcune interfacce utente del sistema usano proplists per indicare la sequenza delle proprietà da visualizzare. Questi proplists possono includere riferimenti a intestazioni di gruppo (ad esempio, System. PropGroup. camera), che indicano all'interfaccia utente di avviare una nuova sezione del gruppo (ad esempio, &quot; le impostazioni della fotocamera &quot; ). Una descrizione della proprietà con il valore di ' Group = &quot; true &quot; ' deve specificare un oggetto <labelInfo label=&quot;Some localized label&quot;> ; in caso contrario, non è una proprietà utile. Questo valore esegue il mapping al flag di PDTF_ISGROUP definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="odd">
<td>aggregationType</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot; default &quot; . Specifica la modalità di visualizzazione delle proprietà di aggregazione quando vengono selezionati più elementi. Una volta impostati qui, questi valori vengono recuperati da <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getaggregationtype"><strong>IPropertyDescription:: GetAggregationType</strong></a> come <a href="/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type"><strong>PROPDESC_AGGREGATION_TYPE</strong></a>. Di seguito sono riportati i tipi validi.

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
<td>Valore predefinito. Visualizza un segnaposto con <strong>più valori</strong> nell'interfaccia utente. Si tratta dell'impostazione predefinita se il <em>tipo</em> non è compatibile con il <em>aggregationType</em>specificato.</td>
</tr>
<tr class="even">
<td>First (Primo)</td>
<td>Consente di visualizzare il valore della proprietà del primo elemento della selezione o della raccolta.</td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>Visualizza la somma dei valori numerici. Utile per proprietà quali System. Media. Duration o System. size. Questo valore non è compatibile con i tipi non numerici.</td>
</tr>
<tr class="even">
<td>Media</td>
<td>Visualizza la media dei valori numerici. Utile per proprietà quali System. rating. Questo valore non è compatibile con i tipi non numerici.</td>
</tr>
<tr class="odd">
<td>DateRange</td>
<td>Visualizza un intervallo di date. Utile per proprietà quali System. Photo. DateTaken. Questo valore non è compatibile con qualsiasi elemento tranne Type = &quot; DateTime &quot; ed è il valore predefinito per le proprietà di quel tipo.</td>
</tr>
<tr class="even">
<td>Union</td>
<td>Consente di visualizzare un'Unione di tutti i valori della selezione o della raccolta. L'ordine in cui vengono visualizzati i valori non è definito. Questo valore è l'impostazione predefinita per le proprietà di tipo = &quot; String &quot; e multipleValues = &quot; true &quot; .</td>
</tr>
<tr class="odd">
<td>Massimo</td>
<td>Consente di visualizzare il valore massimo nella raccolta. Utile per proprietà quali System. DateModified. Non è compatibile con i tipi non numerici o non di data.</td>
</tr>
<tr class="even">
<td>Minima</td>
<td>Consente di visualizzare il valore minimo nella raccolta. Non è compatibile con i tipi non numerici o non di data.</td>
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
<td>Visualizzabile</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;. Specifica se questa proprietà deve essere visibile all'utente. Ad esempio, l'interfaccia utente di selezione colonne Mostra solo le proprietà con l'oggetto visualizzabile = &quot; true &quot; . L'eccezione è l'interfaccia utente basata su un oggetto prop, che Mostra sempre la proprietà. Se si dispone di una proprietà che è destinata solo a eseguire la spola dei dati tra due oggetti e non è mai stata progettata per essere visualizzata dall'utente, questo attributo deve essere false. Questo valore esegue il mapping al flag di PDTF_ISVIEWABLE definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="even">
<td>Queryable</td>
<td>Solo Windows Vista. Non supportato in Windows 7 e versioni successive. Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;. Specifica se questa proprietà deve essere disponibile nell'interfaccia utente di ricerca Generatore di query. Una proprietà deve avere un valore di visualizzabile = &quot; true &quot; prima che &quot; venga rispettata l'esecuzione di Queryable = true &quot; . Questo valore esegue il mapping al flag di PDTF_ISQUERYABLE definito in <a href="/windows/win32/api/propsys/ne-propsys-propdesc_type_flags"><strong>PROPDESC_TYPE_FLAGS</strong></a> e usato in <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-gettypeflags"><strong>IPropertyDescription:: GetTypeFlags</strong></a>.</td>
</tr>
<tr class="odd">
<td>searchRawValue</td>
<td><strong>Windows 7 e versioni successive.</strong> Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>includeInFullTextQuery</td>
<td>Solo Windows Vista. Non supportato in Windows 7 e versioni successive. Pubblica. facoltativo. Il valore predefinito è &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>conditionType</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot; String &quot; . Specifica un hint per l'interfaccia utente di ricerca Generatore di query in modo che sia in grado di determinare l'elenco di possibili operatori di condizione all'interno di un predicato. Di seguito sono riportati i valori riconosciuti. 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>string</td>
<td>Valore predefinito. Verranno utilizzati gli operatori seguenti: &quot; è &quot; , non è,,,, &quot; &quot; &quot; &lt; &quot; &quot; &gt; &quot; &quot; <= &quot; &quot; >= &quot; , &quot; inizia con &quot; , &quot; termina con &quot; , &quot; Contains &quot; , &quot; non contiene &quot; , &quot; è simile a &quot; .</td>
</tr>
<tr class="even">
<td>Number</td>
<td>Valore predefinito per le proprietà numeriche. Verranno utilizzati gli operatori seguenti: &quot; uguale a, &quot; non uguale a, &quot; &quot; &quot; è minore di &quot; , &quot; è maggiore di &quot; , &quot; è minore o uguale a &quot; , &quot; è maggiore o uguale a &quot; .</td>
</tr>
<tr class="odd">
<td>Datetime</td>
<td>Valore predefinito per le proprietà di tipo = &quot; DateTime &quot; . Verranno utilizzati gli operatori seguenti: &quot; is &quot; , is &quot; Not &quot; , &quot; is before, is &quot; &quot; after &quot; , &quot; is before ma includes &quot; , is &quot; after ma includes &quot; .</td>
</tr>
<tr class="even">
<td>Boolean</td>
<td>Valore predefinito per le proprietà di tipo = &quot; Boolean &quot; . Uguale al numero.</td>
</tr>
<tr class="odd">
<td>Dimensione</td>
<td>Uguale al numero.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>defaultOperation</td>
<td>Pubblica. facoltativo. Il valore predefinito è &quot; uguale a &quot; . Specifica un hint per lo strumento Generatore di query di ricerca in modo che sia in grado di determinare l'operatore predefinito. I valori possibili sono i seguenti:

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
<td>Valore predefinito. Indica l'equivalente.</td>
</tr>
<tr class="even">
<td>NotEqual</td>
<td>Indica un valore diverso da.</td>
</tr>
<tr class="odd">
<td>LessThan</td>
<td>Indica minore di.</td>
</tr>
<tr class="even">
<td>GreaterThan</td>
<td>Impostazione predefinita per le proprietà di conditionType = &quot; size &quot; . Indica maggiore di.</td>
</tr>
<tr class="odd">
<td>Contiene</td>
<td>Impostazione predefinita per le proprietà di conditionType = &quot; String &quot; . Indica l'inclusione.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
