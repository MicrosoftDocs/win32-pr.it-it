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
# <a name="counter-complex-type"></a><span data-ttu-id="0c193-103">Tipo complesso contatore</span><span class="sxs-lookup"><span data-stu-id="0c193-103">counter Complex Type</span></span>

<span data-ttu-id="0c193-104">Definisce un contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-104">Defines a counter.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="0c193-105">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0c193-105">Child elements</span></span>



| <span data-ttu-id="0c193-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="0c193-106">Element</span></span>               | <span data-ttu-id="0c193-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c193-107">Type</span></span>                                                                                 | <span data-ttu-id="0c193-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c193-108">Description</span></span>                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c193-109">**counterAttributes**</span><span class="sxs-lookup"><span data-stu-id="0c193-109">**counterAttributes**</span></span> | [<span data-ttu-id="0c193-110">**uomo: counterAttributes**</span><span class="sxs-lookup"><span data-stu-id="0c193-110">**man:counterAttributes**</span></span>](performance-counters-counterattributes-complex-type.md) | <span data-ttu-id="0c193-111">Elenca gli attributi univoci che specificano la modalità di visualizzazione dei dati del contatore in un'applicazione consumer.</span><span class="sxs-lookup"><span data-stu-id="0c193-111">Lists the unique attributes that specify how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="0c193-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="0c193-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c193-113">Nome</span><span class="sxs-lookup"><span data-stu-id="0c193-113">Name</span></span></th>
<th><span data-ttu-id="0c193-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c193-114">Type</span></span></th>
<th><span data-ttu-id="0c193-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c193-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0c193-116">aggregate</span><span class="sxs-lookup"><span data-stu-id="0c193-116">aggregate</span></span></td>

<td><span data-ttu-id="0c193-117">Funzione di aggregazione da applicare se l'attributo <strong>instances</strong> del <a href="performance-counters-counterset-complex-type.md"><strong>contatore</strong></a> è GlobalAggregate, multipleAggregate o globalAggregateHistory.</span><span class="sxs-lookup"><span data-stu-id="0c193-117">The aggregation function to apply if the <strong>instances</strong> attribute of <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> is globalAggregate, multipleAggregate, or globalAggregateHistory.</span></span> <span data-ttu-id="0c193-118">Di seguito sono riportate le possibili funzioni di aggregazione che è possibile applicare:</span><span class="sxs-lookup"><span data-stu-id="0c193-118">The following are the possible aggregation functions that you can apply:</span></span><br/> <dl> <span data-ttu-id="0c193-119"><dt><span id="max"></span><span id="MAX"></span>Max</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-119"><dt><span id="max"></span><span id="MAX"></span>max</dt> </span></span><dd> <span data-ttu-id="0c193-120">Viene restituito il valore massimo del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-120">The maximum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="0c193-121"><dt><span id="min"></span><span id="MIN"></span>min</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-121"><dt><span id="min"></span><span id="MIN"></span>min</dt> </span></span><dd> <span data-ttu-id="0c193-122">Viene restituito il valore minimo del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-122">The minimum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="0c193-123"><dt><span id="avg"></span><span id="AVG"></span>AVG</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-123"><dt><span id="avg"></span><span id="AVG"></span>avg</dt> </span></span><dd> <span data-ttu-id="0c193-124">Viene restituito il valore medio del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-124">The average counter value is returned.</span></span><br/> </dd> <span data-ttu-id="0c193-125"><dt><span id="sum"></span><span id="SUM"></span>somma</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-125"><dt><span id="sum"></span><span id="SUM"></span>sum</dt> </span></span><dd> <span data-ttu-id="0c193-126">Viene restituita la somma dei valori del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-126">The sum of the counter values is returned.</span></span><br/> </dd> <span data-ttu-id="0c193-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>non definito</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>undefined</dt> </span></span><dd> <span data-ttu-id="0c193-128">Non aggregare questo contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-128">Do not aggregate this counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c193-129">baseID</span><span class="sxs-lookup"><span data-stu-id="0c193-129">baseID</span></span></td>
<td><span data-ttu-id="0c193-130"><a href="performance-counters-uint32type-simple-type.md"><strong>uomo: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c193-130"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="0c193-131">Identificatore di un altro contatore nello stesso insieme di contatori, il cui valore viene utilizzato per calcolare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-131">The identifier of another counter within the same counter set, whose value is used to calculate this counter's value.</span></span> <span data-ttu-id="0c193-132">I tipi di contatori seguenti richiedono un contatore di base:</span><span class="sxs-lookup"><span data-stu-id="0c193-132">The following counter types require a base counter:</span></span><br/> <dl> <span data-ttu-id="0c193-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span></span><dd> <span data-ttu-id="0c193-134">Richiede il contatore di base PERF_AVERAGE_BASE.</span><span class="sxs-lookup"><span data-stu-id="0c193-134">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="0c193-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span></span><dd> <span data-ttu-id="0c193-136">Richiede il contatore di base PERF_AVERAGE_BASE.</span><span class="sxs-lookup"><span data-stu-id="0c193-136">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="0c193-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span></span><dd> <span data-ttu-id="0c193-138">Richiede il contatore di base PERF_COUNTER_MULTI_BASE.</span><span class="sxs-lookup"><span data-stu-id="0c193-138">Requires the PERF_COUNTER_MULTI_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="0c193-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="0c193-140">Richiede il contatore di base PERF_LARGE_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="0c193-140">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="0c193-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span></span><dd> <span data-ttu-id="0c193-142">Richiede il contatore di base PERF_LARGE_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="0c193-142">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="0c193-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="0c193-144">Richiede il contatore di base PERF_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="0c193-144">Requires the PERF_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="0c193-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span></span><dd> <span data-ttu-id="0c193-146">Richiede il contatore di base PERF_SAMPLE_BASE.</span><span class="sxs-lookup"><span data-stu-id="0c193-146">Requires the PERF_SAMPLE_BASE base counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c193-147">defaultScale</span><span class="sxs-lookup"><span data-stu-id="0c193-147">defaultScale</span></span></td>

