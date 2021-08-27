---
description: Informazioni sull'elemento PrintCapabilities, che rappresenta la radice del documento PrintCapabilities.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef035015e8024954b32d17dd87bab929221ac78
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883928"
---
# <a name="printcapabilities"></a>PrintCapabilities

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento PrintCapabilities rappresenta la radice del documento PrintCapabilities. Il documento PrintCapabilities contiene tutte le informazioni necessarie per descrivere gli attributi del dispositivo supportati, data una particolare configurazione del dispositivo.

## <a name="element-tag"></a>Element Tag

&lt;PrintCapabilities&gt;

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML      | Dettagli                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Specifica la versione dello schema che definisce i tipi di elemento e la relativa struttura. L'attributo version è di tipo integer. La versione corrente dello schema è designata come "1". Questo attributo è obbligatorio. <br/> |



 

Per altre informazioni, vedere la [sezione Attributi](xml-attributes.md) XML.

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.



| Category                   | Dettagli                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | Solo radice del documento.<br/>                                                                                    |
| Elementi figlio<br/>  | *Funzionalità* (zero o più)<br/> *ParameterDef* (zero o più)<br/> *Proprietà* (zero o più)<br/> |
| Questo elemento<br/>    | Non sono consentiti dati di tipo carattere.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/>                 |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

L'elemento radice potrebbe non avere dipendenze di configurazione.

## <a name="example"></a>Esempio

Vedere [Esempio di documento PrintCapabilities.](printcapabilities-document-example.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




