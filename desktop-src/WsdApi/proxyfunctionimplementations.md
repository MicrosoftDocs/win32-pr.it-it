---
description: Genera implementazioni per le funzioni proxy per le operazioni sul tipo di porta.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: Elemento proxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d64ae53d76100e5d38e1dd1a363f64a1004284b6f8a35ce5eb4e49d6d1e9a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552430"
---
# <a name="proxyfunctionimplementations-element"></a>Elemento proxyFunctionImplementations

Genera implementazioni per le funzioni proxy per le operazioni sul tipo di porta.

## <a name="usage"></a>Utilizzo

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                     | Descrizione                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**async**](async.md)<br/>           | Specifica se le operazioni asincrone vengono incluse nelle funzioni proxy generate.<br/> <br/>         |
| [**Eventi**](events.md)<br/>         | Specifica se gli eventi correlati vengono inclusi nelle funzioni generate.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>   | Specifica se i parametri utilizzati per passare le informazioni sugli errori vengono inclusi nelle funzioni generate.<br/> <br/> |
| [**Operazione**](operation.md)<br/>   | Specifica un'operazione per cui deve essere generato il codice.<br/> <br/>                                        |
| [**Porttype**](porttype.md)<br/>     | Specifica il tipo di porta per cui deve essere generato il codice.<br/> <br/>                                       |
| [**proxyClass**](proxyclass.md)<br/> | Specifica il nome della classe proxy sul lato client.<br/> <br/>                                               |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
  faultInfo?
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
| Può essere vuoto                        | Sì           |



 

 