<td><span data-ttu-id="0c193-148">Fattore di scala da applicare al valore del contatore (fattore \* valore del contatore).</span><span class="sxs-lookup"><span data-stu-id="0c193-148">The scale factor to apply to the counter value (factor \* counter value).</span></span> <span data-ttu-id="0c193-149">Il valore predefinito è zero se non viene applicata alcuna scala.</span><span class="sxs-lookup"><span data-stu-id="0c193-149">The default is zero if no scale is applied.</span></span> <span data-ttu-id="0c193-150">I valori validi sono compresi tra 10 e 10 (da 0,0000000001 a 1 miliardo).</span><span class="sxs-lookup"><span data-stu-id="0c193-150">Valid values range from  10 to 10 (0.0000000001 to 1000000000).</span></span> <span data-ttu-id="0c193-151">Se questo valore è zero, il valore di scala è 1; Se questo valore è 1, il valore della scala è 10. Se questo valore è 1, il valore della scala è. 10; E così via.</span><span class="sxs-lookup"><span data-stu-id="0c193-151">If this value is zero, the scale value is 1; if this value is 1, the scale value is 10; if this value is  1, the scale value is .10; and so on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c193-152">description</span><span class="sxs-lookup"><span data-stu-id="0c193-152">description</span></span></td>
<td><span data-ttu-id="0c193-153"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-153"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="0c193-154">Breve descrizione del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-154">A short description of the counter.</span></span> <span data-ttu-id="0c193-155">Non è necessario specificare questo attributo se il contatore include l'attributo <a href="performance-counters-counterattribute-complex-type.md"><strong>NoDisplay</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0c193-155">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c193-156">detailLevel</span><span class="sxs-lookup"><span data-stu-id="0c193-156">detailLevel</span></span></td>

