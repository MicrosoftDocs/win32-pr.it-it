---
description: Genera implementazioni per le funzioni proxy per le operazioni del tipo di porta.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: elemento proxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a27e217cfa3d0a9efd204a1b18c7b2f0ca16f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883989"
---
# <a name="proxyfunctionimplementations-element"></a>elemento proxyFunctionImplementations

Genera implementazioni per le funzioni proxy per le operazioni del tipo di porta.

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
| [**async**](async.md)<br/>           | Specifica se le operazioni asincrone sono incluse nelle funzioni proxy generate.<br/> <br/>         |
| [**eventi**](events.md)<br/>         | Specifica se gli eventi correlati sono inclusi nelle funzioni generate.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>   | Specifica se i parametri utilizzati per passare informazioni sugli errori sono inclusi nelle funzioni generate.<br/> <br/> |
| [**operazione**](operation.md)<br/>   | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>                                        |
| [**portType**](porttype.md)<br/>     | Specifica il tipo di porta per il quale deve essere generato il codice.<br/> <br/>                                       |
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
| [**file**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




