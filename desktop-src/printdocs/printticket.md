---
description: Trovare informazioni sull'elemento PrintTicket. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b279ff681704a63f6547738c73fb9192d6f8a65d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120076"
---
# <a name="printticket"></a>PrintTicket

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento PrintTicket è l'elemento radice del documento PrintTicket. Un elemento PrintTicket contiene tutte le informazioni di formattazione del processo necessarie per l'output di un processo.

## <a name="element-tag"></a>Element Tag

<PrintTicket>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML      | Dettagli                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Specifica la versione dello schema che definisce i tipi di elemento e la relativa struttura, un valore letterale di tipo integer. La versione corrente dello schema è "1". Questo attributo è obbligatorio. <br/> |



 

Per altre informazioni, vedere la [sezione Attributi](xml-attributes.md) XML.

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.



| Categoria                   | Dettagli                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | Solo radice del documento.<br/>                                                                                     |
| Elementi figlio<br/>  | *Funzionalità* (zero o più)<br/> *ParameterInit* (zero o più)<br/> *Proprietà* (zero o più)<br/> |
| Questo elemento<br/>    | Non sono consentiti dati di tipo carattere.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/>                  |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Le dipendenze di configurazione sono applicabili solo agli elementi in un documento PrintCapabilities.

## <a name="example"></a>Esempio

Vedere [Esempio di PrintTicket.](printticket-example.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




