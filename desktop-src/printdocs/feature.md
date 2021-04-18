---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89655181563e2da3a8d4841b1d90ecd4e6ac07
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321000"
---
# <a name="feature"></a>Funzionalità

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento Feature contiene un elenco completo degli elementi option e Property che descrivono completamente un attributo del dispositivo, l'impostazione della formattazione dei processi o altre caratteristiche rilevanti.

## <a name="element-tag"></a>Tag elemento

<Feature>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML   | Dettagli                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| name<br/> | Include il nome della funzionalità, ovvero una funzionalità standard o una funzionalità definita privatamente. <br/> |



 

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
<td>PrintCapabilities <br/> PrintTicket <br/> Funzionalità<br/></td>
</tr>
<tr class="even">
<td>Elementi figlio<br/></td>
<td>Uno dei seguenti gruppi:<br/>
<ul>
<li><em>Funzionalità</em> (zero o più)<br/></li>
<li><em>Opzione</em> (uno o più)<br/></li>
<li><em>Property</em> (zero o più)<br/></li>
</ul>
oppure <br/>
<ul>
<li><em>Funzionalità</em> (uno o più)<br/></li>
<li><em>Opzione</em> (zero o più)<br/></li>
<li><em>Property</em> (zero o più)<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Questo elemento<br/></td>
<td>Non sono consentiti dati di tipo carattere.<br/> Sono consentiti elementi di opzioni figlio duplicati di pari livello. Sono consentiti collegamenti a attributi nome duplicati. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Gli elementi Feature non possono avere dipendenze di configurazione.

## <a name="element-usage"></a>Utilizzo elementi

### <a name="relationship-to-xml-attributes"></a>Relazione con attributi XML

Nella rappresentazione di funzionalità/opzioni, un attributo del dispositivo è rappresentato da un elemento Feature. L'attributo Device viene identificato in modo univoco dall'attributo Name nell'elemento Feature dell'attributo Device, come nell'esempio seguente. In questo esempio, l'attributo del dispositivo è Resolution.

``` syntax
<Feature name="Resolution" />
```

Lo schema di stampa definisce un set di attributi di nome per determinate istanze di funzionalità. Questi attributi del nome servono per identificare un set di istanze di funzionalità predefinite associate a specifici attributi di dispositivo configurabili. Questi nomi di istanze di funzionalità devono essere usati quando applicabile, perché aumentano la portabilità del documento PrintCapabilities e gli PrintTicket che derivano da essi. È possibile che vengano introdotte istanze di funzionalità definite privatamente se alcuni attributi del dispositivo non corrispondono a nessuna delle istanze di funzionalità definite dallo schema. Per informazioni sulla sintassi per gli attributi Name e sulle convenzioni applicabili ai nomi definiti dallo schema e privati, vedere [attributi XML](xml-attributes.md).

### <a name="relationship-to-option-element"></a>Relazione con elemento option

Ognuno degli stati possibili è rappresentato da un elemento option. Ogni definizione di opzione contiene uno o più elementi ScoredProperty, che sono stati raggruppati in modo univoco o caratterizzano lo stato rappresentato. La tecnica utilizzata per creare le definizioni delle opzioni è descritta in [definizioni di opzioni](option-definitions.md). Tutti gli elementi option associati a un particolare elemento Feature si trovano come elementi figlio dell'elemento Feature.

### <a name="subfeatures"></a>Sottocaratteristiche

Il Framework dello schema di stampa consente inoltre di raggruppare gli elementi della funzionalità in modo gerarchico. Ovvero un elemento feature può contenere uno o più elementi Feature figlio (sottocaratteristiche). Questo può essere utile per organizzare elementi di funzionalità correlati o per elementi di funzionalità che controllano gli aspetti di una funzionalità del dispositivo. Un esempio è un dispositivo che supporta la graffettatura. Un dispositivo di questo tipo potrebbe offrire all'utente la possibilità di scegliere dove posizionare la graffetta, ad esempio nell'angolo superiore sinistro o nell'angolo superiore destro oppure lungo il bordo superiore oppure lungo il bordo sinistro. L'interfaccia utente per questo dispositivo deve essere in grado di presentare prima l'utente con le scelte di livello più alto, che in questo caso è se usare la graffettatura. Solo dopo che l'utente ha deciso di usare la pinzatura, deve essere presentato con un secondo livello di scelta, la posizione di base. Una gerarchia di funzionalità aggiunge la struttura aggiuntiva che rende possibile un'interfaccia utente di questo tipo. Il Framework dello schema di stampa consente alle funzionalità secondarie di avere le proprie funzionalità secondarie figlio, consentendo così un livello illimitato di annidamento.

Il Framework dello schema di stampa consente inoltre di visualizzare gli elementi delle opzioni allo stesso livello delle sottocaratteristiche; ovvero come elementi di pari livello all'interno dello stesso elemento della funzionalità padre. In questo modo l'utente può prendere la decisione di alto livello (se usare la graffettatura) prima di effettuare le selezioni delle sottofunzionalità. Per questo esempio l'elemento della funzionalità radice, "Staples", può contenere due elementi option, "on" e "off", nonché una sottofunzionalità denominata "StapleLocation".

## <a name="example"></a>Esempio

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option constrained="psk:None">
    <psf:ScoredProperty name="psk:Bin">
      <psf:Value xsi:type="xs:string">SorterBin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




