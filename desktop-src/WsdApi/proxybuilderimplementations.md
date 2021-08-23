---
description: Genera funzioni per creare proxy tipi di dati.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: elemento proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18b13ddda25d8fa157b0399c7b9fba070534fb66e11b3fa63a122b1983dea06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815533"
---
# <a name="proxybuilderimplementations-element"></a>elemento proxyBuilderImplementations

Genera funzioni per creare proxy tipi di dati.

## <a name="usage"></a>Utilizzo

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                     | Descrizione                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>     | Nome da utilizzare per il tipo di porta nel codice generato. Per impostazione predefinita, il nome in codice viene generato dal nome completo del tipo di porta.<br/> <br/> |
| [**Porttype**](porttype.md)<br/>     | Tipo di porta per cui deve essere generato il codice.<br/> <br/>                                                                                             |
| [**classe proxy**](proxyclass.md)<br/> | Nome della classe da generare dalla funzione del generatore di proxy.<br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**File**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



| Etichetta | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




