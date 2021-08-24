---
description: Informazioni sull'elemento ParameterInit, che definisce un valore per un'istanza di un elemento ParameterDef.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b961ede78b313e7fb3655024705a13f04edb947344493be4fe49ff14b5d00843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947857"
---
# <a name="parameterinit"></a>ParameterInit

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Definisce un valore per un'istanza di un elemento ParameterDef. Un elemento ParameterInit è la destinazione del riferimento effettuato da un elemento ParameterRef.

## <a name="element-tag"></a>Tag di elemento

<ParameterInit>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML   | Dettagli                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene l'attributo name dell'elemento ParameterDef che deve essere inizializzato nel contesto del documento corrente.<br/> |



 

Per altre informazioni, vedere la [sezione Attributi XML.](xml-attributes.md)

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.



| Category                   | Nome o restrizione                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------|
| Elementi padre<br/> | PrintTicket (radice PrintTicket)<br/>                                                         |
| Elementi figlio<br/>  | Valore (uno)<br/>                                                                            |
| Questo elemento<br/>    | Non sono consentiti dati di tipo carattere.<br/> Gli elementi di pari livello figlio duplicati non sono consentiti.<br/> |



 

## <a name="configuration-dependencies"></a>Dipendenze di configurazione

nessuno

## <a name="example"></a>Esempio

Nell'esempio seguente viene inizializzato un parametro su 1. L'esempio in [ParameterDef](parameterdef.md) illustra come impostare tutti gli elementi Property necessari per questo parametro.

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