<td><span data-ttu-id="0c193-157">Specifica i destinatari per i dettagli del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-157">Specifies the target audience for the counter details.</span></span> <span data-ttu-id="0c193-158">Di seguito sono indicati i valori possibili:</span><span class="sxs-lookup"><span data-stu-id="0c193-158">The following are the possible values:</span></span><br/> <dl> <span data-ttu-id="0c193-159"><dt><span id="standard"></span><span id="STANDARD"></span>standard</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-159"><dt><span id="standard"></span><span id="STANDARD"></span>standard</dt> </span></span><dd> <span data-ttu-id="0c193-160">Visualizza i dettagli sul contatore che un utente comune potrebbe comprendere.</span><span class="sxs-lookup"><span data-stu-id="0c193-160">Display details about the counter that a typical user would understand.</span></span><br/> </dd> <span data-ttu-id="0c193-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>avanzate</dt> </span><span class="sxs-lookup"><span data-stu-id="0c193-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>advanced</dt> </span></span><dd> <span data-ttu-id="0c193-162">Visualizza i dettagli sul contatore che solo un utente avanzato può comprendere.</span><span class="sxs-lookup"><span data-stu-id="0c193-162">Display details about the counter that only an advanced user would understand.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c193-163">campo</span><span class="sxs-lookup"><span data-stu-id="0c193-163">field</span></span></td>
<td><span data-ttu-id="0c193-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>uomo: CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c193-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="0c193-165">Nome di un campo all'interno dello struct che contiene il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-165">The name of a field within the struct that contains the counter value.</span></span> <span data-ttu-id="0c193-166">Questo attributo non è consentito per i provider in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="0c193-166">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c193-167">id</span><span class="sxs-lookup"><span data-stu-id="0c193-167">id</span></span></td>
<td><span data-ttu-id="0c193-168"><a href="performance-counters-uint32type-simple-type.md"><strong>uomo: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c193-168"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="0c193-169">Numero univoco che identifica il contatore all'interno dell'insieme di contatori.</span><span class="sxs-lookup"><span data-stu-id="0c193-169">A unique number that identifies the counter within the counter set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c193-170">multiCounterID</span><span class="sxs-lookup"><span data-stu-id="0c193-170">multiCounterID</span></span></td>
<td><span data-ttu-id="0c193-171"><a href="performance-counters-uint32type-simple-type.md"><strong>uomo: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c193-171"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="0c193-172">Identificatore di un altro contatore nello stesso insieme di contatori, il cui valore del moltiplicatore viene usato per calcolare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-172">The identifier of another counter within the same counter set, whose multiplier value is used to calculate this counter's value.</span></span> <span data-ttu-id="0c193-173">I tipi di contatori seguenti richiedono un valore moltiplicatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-173">The following counter types require a multiplier value.</span></span> <span data-ttu-id="0c193-174">Il contatore a cui viene fatto riferimento deve essere di tipo PERF_COUNTER_RAWCOUNT.</span><span class="sxs-lookup"><span data-stu-id="0c193-174">The referenced counter must be of type PERF_COUNTER_RAWCOUNT.</span></span><br/>
<ul>
<li><span data-ttu-id="0c193-175">PERF_COUNTER_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="0c193-175">PERF_COUNTER_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="0c193-176">PERF_COUNTER_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="0c193-176">PERF_COUNTER_MULTI_TIMER_INV</span></span></li>
<li><span data-ttu-id="0c193-177">PERF_100NSEC_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="0c193-177">PERF_100NSEC_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="0c193-178">PERF_100NSEC_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="0c193-178">PERF_100NSEC_MULTI_TIMER_INV</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c193-179">name</span><span class="sxs-lookup"><span data-stu-id="0c193-179">name</span></span></td>

