---
description: Genera implementazioni per le funzioni stub per le operazioni di tipo porta.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: elemento stubDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6676cfc6cf55aa9c9961bd614506500d847def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313145"
---
# <a name="stubdefinitions-element"></a>elemento stubDefinitions

Genera implementazioni per le funzioni stub per le operazioni di tipo porta.

## <a name="usage"></a>Utilizzo

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a>Attributi

Non ci sono attributi.

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                         | Descrizione                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**deallocatore**](deallocator.md)<br/>                   | Specifica il tipo di deallocatore che deve essere utilizzato da una funzione stub.<br/> <br/>                                 |
| [**eventArg**](eventarg.md)<br/>                         | Specifica se gli argomenti dell'evento correlati sono inclusi nelle funzioni generate.<br/> <br/>               |
| [**eventi**](events.md)<br/>                             | Specifica se gli eventi correlati sono inclusi nelle funzioni generate.<br/> <br/>                        |
| [**faultInfo**](faultinfo.md)<br/>                       | Specifica se i parametri utilizzati per passare informazioni sugli errori sono inclusi nelle funzioni generate.<br/> <br/> |
| [**operazione**](operation.md)<br/>                       | Specifica un'operazione per la quale deve essere generato il codice.<br/> <br/>                                        |
| [**operationDeallocator**](operationdeallocator.md)<br/> | Specifica il tipo di deallocatore che deve essere utilizzato dalla funzione stub di un'operazione.<br/> <br/>                    |
| [**portType**](porttype.md)<br/>                         | Specifica il tipo di porta per il quale deve essere generato il codice.<br/> <br/>                                       |
| [**serverClass**](serverclass.md)<br/>                   | Specifica il nome della classe server sul lato host.<br/> <br/>                                                |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
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
| Può essere vuoto                        | No            |



 

 




