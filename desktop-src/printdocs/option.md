---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Opzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379834d12cd01847c95783d727be5dcdc6c575bf
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321050"
---
# <a name="option"></a>Opzione

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento option contiene tutti gli elementi Property e ScoredProperty associati a questa opzione.

## <a name="element-tag"></a>Tag elemento

<Option>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML          | Dettagli                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| vincolata<br/> | Questo attributo è facoltativo per un documento PrintCapabilities.<br/> Questo attributo indica se l'opzione è disponibile per la selezione o l'utilizzo. Questo attributo XML può essere impostato su uno dei valori seguenti: None, PrintTicketSettings, AdminSetting o DeviceSettings. <br/> Vedere [attributi XML](xml-attributes.md)<br/> |
| name<br/>        | Include il nome dell'opzione, ovvero un'opzione standard o un'opzione definita privatamente. L'attributo XML viene usato in questo modo per distinguere le istanze di opzioni. <br/>                                                                                                                                                        |



 

Per ulteriori informazioni, vedere la sezione [attributi XML](xml-attributes.md) .

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento e tutte le restrizioni relative all'elemento stesso.



| Category                   | Dettagli                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | Funzionalità <br/>                                                                                                                                                                                                                                                                              |
| Elementi figlio<br/>  | *Property* (zero o più)<br/> *ScoredProperty* (zero o più opzioni con l'attributo XML ' name '; una o più opzioni per l'utilizzo dell'attributo XML ' name ' \* )<br/> \* solo le opzioni pubbliche definite nello schema di stampa non possono avere un attributo ' name ', ad esempio DocumentNUp<br/> |
| Questo elemento<br/>    | Non sono consentiti dati di tipo carattere.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Un elemento di definizione di opzione non può avere dipendenze di configurazione.

## <a name="element-usage"></a>Utilizzo elementi

Lo scopo dell'elemento option è quello di caratterizzare uno degli Stati che un attributo di configurazione del dispositivo, rappresentato da un elemento Feature, può assumere. Ogni definizione di elemento option contiene uno o più elementi ScoredProperty che descrivono una caratteristica intrinseca o essenziale di tale opzione. Per facilitare la portabilità e la conservazione dello scopo, lo schema di stampa definisce molti elementi di funzionalità comuni e una varietà di elementi option per ciascuna funzionalità. È quindi importante usare gli elementi delle opzioni di stampa definiti dallo schema, se possibile, prima di creare definizioni di opzioni personalizzate. La comprensione del processo di definizione degli elementi delle opzioni fornisce informazioni utili sul modo in cui il documento PrintCapabilities e gli PrintTicket vengono utilizzati nella versione di Microsoft .NET Framework 3,0 e nell'architettura di stampa di Windows Vista.

## <a name="example"></a>Esempio

Nell'esempio seguente viene definito un nome per l'opzione.

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




