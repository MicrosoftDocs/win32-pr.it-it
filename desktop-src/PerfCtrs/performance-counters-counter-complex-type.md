---
description: Definisce un contatore.
ms.assetid: 8f1338c0-7ea6-4d0c-af71-51012973e4a0
title: Tipo complesso contatore
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d591d4c23b626eaf2e2bfb10b528ff7c054507df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312137"
---
# <a name="counter-complex-type"></a>Tipo complesso contatore

Definisce un contatore.

``` syntax
<xs:complexType name="counter">
    <xs:choice
        minOccurs="0"
        maxOccurs="1"
    >
        <xs:element name="counterAttributes"
            type="man:counterAttributes"
        >
            <xs:key name="uniqueCounterAttributeName">
                <xs:selector
                    xpath="./man:counterAttribute"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="id"
        type="man:UInt32Type"
        use="required"
     />
    <xs:attribute name="uri"
        type="xs:anyURI"
        use="required"
     />
    <xs:attribute name="name"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:maxLength
                    value="1023"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="description"
        type="xs:string"
        use="optional"
     />
    <xs:attribute name="type"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="perf_counter_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer"
                 />
                <xs:enumeration
                    value="perf_counter_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_large_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_100ns_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_obj_time_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_bulk_count"
                 />
                <xs:enumeration
                    value="perf_counter_text"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_sample_fraction"
                 />
                <xs:enumeration
                    value="perf_sample_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer_inv"
                 />
                <xs:enumeration
                    value="perf_sample_base"
                 />
                <xs:enumeration
                    value="perf_average_timer"
                 />
                <xs:enumeration
                    value="perf_average_base"
                 />
                <xs:enumeration
                    value="perf_average_bulk"
                 />
                <xs:enumeration
                    value="perf_obj_time_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_base"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_large_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_raw_base"
                 />
                <xs:enumeration
                    value="perf_large_raw_base"
                 />
                <xs:enumeration
                    value="perf_elapsed_time"
                 />
                <xs:enumeration
                    value="perf_counter_delta"
                 />
                <xs:enumeration
                    value="perf_counter_large_delta"
                 />
                <xs:enumeration
                    value="perf_precision_system_timer"
                 />
                <xs:enumeration
                    value="perf_precision_100ns_timer"
                 />
                <xs:enumeration
                    value="perf_precision_object_timer"
                 />
                <xs:enumeration
                    value="perf_counter_composite"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="baseID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="detailLevel"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="standard"
                 />
                <xs:enumeration
                    value="advanced"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="defaultScale"
        use="optional"
        default="0"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:integer"
            >
                <xs:minInclusive
                    value="-10"
                 />
                <xs:maxInclusive
                    value="10"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="aggregate"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="sum"
                 />
                <xs:enumeration
                    value="avg"
                 />
                <xs:enumeration
                    value="max"
                 />
                <xs:enumeration
                    value="min"
                 />
                <xs:enumeration
                    value="undefined"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="perfTimeID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="perfFreqID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="multiCounterID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="struct"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="field"
        type="man:CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento               | Tipo                                                                                 | Descrizione                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| **counterAttributes** | [**uomo: counterAttributes**](performance-counters-counterattributes-complex-type.md) | Elenca gli attributi univoci che specificano la modalità di visualizzazione dei dati del contatore in un'applicazione consumer.<br/> |



## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Tipo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>aggregate</td>

<td>Funzione di aggregazione da applicare se l'attributo <strong>instances</strong> del <a href="performance-counters-counterset-complex-type.md"><strong>contatore</strong></a> è GlobalAggregate, multipleAggregate o globalAggregateHistory. Di seguito sono riportate le possibili funzioni di aggregazione che è possibile applicare:<br/> <dl> <dt><span id="max"></span><span id="MAX"></span>Max</dt> <dd> Viene restituito il valore massimo del contatore.<br/> </dd> <dt><span id="min"></span><span id="MIN"></span>min</dt> <dd> Viene restituito il valore minimo del contatore.<br/> </dd> <dt><span id="avg"></span><span id="AVG"></span>AVG</dt> <dd> Viene restituito il valore medio del contatore.<br/> </dd> <dt><span id="sum"></span><span id="SUM"></span>somma</dt> <dd> Viene restituita la somma dei valori del contatore.<br/> </dd> <dt><span id="undefined"></span><span id="UNDEFINED"></span>non definito</dt> <dd> Non aggregare questo contatore.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>baseID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>uomo: UInt32Type</strong></a></td>
<td>Identificatore di un altro contatore nello stesso insieme di contatori, il cui valore viene utilizzato per calcolare il valore del contatore. I tipi di contatori seguenti richiedono un contatore di base:<br/> <dl> <dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> <dd> Richiede il contatore di base PERF_AVERAGE_BASE.<br/> </dd> <dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> <dd> Richiede il contatore di base PERF_AVERAGE_BASE.<br/> </dd> <dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> <dd> Richiede il contatore di base PERF_COUNTER_MULTI_BASE.<br/> </dd> <dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> <dd> Richiede il contatore di base PERF_LARGE_RAW_BASE.<br/> </dd> <dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> <dd> Richiede il contatore di base PERF_LARGE_RAW_BASE.<br/> </dd> <dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> <dd> Richiede il contatore di base PERF_RAW_BASE.<br/> </dd> <dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> <dd> Richiede il contatore di base PERF_SAMPLE_BASE.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td>defaultScale</td>

<td>Fattore di scala da applicare al valore del contatore (fattore * valore del contatore). Il valore predefinito è zero se non viene applicata alcuna scala. I valori validi sono compresi tra 10 e 10 (da 0,0000000001 a 1 miliardo). Se questo valore è zero, il valore di scala è 1; Se questo valore è 1, il valore della scala è 10. Se questo valore è 1, il valore della scala è. 10; E così via.<br/></td>
</tr>
<tr class="even">
<td>description</td>
<td><strong>xs:string</strong></td>
<td>Breve descrizione del contatore. Non è necessario specificare questo attributo se il contatore include l'attributo <a href="performance-counters-counterattribute-complex-type.md"><strong>NoDisplay</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td>detailLevel</td>

<td>Specifica i destinatari per i dettagli del contatore. Di seguito sono indicati i valori possibili:<br/> <dl> <dt><span id="standard"></span><span id="STANDARD"></span>standard</dt> <dd> Visualizza i dettagli sul contatore che un utente comune potrebbe comprendere.<br/> </dd> <dt><span id="advanced"></span><span id="ADVANCED"></span>avanzate</dt> <dd> Visualizza i dettagli sul contatore che solo un utente avanzato può comprendere.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>campo</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>uomo: CSymbolType</strong></a></td>
<td>Nome di un campo all'interno dello struct che contiene il valore del contatore. Questo attributo non è consentito per i provider in modalità utente.<br/></td>
</tr>
<tr class="odd">
<td>id</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>uomo: UInt32Type</strong></a></td>
<td>Numero univoco che identifica il contatore all'interno dell'insieme di contatori.<br/></td>
</tr>
<tr class="even">
<td>multiCounterID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>uomo: UInt32Type</strong></a></td>
<td>Identificatore di un altro contatore nello stesso insieme di contatori, il cui valore del moltiplicatore viene usato per calcolare il valore del contatore. I tipi di contatori seguenti richiedono un valore moltiplicatore. Il contatore a cui viene fatto riferimento deve essere di tipo PERF_COUNTER_RAWCOUNT.<br/>
<ul>
<li>PERF_COUNTER_MULTI_TIMER</li>
<li>PERF_COUNTER_MULTI_TIMER_INV</li>
<li>PERF_100NSEC_MULTI_TIMER</li>
<li>PERF_100NSEC_MULTI_TIMER_INV</li>
</ul></td>
</tr>
<tr class="odd">
<td>name</td>

<td>Nome del contatore. Il nome deve essere univoco e inferiore a 1.024 caratteri. Per il nome è prevista la distinzione tra maiuscole e minuscole. Non è necessario specificare questo attributo se il contatore include l'attributo <a href="performance-counters-counterattribute-complex-type.md"><strong>NoDisplay</strong></a> .<br/></td>
</tr>
<tr class="even">
<td>perfFreqID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>uomo: UInt32Type</strong></a></td>
<td>Identificatore di un altro contatore nello stesso insieme di contatori, il cui valore Frequency viene utilizzato per calcolare il valore del contatore. I tipi di contatori seguenti richiedono una frequenza. Il tipo di contatore PERF_COUNTER_LARGE_RAWCOUNT contiene il valore del timestamp.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="odd">
<td>perfTimeID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>uomo: UInt32Type</strong></a></td>
<td>Identificatore di un altro contatore nello stesso insieme di contatori, il cui valore timestamp viene utilizzato per calcolare il valore del contatore. I tipi di contatori seguenti richiedono un timestamp. Il tipo di contatore PERF_COUNTER_LARGE_RAWCOUNT contiene il valore del timestamp.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="even">
<td>struct</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>uomo: CSymbolType</strong></a></td>
<td>Nome di un elemento struct che contiene questo valore del contatore. Questo attributo non è consentito per i provider in modalità utente.<br/></td>
</tr>
<tr class="odd">
<td>simbolo</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>uomo: CSymbolType</strong></a></td>
<td>Nome simbolico che identifica il contatore. Lo strumento <a href="ctrpp.md">CTRPP</a> crea una costante che è possibile usare quando si chiamano funzioni che richiedono un identificatore del contatore (ad esempio, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>). Il nome della costante è il nome simbolico.<br/></td>
</tr>
<tr class="even">
<td>tipo</td>

<td>Nome del tipo di contatore. Per i valori possibili, vedere il blocco di sintassi precedente. Per informazioni dettagliate su ogni tipo, vedere <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">tipi di contatori</a> nella Guida alla distribuzione di Windows 2003. Il nome fa distinzione tra maiuscole e minuscole. <br/></td>
</tr>
<tr class="odd">
<td>Uri</td>
<td><strong>XS: anyURI</strong></td>
<td>Identificatore univoco della risorsa uniforme che consente agli utenti di recuperare i valori dei contatori da qualsiasi posizione.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Per garantire la compatibilità con le versioni precedenti, ogni contatore nell'insieme di contatori deve specificare gli stessi valori **perfFreqID** e **perfTimeID** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

