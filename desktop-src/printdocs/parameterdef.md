---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697d8ff89f9aa3c9c95bea9995e18e521a17596c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320962"
---
# <a name="parameterdef"></a>ParameterDef

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ParameterDef definisce le caratteristiche valide dell'input dei parametri. Il valore viene immesso per mezzo di un elemento ParameterInit.

## <a name="element-tag"></a>Tag elemento

<ParameterDef>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML   | Dettagli                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Definisce un nome univoco per il parametro nel contesto del documento corrente. Gli attributi del nome ParameterDef duplicato eseguono il rendering del documento PrintCapabilities non valido.<br/> |



 

Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
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
<td>Property (uno o più elementi)<br/> Gli elementi di proprietà standard seguenti devono apparire come contenuto di un elemento ParameterDef. <br/>
<ul>
<li>DataType <br/></li>
<li>DefaultValue <br/></li>
<li>Obbligatorio <br/></li>
<li>MaxLength o MaxValue<br/></li>
<li>MinLength o MinValue<br/></li>
<li>Più <br/></li>
<li>UnitType <br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Questo elemento<br/></td>
<td>Non sono consentiti dati di tipo carattere.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/></td>
</tr>
</tbody>
</table>



 

\*Obbligatorio quando DataType è Integer o Decimal. Facoltativo quando DataType è una stringa.

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Un ParameterDef e il relativo contenuto a qualsiasi livello di annidamento non possono avere dipendenze di configurazione.

## <a name="example"></a>Esempio

Nell'esempio seguente vengono impostati tutti gli elementi Property necessari per questo parametro. Nell'esempio in [ParameterInit](parameterinit.md) viene illustrato come inizializzare questo parametro.

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

 

 




