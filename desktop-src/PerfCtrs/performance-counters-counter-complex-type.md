---
description: Definisce un contatore.
ms.assetid: 8f1338c0-7ea6-4d0c-af71-51012973e4a0
title: Counter Complex Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 754b72d47e4fecbc5de3697cbec255251714885835a2ec429210c9ce5f489c77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793755"
---
# <a name="counter-complex-type"></a>Counter Complex Type

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
| **counterAttributes** | [**man:counterAttributes**](performance-counters-counterattributes-complex-type.md) | Elenca gli attributi univoci che specificano la modalità di visualizzazione dei dati del contatore in un'applicazione consumer.<br/> |



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

<td>Funzione di aggregazione da applicare se l'attributo <strong>instances</strong> di <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> è globalAggregate, multipleAggregate o globalAggregateHistory. Di seguito sono riportate le possibili funzioni di aggregazione che è possibile applicare:<br/> <dl> <dt><span id="max"></span><span id="MAX"></span>Massimo</dt> <dd> Viene restituito il valore massimo del contatore.<br/> </dd> <dt><span id="min"></span><span id="MIN"></span>Minimo</dt> <dd> Viene restituito il valore minimo del contatore.<br/> </dd> <dt><span id="avg"></span><span id="AVG"></span>Media</dt> <dd> Viene restituito il valore medio del contatore.<br/> </dd> <dt><span id="sum"></span><span id="SUM"></span>Somma</dt> <dd> Viene restituita la somma dei valori del contatore.<br/> </dd> <dt><span id="undefined"></span><span id="UNDEFINED"></span>Indefinito</dt> <dd> Non aggregare questo contatore.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>baseID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td>Identificatore di un altro contatore all'interno dello stesso insieme di contatori, il cui valore viene utilizzato per calcolare il valore del contatore. I tipi di contatore seguenti richiedono un contatore di base:<br/> <dl> <dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> <dd> Richiede il contatore PERF_AVERAGE_BASE base.<br/> </dd> <dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> <dd> Richiede il contatore PERF_AVERAGE_BASE base.<br/> </dd> <dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> <dd> Richiede il contatore PERF_COUNTER_MULTI_BASE base.<br/> </dd> <dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> <dd> Richiede il contatore PERF_LARGE_RAW_BASE base.<br/> </dd> <dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> <dd> Richiede il contatore PERF_LARGE_RAW_BASE base.<br/> </dd> <dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> <dd> Richiede il contatore PERF_RAW_BASE base.<br/> </dd> <dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> <dd> Richiede il contatore PERF_SAMPLE_BASE base.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td>defaultScale</td>

<td>Fattore di scala da applicare al valore del contatore (fattore * valore del contatore). Il valore predefinito è zero se non viene applicata alcuna scala. I valori validi sono da 10 a 10 (da 0,0000000001 a 10000000000). Se questo valore è zero, il valore della scala è 1; se questo valore è 1, il valore della scala è 10; se questo valore è 1, il valore di scala è 0,10; E così via.<br/></td>
</tr>
<tr class="even">
<td>description</td>
<td><strong>xs:string</strong></td>
<td>Breve descrizione del contatore. Non è necessario specificare questo attributo se il contatore include <a href="performance-counters-counterattribute-complex-type.md"><strong>l'attributo noDisplay.</strong></a><br/></td>
</tr>
<tr class="odd">
<td>detailLevel</td>

<td>Specifica il gruppo di destinatari per i dettagli del contatore. Di seguito sono indicati i valori possibili:<br/> <dl> <dt><span id="standard"></span><span id="STANDARD"></span>Standard</dt> <dd> Visualizzare i dettagli sul contatore che un utente tipico potrebbe comprendere.<br/> </dd> <dt><span id="advanced"></span><span id="ADVANCED"></span>Avanzate</dt> <dd> Visualizzare i dettagli sul contatore che solo un utente avanzato potrebbe comprendere.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>campo</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></td>
<td>Nome di un campo all'interno dello struct che contiene il valore del contatore. Questo attributo non è consentito per i provider in modalità utente.<br/></td>
</tr>
<tr class="odd">
<td>id</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td>Numero univoco che identifica il contatore all'interno dell'insieme di contatori.<br/></td>
</tr>
<tr class="even">
<td>multiCounterID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td>Identificatore di un altro contatore all'interno dello stesso insieme di contatori, il cui valore del moltiplicatore viene utilizzato per calcolare il valore del contatore. I tipi di contatore seguenti richiedono un valore moltiplicatore. Il contatore a cui si fa riferimento deve essere di tipo PERF_COUNTER_RAWCOUNT.<br/>
<ul>
<li>PERF_COUNTER_MULTI_TIMER</li>
<li>PERF_COUNTER_MULTI_TIMER_INV</li>
<li>PERF_100NSEC_MULTI_TIMER</li>
<li>PERF_100NSEC_MULTI_TIMER_INV</li>
</ul></td>
</tr>
<tr class="odd">
<td>name</td>

<td>Nome del contatore. Il nome deve essere univoco e contenere meno di 1.024 caratteri. Per il nome è prevista la distinzione tra maiuscole e minuscole. Non è necessario specificare questo attributo se il contatore include <a href="performance-counters-counterattribute-complex-type.md"><strong>l'attributo noDisplay.</strong></a><br/></td>
</tr>
<tr class="even">
<td>perfFreqID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td>Identificatore di un altro contatore all'interno dello stesso insieme di contatori, il cui valore di frequenza viene utilizzato per calcolare il valore del contatore. I tipi di contatore seguenti richiedono una frequenza. Il PERF_COUNTER_LARGE_RAWCOUNT tipo di contatore contiene il valore del timestamp.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="odd">
<td>perfTimeID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td>Identificatore di un altro contatore all'interno dello stesso insieme di contatori, il cui valore del timestamp viene utilizzato per calcolare il valore del contatore. I tipi di contatore seguenti richiedono un timestamp. Il PERF_COUNTER_LARGE_RAWCOUNT tipo di contatore contiene il valore del timestamp.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="even">
<td>struct</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></td>
<td>Nome di un elemento struct che contiene questo valore del contatore. Questo attributo non è consentito per i provider in modalità utente.<br/></td>
</tr>
<tr class="odd">
<td>simbolo</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></td>
<td>Nome simbolico che identifica il contatore. Lo <a href="ctrpp.md">strumento CTRPP</a> crea una costante che è possibile usare quando si chiamano funzioni che richiedono un identificatore di contatore ( ad <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>esempio, PerfIncrementULongCounterValue</strong></a>). Il nome della costante è il nome simbolico.<br/></td>
</tr>
<tr class="even">
<td>tipo</td>

<td>Nome del tipo di contatore. Per i valori possibili, vedere il blocco di sintassi precedente. Per informazioni dettagliate su ogni tipo, vedere <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Counter Types</a> (Tipi di contatori) nella Windows 2003 Deployment Guide (Guida alla distribuzione di Windows 2003). Il nome fa distinzione tra maiuscole e minuscole e usa lettere minuscole. <br/></td>
</tr>
<tr class="odd">
<td>Uri</td>
<td><strong>xs:anyURI</strong></td>
<td>Uniform Resource Identifier univoco che consente agli utenti di recuperare i valori dei contatori da qualsiasi posizione.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Per garantire la compatibilità con le versioni precedenti, ogni contatore nell'insieme di contatori deve specificare gli stessi valori **perfFreqID** **e perfTimeID.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

