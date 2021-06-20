---
description: Informazioni sull'elemento ParameterInit, che definisce un valore per un'istanza di un elemento ParameterDef.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211fcad2c53824c7786850a7fc78c6825c219a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407264"
---
# <a name="parameterinit"></a>ParameterInit

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Definisce un valore per un'istanza di un elemento ParameterDef. Un elemento ParameterInit è la destinazione del riferimento effettuato da un elemento ParameterRef.

## <a name="element-tag"></a>Element Tag

<ParameterInit>

## <a name="xml-attributes"></a>Attributi XML

Nella tabella seguente sono elencati gli attributi XML che possono essere relativi a questo elemento.



| Attributo XML   | Dettagli                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contiene l'attributo name dell'elemento ParameterDef che deve essere inizializzato nel contesto del documento corrente.<br/> |



 

Per altre informazioni, vedere la [sezione Attributi](xml-attributes.md) XML.

## <a name="element-information"></a>Informazioni sull'elemento

Nella tabella seguente sono elencati gli elementi che possono essere elementi padre di questo elemento, gli elementi che possono essere elementi figlio di questo elemento ed eventuali restrizioni sull'elemento stesso.



| Categoria                   |                                                                                                   |
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

 

 




