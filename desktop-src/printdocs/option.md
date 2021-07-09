---
description: Ottiene informazioni sull'elemento Option. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Opzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ac4318e6a79a3d4daa77f15901d032c66134bdd
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549379"
---
# <a name="option"></a>Opzione

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento Option contiene tutti gli elementi Property e ScoredProperty associati a questa opzione.

## <a name="element-tag"></a>Element Tag

<Option>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML          | Dettagli                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vincolata<br/> | Questo attributo è facoltativo per un documento PrintCapabilities.<br/> Questo attributo indica se l'opzione è disponibile per la selezione o l'uso. Questo attributo XML può essere impostato su uno dei valori seguenti: None, PrintTicketSettings, AdminSetting o DeviceSettings. <br/> Vedere [Attributi XML](xml-attributes.md)<br/> |
| name<br/>        | Contiene il nome dell'opzione, un'opzione standard o un'opzione definita privatamente. L'attributo XML viene utilizzato in questo modo per distinguere le istanze option. <br/>                                                                                                                                                        |



 

Per altre informazioni, vedere la [sezione Attributi](xml-attributes.md) XML.

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.



| Category                   | Dettagli                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | Funzionalità <br/>                                                                                                                                                                                                                                                                              |
| Elementi figlio<br/>  | *Proprietà* (zero o più)<br/> *ScoredProperty* (zero o più per Options con attributo XML 'name'; una o più per Options che non utilizzano l'attributo XML \* 'name')<br/> \* solo le opzioni pubbliche definite nello schema di stampa non possono avere un attributo 'name', ad esempio DocumentNUp<br/> |
| Questo elemento<br/>    | Non sono consentiti dati di tipo carattere.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

Un elemento di definizione Option potrebbe non avere dipendenze di configurazione.

## <a name="element-usage"></a>Utilizzo degli elementi

Lo scopo dell'elemento Option è quello di caratterizzare uno degli stati che un attributo di configurazione del dispositivo, rappresentato da un elemento Feature, può assumere. Ogni definizione di elemento Option contiene uno o più elementi ScoredProperty che descrivono una caratteristica intrinseca o essenziale di tale opzione. Per facilitare la portabilità e la conservazione della finalità, lo schema di stampa definisce molti elementi feature comuni e un'ampia gamma di elementi Option per ogni funzionalità. È quindi importante usare gli elementi Option definiti nello schema di stampa, se possibile, prima di creare definizioni di opzione personalizzate. La comprensione del processo di definizione degli elementi Option offre informazioni utili sul modo in cui il documento PrintCapabilities e i PrintTicket vengono usati nell'architettura di stampa di Microsoft .NET Framework versione 3.0 e Windows Vista.

## <a name="example"></a>Esempio

Nell'esempio seguente viene definito un nome per l'opzione .

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




