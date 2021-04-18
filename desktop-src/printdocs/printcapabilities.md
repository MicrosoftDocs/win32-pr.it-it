---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c6dd8ce98b071f1eb239762544a9b72160035
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321064"
---
# <a name="printcapabilities"></a>PrintCapabilities

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento PrintCapabilities rappresenta la radice del documento PrintCapabilities. Il documento PrintCapabilities contiene tutte le informazioni necessarie per descrivere gli attributi del dispositivo supportati, in base a una particolare configurazione del dispositivo.

## <a name="element-tag"></a>Tag elemento

<PrintCapabilities>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML      | Dettagli                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Specifica la versione dello schema che definisce i tipi di elemento e la relativa struttura. L'attributo Version è di tipo Integer. La versione dello schema corrente è "1". Questo attributo è obbligatorio. <br/> |



 

Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.



| Category                   | Dettagli                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | Solo radice del documento.<br/>                                                                                    |
| Elementi figlio<br/>  | *Funzionalità* (zero o più)<br/> *ParameterDef* (zero o più)<br/> *Property* (zero o più)<br/> |
| Questo elemento<br/>    | Non sono consentiti dati di tipo carattere.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/>                 |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

L'elemento radice non può avere dipendenze di configurazione.

## <a name="example"></a>Esempio

Vedere [esempio di documento PrintCapabilities](printcapabilities-document-example.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




