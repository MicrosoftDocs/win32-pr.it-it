---
description: Informazioni sull'elemento ParameterDef, che definisce le caratteristiche valide dell'input del parametro. Il valore viene immesso tramite un elemento ParameterInit.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2682e3da11f471401e95e3f6515de5e18b6be895
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407294"
---
# <a name="parameterdef"></a>ParameterDef

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ParameterDef definisce le caratteristiche valide dell'input del parametro. Il valore viene immesso tramite un elemento ParameterInit.

## <a name="element-tag"></a>Tag di elemento

<ParameterDef>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML   | Dettagli                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Definisce un nome univoco per il parametro nel contesto del documento corrente. Gli attributi di nome ParameterDef duplicati rendono il documento PrintCapabilities non valido.<br/> |



 

Per altre informazioni, vedere la [sezione Attributi XML.](xml-attributes.md)

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Categoria</th>
<th>Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Elementi padre<br/></td>
<td>PrintCapabilities <br/></td>
</tr>
<tr class="even">
<td>Elementi figlio<br/></td>
<td>Property (uno o più elementi)<br/> Gli elementi Property standard seguenti devono essere visualizzati come contenuto di un elemento ParameterDef. <br/>
<ul>
<li>DataType <br/></li>
<li>DefaultValue <br/></li>
<li>Obbligatorio <br/></li>
<li>MaxLength o MaxValue<br/></li>
<li>MinLength o MinValue<br/></li>
<li>Multiplo* <br/></li>
<li>UnitType <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Questo elemento<br/></td>
<td>Non sono consentiti dati di tipo carattere.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/></td>
</tr>
</tbody>
</table>



 

\*Obbligatorio quando DataType è intero o decimale. Facoltativo quando DataType è string.

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Un ParameterDef e il relativo contenuto a qualsiasi livello di annidamento potrebbero non avere dipendenze di configurazione.

## <a name="example"></a>Esempio

L'esempio seguente imposta tutti gli elementi Property necessari per questo parametro. L'esempio in [ParameterInit](parameterinit.md) illustra come inizializzare questo parametro.

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




