---
description: Descrive uno spazio dei nomi.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: nameSpace - elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c3e2735efbb99fbe404f2531336c2e2bd0f89d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994278"
---
# <a name="namespace-element"></a>nameSpace - elemento

Descrive uno spazio dei nomi. Questo spazio dei nomi può essere usato per la generazione di codice o per la \<wsdl:import> gestione delle direttive .

## <a name="usage"></a>Utilizzo

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a>Attributi



| Attributo          | Type                         | Obbligatoria       | Descrizione                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| **Uri**<br/> | stringa di \_ caratteri<br/> | Sì<br/> | URI univoco dello spazio dei nomi.<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                               | Descrizione                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>               | Nome da utilizzare per identificare lo spazio dei nomi nel codice generato.<br/> <br/>                  |
| [**macroPrefix**](macroprefix.md)<br/>         | Prefisso da utilizzare nel codice generato per i nomi delle macro nello spazio dei nomi .<br/> <br/> |
| [**Nome**](name.md)<br/>                       | Nome completo nello spazio dei nomi .<br/> <br/>                                                |
| [**preferredPrefix**](preferredprefix.md)<br/> | Prefisso a cui deve essere eseguito il mapping dello spazio dei nomi per rendere il codice XML più leggibile.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                                     | Descrizione                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento radice di un file script XML del generatore di codice WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo elemento può essere utilizzato per fornire al generatore di codice informazioni aggiuntive sugli spazi dei nomi rilevati nei file WSDL e XSD o per introdurre nuovi spazi dei nomi.

Gli spazi dei nomi impliciti nella reflection del tipo o specificati nei file WSDL e XSD vengono analizzati automaticamente dal generatore di codice e non devono essere definiti in modo esplicito nello script. In alcuni casi, questo elemento può essere utilizzato per aggiungere proprietà o nomi aggiuntivi a uno spazio dei nomi a cui fa riferimento la reflection del tipo o WSDL/XSD. Il generatore di codice non considera questo tipo di conflitto.

Nel codice XML seguente viene illustrato un elemento nameSpace (con elementi figlio omessi per brevità).

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




