---
description: Trovare informazioni sull'elemento PrintTicket. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a38638083f6a6aabd0290fa3466a30fd50f7375
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884892"
---
# <a name="printticket"></a>PrintTicket

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento PrintTicket è l'elemento radice del documento PrintTicket. Un elemento PrintTicket contiene tutte le informazioni di formattazione del processo necessarie per l'output di un processo.

## <a name="element-tag"></a>Tag di elemento

&lt;PrintTicket&gt;

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML      | Dettagli                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Specifica la versione dello schema che definisce i tipi di elemento e la relativa struttura, un valore letterale di tipo Integer. La versione corrente dello schema è "1". Questo attributo è obbligatorio. <br/> |



 

Per altre informazioni, vedere la [sezione Attributi XML.](xml-attributes.md)

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.



| Category                   | Dettagli                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | Solo radice del documento.<br/>                                                                                     |
| Elementi figlio<br/>  | *Funzionalità* (zero o più)<br/> *ParameterInit* (zero o più)<br/> *Proprietà* (zero o più)<br/> |
| Questo elemento<br/>    | Non sono consentiti dati di tipo carattere.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/>                  |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Le dipendenze di configurazione sono applicabili solo agli elementi di un documento PrintCapabilities.

## <a name="example"></a>Esempio

Vedere [Esempio di PrintTicket](printticket-example.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




