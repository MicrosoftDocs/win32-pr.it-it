---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 933528f6-8f34-4509-887c-c7c223c79367
title: Valore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a8f8c5bf9e2ec1696d6282b859fc99b7701159
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320880"
---
# <a name="value"></a>Valore

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento Value associa un valore letterale a un tipo.

## <a name="element-tag"></a>Tag elemento

<Value>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML       | Dettagli                                                                                                                                                                          |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| xsi:type<br/> | Specifica il tipo di dati di value, che deve essere uno dei seguenti tipi definiti da XSD: String, Integer, Decimal, QName. Se mancante, il tipo di dati predefinito è String.<br/> |



 

Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.



| Category                   | Dettagli                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | ParameterInit <br/> Proprietà<br/> ScoredProperty<br/>                                                                                   |
| Elementi figlio<br/>  | È consentito solo il contenuto di tipo carattere o Integer.<br/>                                                                                                |
| Questo elemento<br/>    | Contenuto null consentito. Il contenuto carattere deve essere conforme alla sintassi definita dal tipo di dati.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/> |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Gli elementi valore visualizzati all'interno dell'elemento ScoredProperty non possono avere dipendenze di configurazione. Gli elementi valore visualizzati negli elementi Property possono avere dipendenze arbitrarie dalla configurazione.

## <a name="element-usage"></a>Utilizzo elementi

Un elemento Value può essere visualizzato all'interno di una proprietà o di un elemento ScoredProperty. Lo scopo dell'elemento value è rappresentare un valore come tipo di dati XML standard. Il tipo di dati viene specificato come attributo XML dell'elemento value, xsi: Type. Si noti che non tutti i tipi definiti da XSD o XML sono supportati. Per un elenco dei tipi supportati, vedere [Riepilogo dei tipi di elemento](summary-of-element-types.md). Un elemento Value può contenere solo contenuto di tipo carattere. Nessun altro elemento può apparire come contenuto in un elemento value.

> [!Note]  
> Alcuni elementi Property definito dallo schema di stampa e ScoredProperty non contengono un elemento value, perché il loro scopo è semplicemente quello di essere elementi padre delle sottoproprietà. Non è necessario aggiungere un elemento value a tali proprietà, ovvero proprietà che non contengono un elemento value.

 

Per essere conforme a Print Schema Framework, che richiede un elemento value o sottoelementi presenti negli elementi che supportano valori, un valore assente o non definito deve essere rappresentato presentando l'elemento value come elemento vuoto. ovvero come <Value></Value>.

## <a name="example"></a>Esempio

Definire un valore di tipo Decimal e inizializzarlo su "128,5".

``` syntax
<Value xsi:type="decimal">128.5</Value>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




