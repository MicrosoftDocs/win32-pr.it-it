---
description: Esaminare gli elementi Feature, che contengono un elenco di elementi Option e Property che descrivono un attributo del dispositivo, un'impostazione di formattazione del processo o altre caratteristiche rilevanti.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28ab7e8cc69ecc9ba3956fbae3c5278baace8cf
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120636"
---
# <a name="feature"></a>Funzionalità

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento Feature contiene un elenco completo degli elementi Option e Property che descrivono completamente un attributo del dispositivo, un'impostazione di formattazione del processo o altre caratteristiche rilevanti.

## <a name="element-tag"></a>Tag di elemento

<Feature>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML   | Dettagli                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene il nome della funzionalità, una funzionalità standard o una funzionalità definita privatamente. <br/> |



 

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
<td>PrintCapabilities <br/> PrintTicket <br/> Funzionalità<br/></td>
</tr>
<tr class="even">
<td>Elementi figlio<br/></td>
<td>Uno dei gruppi seguenti:<br/>
<ul>
<li><em>Funzionalità</em> (zero o più)<br/></li>
<li><em>Opzione</em> (una o più)<br/></li>
<li><em>Proprietà</em> (zero o più)<br/></li>
</ul>
oppure <br/>
<ul>
<li><em>Funzionalità</em> (una o più)<br/></li>
<li><em>Opzione</em> (zero o più)<br/></li>
<li><em>Proprietà</em> (zero o più)<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Questo elemento<br/></td>
<td>Non sono consentiti dati di tipo carattere.<br/> Sono consentiti elementi Option figlio duplicati di pari livello. Tasti di scelta rapida degli attributi nome duplicati consentiti. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Gli elementi di funzionalità potrebbero non avere dipendenze di configurazione.

## <a name="element-usage"></a>Utilizzo degli elementi

### <a name="relationship-to-xml-attributes"></a>Relazione con gli attributi XML

Nella rappresentazione di funzionalità/opzione un attributo del dispositivo è rappresentato da un elemento Feature. L'attributo device è identificato in modo univoco dall'attributo name nell'elemento Feature dell'attributo device, come nell'esempio seguente. In questo esempio l'attributo del dispositivo è Resolution.

``` syntax
<Feature name="Resolution" />
```

Lo schema di stampa definisce un set di attributi del nome per determinate istanze di funzionalità. Questi attributi di nome consentono di identificare un set di istanze di funzionalità predefinite associate a specifici attributi di dispositivo configurabili. Questi nomi di istanza di funzionalità devono essere usati quando applicabile, perché aumentano la portabilità del documento PrintCapabilities e degli oggetti PrintTicket derivati da essi. Le istanze di funzionalità definite privatamente possono essere introdotte se alcuni attributi del dispositivo non corrispondono a nessuna delle istanze di funzionalità definite nello schema. Per informazioni sulla sintassi per gli attributi del nome e sulle convenzioni applicabili ai nomi definiti da schema e definiti privatamente, vedere [Attributi XML](xml-attributes.md).

### <a name="relationship-to-option-element"></a>Relazione con l'elemento Option

Ognuno degli stati possibili è rappresentato da un elemento Option. Ogni definizione di opzione contiene uno o più elementi ScoredProperty, che insieme descrivono o caratterizzano in modo univoco lo stato rappresentato. La tecnica usata per creare le definizioni delle opzioni è descritta in [Definizioni di opzioni](option-definitions.md). Tutti gli elementi Option associati a un particolare elemento Feature risiedono come elementi figlio dell'elemento Feature.

### <a name="subfeatures"></a>Funzionalità secondarie

Print Schema Framework consente anche di raggruppare gli elementi feature in modo gerarchico. Ovvero, un elemento Feature può contenere uno o più elementi Feature figlio (sottofeature). Ciò può essere utile per organizzare gli elementi feature correlati o per gli elementi Feature che controllano gli aspetti di una funzionalità del dispositivo. Un esempio è un dispositivo che supporta la graffatura. Un dispositivo di questo tipo potrebbe offrire all'utente la possibilità di scegliere dove trovare la graffatura, ad esempio nell'angolo superiore sinistro o nell'angolo superiore destro, lungo il bordo superiore o lungo il bordo sinistro. L'interfaccia utente per questo dispositivo deve essere in grado di presentare prima all'utente le scelte di livello più alto, che in questo caso è se usare la graffatura. Solo dopo che l'utente ha deciso di usare la graffatura, deve presentarsi con un secondo livello di scelta, la posizione di graffatura. Una gerarchia di funzionalità aggiunge la struttura aggiuntiva che rende possibile un'interfaccia utente di questo tipo. Print Schema Framework consente alle sottofeature di avere sottofeature figlio, consentendo un livello illimitato di annidamento.

Print Schema Framework consente anche di visualizzare gli elementi Option allo stesso livello delle sottofeature. cio, come elementi di pari livello all'interno dello stesso elemento Feature padre. In questo modo l'utente può prendere la decisione di alto livello (se usare la graffatura) prima di effettuare le selezioni delle sottofeature. Per questo esempio l'elemento Feature radice, "Staple", può contenere due elementi Option, "On" e "Off", nonché una sottofeature denominata "StapleLocation".

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

 

 




