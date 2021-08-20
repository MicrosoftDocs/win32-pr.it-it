---
description: Informazioni sull'elemento Value, che associa un valore letterale a un tipo. Il tipo di dati value deve essere string, integer, decimal o QName.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Valore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739ce465408d1cd1447de5aeac2e314e879f48f69f13735855e628c8901c2c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117685862"
---
# <a name="value"></a>Valore

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento Value associa un valore letterale a un tipo.

## <a name="element-tag"></a>Tag di elemento

<Value>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML       | Dettagli                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| xsi:type<br/> | Specifica il tipo di dati Value, che deve essere uno dei tipi definiti da XSD seguenti: string, integer, decimal, QName. Se mancante, il tipo di dati predefinito è string.<br/> |



 

Per altre informazioni, vedere la [sezione Attributi XML.](xml-attributes.md)

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.



| Category                   | Dettagli                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | ParameterInit <br/> Proprietà<br/> ScoredProperty<br/>                                                                                   |
| Elementi figlio<br/>  | È consentito solo contenuto di tipo carattere o intero.<br/>                                                                                                |
| Questo elemento<br/>    | Il contenuto Null è consentito. Il contenuto dei caratteri deve essere conforme alla sintassi definita dal tipo di dati .<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/> |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Gli elementi value visualizzati all'interno dell'elemento ScoredProperty potrebbero non avere dipendenze di configurazione. Gli elementi value visualizzati all'interno degli elementi Property possono avere dipendenze arbitrarie nella configurazione.

## <a name="element-usage"></a>Utilizzo degli elementi

Un elemento Value può essere visualizzato all'interno di un elemento Property o ScoredProperty. Lo scopo dell'elemento Value è rappresentare un valore come tipo di dati XML standard. Il tipo di dati viene specificato come attributo XML dell'elemento Value, xsi:type. Si noti che non tutti i tipi definiti da XSD o XML sono supportati. Per un elenco dei tipi supportati, vedere [Riepilogo dei tipi di elemento](summary-of-element-types.md). Un elemento Value può contenere solo contenuto di caratteri. Nessun altro elemento può essere visualizzato come contenuto in un elemento Value.

> [!Note]  
> Alcuni elementi Print Schema-defined Property e ScoredProperty non contengono un elemento Value, perché il loro scopo è semplicemente essere elementi padre di sottoproprietà. Non è consigliabile aggiungere un elemento Value a tali proprietà, ad esempio le proprietà che non contengono un elemento Value.

 

Per essere conforme a Print Schema Framework, che richiede che sia presente un elemento Value o sottoelementi negli elementi che supportano i valori, un valore assente o non definito deve essere rappresentato presentando l'elemento Value come elemento vuoto. cio, come <Value></Value>.

## <a name="example"></a>Esempio

Definire un valore di tipo decimal e inizializzarlo su "128.5".

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




