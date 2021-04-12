---
description: Descrive uno spazio dei nomi.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: nameSpace-elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8747a25988b880d5287d959273fa0f4d144045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528579"
---
# <a name="namespace-element"></a>nameSpace-elemento

Descrive uno spazio dei nomi. Questo spazio dei nomi può essere utilizzato per la generazione di codice o per la gestione di <WSDL: Import> direttive.

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
| **Uri**<br/> | stringa di caratteri \_<br/> | Sì<br/> | URI univoco dello spazio dei nomi.<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                               | Descrizione                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**codeName**](codename.md)<br/>               | Nome da utilizzare per identificare lo spazio dei nomi nel codice generato.<br/> <br/>                  |
| [**macroPrefix**](macroprefix.md)<br/>         | Prefisso da utilizzare nel codice generato per i nomi delle macro nello spazio dei nomi.<br/> <br/> |
| [**nome**](name.md)<br/>                       | Nome completo nello spazio dei nomi.<br/> <br/>                                                |
| [**preferredPrefix**](preferredprefix.md)<br/> | Prefisso a cui deve essere eseguito il mapping dello spazio dei nomi per rendere più leggibile il codice XML.<br/> <br/> |



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
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento radice di un file di script XML del generatore di codice WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo elemento può essere utilizzato per fornire al generatore di codice ulteriori informazioni sugli spazi dei nomi rilevati nei file WSDL e XSD o per introdurre nuovi spazi dei nomi.

Gli spazi dei nomi impliciti nella reflection del tipo o specificati nei file WSDL e XSD vengono analizzati automaticamente dal generatore di codice e non devono essere definiti in modo esplicito nello script. In alcuni casi, questo elemento può essere utilizzato per aggiungere ulteriori proprietà o nomi a uno spazio dei nomi a cui fa riferimento il tipo reflection o WSDL/XSD. Il generatore di codice non considera questa situazione un conflitto.

Nel codice XML seguente viene illustrato un elemento nameSpace (con elementi figlio omessi per brevità).

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