<td><span data-ttu-id="0c193-180">Nome del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-180">The name of the counter.</span></span> <span data-ttu-id="0c193-181">Il nome deve essere univoco e inferiore a 1.024 caratteri.</span><span class="sxs-lookup"><span data-stu-id="0c193-181">The name must be unique and less than 1,024 characters.</span></span> <span data-ttu-id="0c193-182">Per il nome è prevista la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0c193-182">The name is case-sensitive.</span></span> <span data-ttu-id="0c193-183">Non è necessario specificare questo attributo se il contatore include l'attributo <a href="performance-counters-counterattribute-complex-type.md"><strong>NoDisplay</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0c193-183">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c193-184">perfFreqID</span><span class="sxs-lookup"><span data-stu-id="0c193-184">perfFreqID</span></span></td>
<td><span data-ttu-id="0c193-185"><a href="performance-counters-uint32type-simple-type.md"><strong>uomo: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c193-185"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="0c193-186">Identificatore di un altro contatore nello stesso insieme di contatori, il cui valore Frequency viene utilizzato per calcolare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-186">The identifier of another counter within the same counter set, whose frequency value is used to calculate this counter's value.</span></span> <span data-ttu-id="0c193-187">I tipi di contatori seguenti richiedono una frequenza.</span><span class="sxs-lookup"><span data-stu-id="0c193-187">The following counter types require a frequency.</span></span> <span data-ttu-id="0c193-188">Il tipo di contatore PERF_COUNTER_LARGE_RAWCOUNT contiene il valore del timestamp.</span><span class="sxs-lookup"><span data-stu-id="0c193-188">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="0c193-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="0c193-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="0c193-190">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="0c193-190">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="0c193-191">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="0c193-191">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="0c193-192">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="0c193-192">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c193-193">perfTimeID</span><span class="sxs-lookup"><span data-stu-id="0c193-193">perfTimeID</span></span></td>
<td><span data-ttu-id="0c193-194"><a href="performance-counters-uint32type-simple-type.md"><strong>uomo: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c193-194"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="0c193-195">Identificatore di un altro contatore nello stesso insieme di contatori, il cui valore timestamp viene utilizzato per calcolare il valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-195">The identifier of another counter within the same counter set, whose time stamp value is used to calculate this counter's value.</span></span> <span data-ttu-id="0c193-196">I tipi di contatori seguenti richiedono un timestamp.</span><span class="sxs-lookup"><span data-stu-id="0c193-196">The following counter types require a time stamp.</span></span> <span data-ttu-id="0c193-197">Il tipo di contatore PERF_COUNTER_LARGE_RAWCOUNT contiene il valore del timestamp.</span><span class="sxs-lookup"><span data-stu-id="0c193-197">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="0c193-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="0c193-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="0c193-199">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="0c193-199">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="0c193-200">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="0c193-200">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="0c193-201">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="0c193-201">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c193-202">struct</span><span class="sxs-lookup"><span data-stu-id="0c193-202">struct</span></span></td>
<td><span data-ttu-id="0c193-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>uomo: CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c193-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="0c193-204">Nome di un elemento struct che contiene questo valore del contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-204">The name of a struct element that contains this counter value.</span></span> <span data-ttu-id="0c193-205">Questo attributo non è consentito per i provider in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="0c193-205">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c193-206">simbolo</span><span class="sxs-lookup"><span data-stu-id="0c193-206">symbol</span></span></td>
<td><span data-ttu-id="0c193-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>uomo: CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="0c193-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="0c193-208">Nome simbolico che identifica il contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-208">A symbolic name that identifies the counter.</span></span> <span data-ttu-id="0c193-209">Lo strumento <a href="ctrpp.md">CTRPP</a> crea una costante che è possibile usare quando si chiamano funzioni che richiedono un identificatore del contatore (ad esempio, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="0c193-209">The <a href="ctrpp.md">CTRPP</a> tool creates a constant that you can use when calling functions that require a counter identifier (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>).</span></span> <span data-ttu-id="0c193-210">Il nome della costante è il nome simbolico.</span><span class="sxs-lookup"><span data-stu-id="0c193-210">The name of the constant is the symbolic name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0c193-211">tipo</span><span class="sxs-lookup"><span data-stu-id="0c193-211">type</span></span></td>

<td><span data-ttu-id="0c193-212">Nome del tipo di contatore.</span><span class="sxs-lookup"><span data-stu-id="0c193-212">The name of the counter type.</span></span> <span data-ttu-id="0c193-213">Per i valori possibili, vedere il blocco di sintassi precedente.</span><span class="sxs-lookup"><span data-stu-id="0c193-213">For possible values, see the above syntax block.</span></span> <span data-ttu-id="0c193-214">Per informazioni dettagliate su ogni tipo, vedere <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">tipi di contatori</a> nella Guida alla distribuzione di Windows 2003.</span><span class="sxs-lookup"><span data-stu-id="0c193-214">For details of each type, see <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Counter Types</a> in the Windows 2003 Deployment Guide.</span></span> <span data-ttu-id="0c193-215">Il nome fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0c193-215">The name is case-sensitive use lowercase.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0c193-216">Uri</span><span class="sxs-lookup"><span data-stu-id="0c193-216">uri</span></span></td>
<td><span data-ttu-id="0c193-217"><strong>XS: anyURI</strong></span><span class="sxs-lookup"><span data-stu-id="0c193-217"><strong>xs:anyURI</strong></span></span></td>
<td><span data-ttu-id="0c193-218">Identificatore univoco della risorsa uniforme che consente agli utenti di recuperare i valori dei contatori da qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="0c193-218">A unique uniform resource identifier that lets users retrieve counter values from any location.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="0c193-219">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c193-219">Remarks</span></span>

<span data-ttu-id="0c193-220">Per garantire la compatibilità con le versioni precedenti, ogni contatore nell'insieme di contatori deve specificare gli stessi valori **perfFreqID** e **perfTimeID** .</span><span class="sxs-lookup"><span data-stu-id="0c193-220">To provide backwards-compatibility, each counter in the counter set should specify the same **perfFreqID** and **perfTimeID** values.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c193-221">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c193-221">Requirements</span></span>



| <span data-ttu-id="0c193-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c193-222">Requirement</span></span> | <span data-ttu-id="0c193-223">Valore</span><span class="sxs-lookup"><span data-stu-id="0c193-223">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c193-224">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c193-224">Minimum supported client</span></span><br/> | <span data-ttu-id="0c193-225">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c193-225">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0c193-226">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c193-226">Minimum supported server</span></span><br/> | <span data-ttu-id="0c193-227">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c193-227">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

